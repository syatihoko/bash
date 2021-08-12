

##Работа с файлами     
    
Если ваши файлы не находятся в одном каталоге, вы можете использовать команду find до объединения:    
find /path/to/directory/ -name *.csv -print0 | xargs -0 -I file cat file > merged.file    
Очень полезно, когда ваши файлы уже упорядочены, и вы хотите объединить их, чтобы проанализировать их.    

Более переносимо:              
find /path/to/directory/ -name *.csv -exec cat {} + > merged.file    
Это может или не может сохранить порядок файлов.    

#Объединяем несколько текстовых     
cat * >> test.txt    


#Раскрываем все файлы в директории    
find . -name "*.gz" -exec gunzip {} \;    
