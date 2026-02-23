cd "C:\Users\LENOVO\daily-auto"

for ($i=1; $i -le 10; $i++) {
    Add-Content activity.txt "Update $i - $(Get-Date)"
    git add .
    git commit -m "Auto commit $i"
    git push
}