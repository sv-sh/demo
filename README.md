# New Project
###############################
# Копіюємо репозиторій пустий в директорію батька від нашої робочої
git clone https://github.com/sv-sh/new-project
# каталог "new-project"  перейдіть в нього

cd new-project

# Ініціалізуйте новий публічний Git-репозиторій
git init

# Створіть новий файл "README.md" і додайте до нього початковий текст
echo "# New Project" > README.md

# Підготуйте файл "README.md" до коміту
git add README.md

# Закомітьте зміни у репозиторій з коміт повідомленням "init"
git commit -m "init"

# Створіть нову гілку "development" і перейдіть до неї
git branch development
git checkout development

# Додайте інструкцію до файлу "README.md" і підготуйте їх до коміту
echo -e "\n## Development Branch\n\nThis branch is for ongoing development work." >> README.md

# Підготуйте файл "README.md" до коміту
git add README.md

# Закомітьте зміни у гілці "development" з повідомленням про коміт
git commit -m "instructioт development branch"

# Об'єднайте зміни з гілки "development" у гілку "main"
git checkout main
git merge development

# Перевірте статус, переконайтеся, що все актуально
git status

# Закомітьте зміни
git commit -m "Merge development into main"
