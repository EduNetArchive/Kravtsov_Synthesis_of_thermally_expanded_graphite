# Kravtsov Synthesis of thermally expanded graphite

0. Изображения, из которых строили кумулятивные распределения, в папках PNG-x и TNFG-x-M.
1. code/EG_Pore_Segmentation.ipynb
	Прописать пути к обрабатываемым изображениям и hdr-файлам с масштабом.
	Для этого есть переменные path_images, path_hdrs.
	Запустить все ячейки. ex.save() приведёт к сохранению csv-файла в 
	папке с изображениями path_images.
	Этот файл содержит площади всех пор на всех картинках в path_images,
	в нашем случае на 10 изображениях.
	Это было сделано для всех образцов PNG-x и TNFG-x-M.
2. Итого имеем 8 csv-файлов. Далее все данные переносим в distributions.opj.
	Это файл софта Origin 8.
	Данные каждого файла необходимо разбить по частоте от 5 мкм до максимального значения.
	Ширина бина 1 мкм. Эта процедура описана в статье.
	Таким образом получаем кумулятивные распределения.
3. Есть ещё отработка модели (без watershed) на тестовых данных.
	code/model_test.ipynb.
        Тестовые данные можно найти [тут](https://edunet.kea.su/students_datasets/Biology_and_Chemistry/Kravtsov/test_images_512x512_npy.zip).
	
Веса обученной модели можно найти [тут](https://edunet.kea.su/students_datasets/Biology_and_Chemistry/Kravtsov/best_model_FPN_efficientnet-b4_ep100_bs11_wc_wlrsch_lr0_001_imagenet.pth).
