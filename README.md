# hse_hw2_chip

Ссылка на Colab: https://colab.research.google.com/drive/1My5FQ3xjaGaiWcOsAo-dld8M7rQ7GsZU#scrollTo=PM5vR8qbDn78
### Для задания была выбрана клеточная линия PC-9, гист. метка	H3K9me2, а также 2 ChIP-seq реплики:	ENCFF531DKR и ENCFF112DNA, контроль -	ENCSR011GWK.

## Анализ Fastq
Для обеих реплик и контроля я сделала fastqc для исходных файлов, а так же сразу для подрезания. Опытным путём можно посмотреть, где это нужно, а где без этого можно обойтись.
### Результаты:
Более подробную информацию можно посмотреть в папке html, я туда загрузила оба варианта отчётов.
#### Было (ENCFF112DNA_fastqc):
![image](https://user-images.githubusercontent.com/61352475/156132379-44723d0a-d839-4c8b-ac14-355938135054.png)

Стало (ENCFF112DNA_trimmed_fastqc): 
![image](https://user-images.githubusercontent.com/61352475/156131032-f1d7a0af-c6d9-4212-8cbf-e73bfcff0070.png)


#### Было (ENCFF531DKR_fastqc):
![image](https://user-images.githubusercontent.com/61352475/156131577-29f28a8c-84b1-4768-a8af-ed9cab5f7d9e.png)

Стало (ENCFF531DKR_trimmed_fastqc):
![image](https://user-images.githubusercontent.com/61352475/156131758-1443e6e6-7b9f-413c-bfa8-b2e9ae993e2d.png)

#### Контроль было (ENCFF163PYU_fastqc) :
![image](https://user-images.githubusercontent.com/61352475/156131861-06036bbb-3105-461e-90df-0c7346d09e69.png)

Стало (ENCFF163PYU_trimmed_fastqc):
![image](https://user-images.githubusercontent.com/61352475/156132050-62405e25-c338-49db-a4b9-d69f36373099.png)

### Очевидно, что данные у нас итак хорошего качества, но я оставлю в и сходном виде только контроль (последние два скриншота).

## Выравнивание на хромосому
Следует выбрать одну хромосому (14), потому что ресурсы google colab ограничены. 

Таблица со статистикой по каждому из 3 образцов:



```
Q: Почему процент выравниваний получился именно таким?
A:
```

## Cравнение результатов



```
Q: Как можно объяснить различия в количестве пересечений?
A: Различия появляются, потому что сначала мы накладываем одни участки на другие, 
а потом вторые на первые... 
