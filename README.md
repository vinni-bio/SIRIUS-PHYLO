# МОДУЛЬ "ФИЛОГЕНОМИКА"<br/>
ОСНОВЫ ВЫЧИСЛИТЕЛЬНОЙ БИОЛОГИИ И БИОИНФОРМАТИКИ (10-22 марта 2022)

## СОДЕРЖАНИЕ
* [ПРАКТИКА #1.](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0-1-%D0%B2%D1%8B%D1%80%D0%B0%D0%B2%D0%BD%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%D1%81%D1%82%D0%B5%D0%B9) ВЫРАВНИВАНИЕ ПОСЛЕДОВАТЕЛЬНОСТЕЙ
* [ПРАКТИКА #2.](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0-2-%D0%B2%D1%8B%D0%B1%D0%BE%D1%80-%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D0%B8-%D0%B8-%D0%BF%D0%BE%D1%81%D1%82%D1%80%D0%BE%D0%B5%D0%BD%D0%B8%D0%B5-%D1%84%D0%B8%D0%BB%D0%BE%D0%B3%D0%B5%D0%BD%D0%B5%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85-%D0%B4%D0%B5%D1%80%D0%B5%D0%B2%D1%8C%D0%B5%D0%B2) ВЫБОР МОДЕЛИ И ПОСТРОЕНИЕ ФИЛОГЕНЕТИЧЕСКИХ ДЕРЕВЬЕВ
  1. [ЗАДАНИЯ: МАКСИМАЛЬНАЯ ПАРСИМОНИЯ](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BC%D0%B0%D0%BA%D1%81%D0%B8%D0%BC%D0%B0%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F-%D0%BF%D0%B0%D1%80%D1%81%D0%B8%D0%BC%D0%BE%D0%BD%D0%B8%D1%8F)
  2. [ЗАДАНИЯ: ДИСТАНЦИОННЫЕ МЕТОДЫ](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F-%D0%B4%D0%B8%D1%81%D1%82%D0%B0%D0%BD%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5-%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D1%8B)
  3. [ЗАДАНИЯ: ВЫБОР МОДЕЛИ НУКЛЕОТИДНЫХ ЗАМЕН](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F-%D0%B2%D1%8B%D0%B1%D0%BE%D1%80-%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D0%B8-%D0%BD%D1%83%D0%BA%D0%BB%D0%B5%D0%BE%D1%82%D0%B8%D0%B4%D0%BD%D1%8B%D1%85-%D0%B7%D0%B0%D0%BC%D0%B5%D0%BD)
  4. [ЗАДАНИЯ: ПОИСК ОПТИМАЛЬНОГО РАЗДЕЛА](https://github.com/vinni-bio/WS-20160909#homework-questions-partition-analysis)
  5. [ЗАДАНИЯ: ПОСТРОЕНИЕ ДЕРЕВЬЕВ](https://github.com/vinni-bio/WS-20160909#homework-questions-likelihood-and-bayesian-methods)
* [ПРИЛОЖЕНИЕ](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%B1%D0%B0%D0%B7%D1%8B-%D0%B3%D0%B5%D0%BD%D0%B5%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85) БАЗЫ ГЕНЕТИЧЕСКИХ ДАННЫХ 
* [ПРИЛОЖЕНИЕ](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%B1%D0%B0%D0%B7%D1%8B-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-ncbi) БАЗЫ ДАННЫХ NCBI
* [ПРИЛОЖЕНИЕ](https://github.com/vinni-bio/SIRIUS-PHYLO#%D0%BF%D0%BE%D0%BB%D1%8F-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%BE%D0%B2-%D0%BF%D0%BE%D0%B8%D1%81%D0%BA%D0%B0-ncbi) ПОЛЯ ЗАПРОСОВ ПОИСКА NCBI

## ПРАКТИКА #1. ВЫРАВНИВАНИЕ ПОСЛЕДОВАТЕЛЬНОСТЕЙ

### НЕОБХОДИМЫЕ ПРОГРАММЫ
* Текстовый редактор [SUBLIME TEXT 3](https://www.sublimetext.com/3) ИЛИ [Notepad++](https://notepad-plus-plus.org/downloads/) (только Windows)
* [MEGA X](http://www.megasoftware.net/)
* [Sequence Matrix](http://gaurav.github.io/taxondna/)

### РЕГИСТРАЦИЯ В CIPRES
* портал [CIPRES: Cyberinfrastructure for Phylogenetic Research](https://www.phylo.org/)
* необходимо создать аккаунт и подтвердить его

### 1A. Проверьте количество записей в Генном банке по исследуемой группе (например, медведи):
1. Зайдите на страницу Генного банка `http://www.ncbi.nlm.nih.gov`
2. Найдите кнопку **All Resources**  в левом меню
3. В списке баз данных выберите **Nucleotide Database**
4. В поисковой строке введите запрос и нажмите кнопку поиска **SEARCH**:
`all[filter]`
5. В левом меню найдите фильтр **_Species_** и нажмите кнопку **customize**
6. Добавьте исследуемую группу (`Ursidae`) и нажмите кнопку **add**
7. Сколько записей относится к исследуемой группе?

### 1Б. Загрузите на свой компьютер записи исследуемой группы для анализа:
1. Зайдите снова в Генный банк (**Nucleotide Database**)
2. В поисковой строке введите запрос `"Yu L"[AUTH] AND Ursidae[ORGN] AND irbp[TITL]`
3. Сохраните последовательности в формате 'FASTA':<br/>
[irbp-ursidae.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp-ursidae.fasta)
4. В поисковой строке введите запрос `mitochondrion[filter] AND Ursidae[ORGN] AND "Talbot SL"[AUTH] AND 1140[SLEN]`
5. Сохраните последовательности в формате 'FASTA':<br/>
[cytb-ursidae.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb-ursidae.fasta)

### 1В. Выбор внешней группы
1. Откройте вкладку **Resources** в верхнем меню
2. Выберите **Sequence Analysis** и нажмите **_BLAST (Basic Local Alignment Search Tool)_**
3. Выберите <br/><img src="https://blast.ncbi.nlm.nih.gov/images/nucleutide-blast-cover.png" 
alt="Nucleotide BLAST" width="360" border="5" />
4. Введите номер NCBI для анализа последовательности вида *Ursus maritimus*:`AY303843.1`
5. Выберите базу данных **Nucleotide collection** и исключите медведей `Ursidae` из поиска
6. Нажмите <img src="https://blast.ncbi.nlm.nih.gov/images/blastButtonDown.jpg" 
alt="BLAST" width="360" border="5" />
7. Просмотрите результаты поиска и выберите наиболее подходящую последовательность со 100% покрытием:
`Panthera pardus` [AY525041.1](https://www.ncbi.nlm.nih.gov/nuccore/AY525041.1) (Леопард)
8. Сохраните внешнюю группу по гену *irbp* в отдельный файл в формате 'FASTA':<br/>
[irbp-outgroup.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp-outgroup.fasta)
9. Зайдите снова в Генный банк (**Nucleotide Database**)
10. В поисковой строке введите запрос <br/>`mitochondrion[filter] AND "Panthera pardus"[ORGN] AND "complete genome"[TITL]`
11. Выберите любой полный митохондриальный геном вида *Panthera pardus* (например, [KP001507.1](https://www.ncbi.nlm.nih.gov/nuccore/KP001507.1))
12. Выберите  **Change region shown** в правом меню и укажите координаты от `15000` до `16500`. Нажмите кнопку **update**.
13. Сохраните внешнюю группу по гену *cytb* в отдельный файл в формате 'FASTA':<br/>
[cytb-outgroup.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb-outgroup.fasta)

### 1Г. Выравнивание множественных последовательностей алгоритмом MUSCLE в MEGA
1. Запустите программу [MEGA X](http://www.megasoftware.net/)
2. Откройте меню **Data** и выберите **Open a File**, чтобы открыть файл [cytb-ursidae.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb-ursidae.fasta)
3. Выберите меню **Edit** и нажмите **Insert sequence from file**, чтобы вставить последовательность `cytb-outgroup.fasta`
4. Выберите все последовательности `Ctr+A` и нажмите на кнопку **MUSCLE** в верхнем меню
5. Нажмите посчитать **Compute**
6. Обрежте концы с пропусками
7. Откройте меню **Data** и выберите **Export alignment**, чтобы сохранить результаты:<br/>
[cytb.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb.fasta)
8. Повторите ту же самую процедуру для гена *irbp* :<br/>
[irbp.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.fasta)

### 1Д. Конвертация формата последовательностей и объединение последовательностей 
1. Запустите программу [Sequence Matrix](http://gaurav.github.io/taxondna/) program
2. Перетащите в окно программы файл [irbp.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.fasta) 
3. Выберите **Use species names**
4. Сохраните последовательности в формате NEXUS ("naked"):<br/>
[irbp.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.nex)
5. Сохраните последовательности в формате Phylip (RAxML)<br/>
[irbp.phy](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.phy)
6. Откройте меню **File** и выберите **Clear all sequences**
7. Перетащите в окно программы файл [cytb.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb.fasta) 
8. Выберите **Use species names**
9. Сохраните последовательности в формате NEXUS ("naked"):<br/>
[cytb.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb.nex)
9. Сохраните последовательности в формате Phylip (RAxML)<br/>
[cytb.phy](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb.phy)
10. Перетащите в окно программы файл [irbp.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.fasta) file to Sequence Matrix window
11. Сохраните последовательности в формате NEXUS ("naked"):<br/>
[bears.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/bears.nex)
12. Сохраните последовательности в формате Phylip (RAxML)<br/>
[bears.phy](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/bears.phy)

### 1E. Ознакомьтесь с функцией белка *irbp* в базе данных UniProt 
1. Зайдите на страницу http://www.uniprot.org/
2. В меню поиска, введите:<br/>
`name:"interphotoreceptor retinoid binding"`
3. В меню поиска, введите:<br/>
`name:"interphotoreceptor retinoid binding" AND taxonomy:"Ursidae"`

## ПРАКТИКА #2. ВЫБОР МОДЕЛИ И ПОСТРОЕНИЕ ФИЛОГЕНЕТИЧЕСКИХ ДЕРЕВЬЕВ

### НЕОБХОДИМЫЕ ПРОГРАММЫ
* [MEGA X](http://www.megasoftware.net/)
* [jModelTest v2.1.10](https://github.com/ddarriba/jmodeltest2/releases)
* [PartitionFinder v2.1.1](https://github.com/brettc/partitionfinder/releases/tag/v2.1.1)
* [MrBayes v.3.2.7](https://nbisweden.github.io/MrBayes/download.html)
* [FigTree v.1.4.4](https://github.com/rambaut/figtree/releases)

### РЕГИСТРАЦИЯ В CIPRES
* портал [CIPRES: Cyberinfrastructure for Phylogenetic Research](https://www.phylo.org/)
* необходимо создать аккаунт и подтвердить его

### 2А. Импорт объединенной матрицы с выравниванием в формат MEGA
1. Откройте [MEGA X](http://www.megasoftware.net/)
2. В верхнем меню **File** выберите **Convert file format to MEGA**
3. Укажите [bears.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/bears.nex)
4. Сохраните новый файл [bears.meg](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/bears.meg)
5. Выйдите из **MEGA _File Editor and Format Converter_**
6. Откройте меню **Data** и выберите **Open a File**, чтобы открыть [bears.meg](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/bears.meg)

### 2Б. Метод максимальной парсимонии (MP - Maximum Parsimony)
1. Откройте меню **Phylogeny** и выберите **Construct/Test Maximum Parsimony Tree**
2. Установите *100* репликаций в **bootstrap test** 
3. Установите *complete deletion* в **gaps**
4. Установите **SPR** в *tree search method*
5. Запустите анализ
6. После завершения укорените дерево, используя внешнюю группу
7. Сохраните дерево в формате png:<br/>
![Maximum Parsimony Tree](https://github.com/vinni-bio/WS-20160909/blob/master/LAB2/bears_parsimony.png)

#### ЗАДАНИЯ (МАКСИМАЛЬНАЯ ПАРСИМОНИЯ):
  * Как оригинальное дерево отличается от консенсусного бутстреп дерева?
  * Запустите MP анализ с большим числом бутстреп репликаций. Как изменились значения поддержки ветвей?
  * Запустите MP анализ, выбрав только 1ю и 2ю позиции в кодоне. Как изменились топология дерева и поддержка ветвей?
  * Запустите MP анализ, выбрав другие методы поиска деревьев. Как изменились топология дерева и поддержка ветвей?
  * Запустите MP анализ для каждого гена отдельно (используйте файлы *.fasta). Как различаются топологии деревьев и поддержки ветвей между генными деревьями?

### 2В. Метод ближайшего соседа (NJ - Neighbor-Joining) в MEGA
1. В верхнем меню **Phylogeny**  выберите **Construct/Test Neighbor-Joining Tree**
2. Установите **100** репликаций в **bootstrap test** 
3. Установите *complete deletion* в **gaps**
4. Установите *p-distance* в **model** 
5. Запустите анализ
6. После завершения укорените дерево, используя внешнюю группу
7. Сохраните дерево в формате png:<br/>
![NJ Tree](https://github.com/vinni-bio/WS-20160909/blob/master/LAB2/bears_distance.png)

#### ЗАДАНИЯ (ДИСТАНЦИОННЫЕ МЕТОДЫ):
  * Как оригинальное дерево отличается от консенсусного бутстреп дерева?
  * Запустите NJ анализ с большим числом бутстреп репликаций. Как изменились значения поддержки ветвей?
  * Запустите NJ анализ, выбрав только 1ю и 2ю позиции в кодоне. Как изменились топология дерева и поддержка ветвей?
  * Запустите MP анализ, выбрав другие модели нуклеотидных замен. Как изменились топология дерева и поддержка ветвей?
  * Как различаются топологии и поддержка ветвей между MP и NJ деревьями?
  * Повторите NJ анализ для каждого гена отдельно (используйте файлы *.fasta). Как различаются топологии деревьев и поддержки ветвей между генными деревьями?

### 2Г. Выбор модели нуклеотидных замен в jModelTest
1. Откройте программу [jModelTest.jar](https://github.com/ddarriba/jmodeltest2/releases)
2. Загрузите файл с выравниванием для гена *cytb*: [cytb.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb.nex)
3. В верхнем меню **Analysis**, выберите **_Compute Likelihood scores_**
4. Выберите поиск в 7 схемах нуклеотидных замен и запустите анализ
5. В верхнем меню **Analysis** выберите критерий **AIC**, **AICc**, **BIC** или **DT** (можно выбирать последовательно)
6. В верхнем меню **Results** выберите **_Show results table_**
7. Отсортируйте результаты по **AICc** критерию в соответствующей колонке
8. Выберите наиболее подходящую модель нуклеотидных замен по меньшему значению критерия
9. Проверьте параметры оптимальной модели нуклеотидных замен
10. ПОВТОРИТЕ всю процедуру для гена *irbp*: [irbp.nex](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp.nex)

#### ЗАДАНИЯ (ВЫБОР МОДЕЛИ НУКЛЕОТИДНЫХ ЗАМЕН):
  * Все ли критерии поддерживают одну и ту же модель нуклеотидных замен?
  * Если нет, то по каким параметрам различаются выбранные оптимальные модели?
  * Сравните оптимальную модель по критерию **AICc** со следующей за ней моделью. Как сильно различаются они по поддержке? Посмотрите на значение **delta**. По каким параметрам эти модели различаются?
  * Какую модель нуклеотидных замен вы выбрали для последующей реконструкции филогенетического дерева? Постарайтесь объяснить почему.
  * Как различаются выбранные модели нуклеотидных замен для генов *irbp* и *cytb*?

### 2Д. ПОИСК ОПТИМАЛЬНОГО РАЗДЕЛА В [PartitionFinder](https://github.com/brettc/partitionfinder/releases/tag/v2.1.1)
1. Откройте папку `partitionfinder-2.1.1/examples/nucleotide/` и скопируйте из нее файл `partition_finder.cfg` в вашу рабочую директорию
2. Откройте файл  `partition_finder.cfg` в текстовом редакторе (например, Notepad++ или SUBLIME)
3. Измените `test.phy` в `bears.phy` (ваш файл с выравниванием)
4. Измените секцию с разделами `[data_blocks]` на следующее:
<pre><code>    cytb_pos1 = 1-1140\3;
    cytb_pos2 = 2-1140\3;
    cytb_pos3 = 3-1140\3;
    irbp_pos1 = 1141-2420\3;
    irbp_pos2 = 1142-2420\3;
    irbp_pos3 = 1143-2420\3;</code></pre>
5. Сохраните файл `partition_finder.cfg`, не изменяя его название в папке с файлами выравнивания:<br/>
[partition_finder.cfg](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/partition_finder.cfg)
6. Откройте терминал (promt в Windows)
7. Напечатайте `python` и нажмите пробел
8. Перетащите в окно терминала файл `PartitionFinder.py` и нажмите пробел
9. Перетащите в окно терминала папку, где лежат файлы выравнивания и файл `partition_finder.cfg` [partition_finder.cfg](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/partition_finder.cfg). <br/>По итогу должно получиться что-то похожее на:<br/>
`python /Users/vinni/Desktop/PartitionFinder.py /Users/vinni/Desktop/LAB2/`
10. Нажмите **ENTER**
11. После завершения анализа у вас в директории появится новая папка **analysis**
12. Чтобы увидеть результаты анализа откройте файл [best_scheme.txt](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/best_scheme.txt)
13. Скопируйте и сохраните раздел RAxML в отдельный текстовый файл:<br/>
[partitions.txt](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB2/partitions.txt)

#### ЗАДАНИЯ (ПОИСК ОПТИМАЛЬНОГО РАЗДЕЛА):
  * Сколько оптимальных разделов было выбрано для исследуемой матрицы выравнивания?
  * Как соотносятся оптимальные модели нуклеотидных замен выбранных разделов с теми, что были выбраны для генов в jmodeltest?



## ПРИЛОЖЕНИЯ

### БАЗЫ ГЕНЕТИЧЕСКИХ ДАННЫХ
* [INSDC: International Nucleotide Sequence Database Collaboration](http://www.insdc.org/)
* [NCBI: National Center for Biotechnology Information](http://www.ncbi.nlm.nih.gov/)
* [EMBL: European Molecular Biology Laboratory](http://www.embl.org/)
* [DDBJ: DNA Data Bank of Japan](http://www.ddbj.nig.ac.jp/)
* [ENSEMBL](https://www.ensembl.org/index.html)
* [UCSC Genome Browser](http://hgdownload.soe.ucsc.edu/downloads.html)
* [FlyBase](http://flybase.org/)
* [WormBase](https://www.wormbase.org/)
* [SGD: Saccharomyces Genome Database](http://www.yeastgenome.org/)
* [RNA-Central](http://rnacentral.org/)
* [TAIR](https://www.arabidopsis.org/)
* [EcoCyc](http://ecocyc.org/)
* [HUMAN1000](https://www.internationalgenome.org/)
* [ENCODE](https://www.encodeproject.org/)
* [UniProt: Swiss-Prot & TrEMBL](https://www.uniprot.org/)
* [Virus Pathogen Resource](https://www.viprbrc.org/)


### БАЗЫ ДАННЫХ NCBI

|  NCBI | Описание |
| --------- | --------- |
| [`assembly`](https://www.ncbi.nlm.nih.gov/assembly) | Сборки | 
| [`biocollections`](https://www.ncbi.nlm.nih.gov/biocollections) | Музейные коллекции | 
| [`bioproject`](https://www.ncbi.nlm.nih.gov/bioproject) | Проекты | 
| [`biosample`](https://www.ncbi.nlm.nih.gov/biosample) | Биологические материалы | 
| [`biosystems`](https://www.ncbi.nlm.nih.gov/biosystems) | Биологические системы | 
| [`books`](https://www.ncbi.nlm.nih.gov/books) | Книги | 
| [`clinvar`](https://www.ncbi.nlm.nih.gov/clinvar) | Изменчивость генома человека | 
| [`gap`](https://www.ncbi.nlm.nih.gov/gap) | Генотип и фенотип | 
| [`dbvar`](https://www.ncbi.nlm.nih.gov/dbvar) | Структурная вариация | 
| [`gene`](https://www.ncbi.nlm.nih.gov/gene) | Гены | 
| [`genome`](https://www.ncbi.nlm.nih.gov/genome) | Геномы | 
| [`gds`](https://www.ncbi.nlm.nih.gov/gds) | Экспрессия генов | 
| [`geoprofiles`](https://www.ncbi.nlm.nih.gov/geoprofiles) | Индивидуальная экспрессия генов | 
| [`gtr`](https://www.ncbi.nlm.nih.gov/gtr) | Генетические тесты | 
| [`homologene`](https://www.ncbi.nlm.nih.gov/homologene) | Генные гомологи | 
| [`ipg`](https://www.ncbi.nlm.nih.gov/geoprofiles) | Идентичные белки | 
| [`medgen`](https://www.ncbi.nlm.nih.gov/medgen) | Медицинские данные |
| [`mesh`](https://www.ncbi.nlm.nih.gov/mesh) | Медицинские термины |
| [`ncbisearch`](https://www.ncbi.nlm.nih.gov/ncbisearch) | Сайт NCBI |
| [`nlmcatalog`](https://www.ncbi.nlm.nih.gov/nlmcatalog) | National Library of Medicine |
| [`nuccore`](https://www.ncbi.nlm.nih.gov/nuccore) | ГенБанк |
| [`omim`](https://www.ncbi.nlm.nih.gov/omim) | Банк генетических заболеваний |
| [`pmc`](https://www.ncbi.nlm.nih.gov/pmc) | Журналы PMC |
| [`popset`](https://www.ncbi.nlm.nih.gov/popset) | Популяционные данные |
| [`protein`](https://www.ncbi.nlm.nih.gov/protein) | Белки |
| [`proteinclusters`](https://www.ncbi.nlm.nih.gov/proteinclusters) | Белковые кластеры |
| [`pcassay`](https://www.ncbi.nlm.nih.gov/pcassay) | Активность веществ |
| [`pccompound`](https://www.ncbi.nlm.nih.gov/pccompound) | Химические соединения |
| [`pcsubstance`](https://www.ncbi.nlm.nih.gov/pcsubstance) | Химические вещества |
| [`pubmed`](https://www.ncbi.nlm.nih.gov/pubmed) | Онлайн библиотека |
| [`snp`](https://www.ncbi.nlm.nih.gov/snp) | Нуклеотидные полиморфизмы |
| [`sparcle`](https://www.ncbi.nlm.nih.gov/sparcle) | Функциональная структура белков |
| [`sra`](https://www.ncbi.nlm.nih.gov/sra) | Короткие последовательности |
| [`structure`](https://www.ncbi.nlm.nih.gov/structure) | Структура макромолекул |
| [`taxonomy`](https://www.ncbi.nlm.nih.gov/taxonomy) | Таксономия |
| [`toolkit`](https://www.ncbi.nlm.nih.gov/toolkit) | Программы |


### ПОЛЯ ЗАПРОСОВ ПОИСКА NCBI

| Имя Поля  | Аббревиатура | Функция | Базы NCBI |
| --------- | --------- | --------- | --------- | 
| `[Accession]` | `[ACCN]` | Идентификатор NCBI | Все |
| `[Affiliation]` | `[AFFL]` | Аффилиация | Все |
| `[All Fields]` | `[ALL]` | Все поля | Все |
| `[Author]` | `[AU]` / `[AUTH]` | Автор | Все |
| `[Author - First]` | `[FAUT]` | Имя автора | Все |
| `[Author - Last]` | `[LAUT]` | Фамилия автора | Все |
| `[Feature Key]` | `[FKEY]` | Характеристики | Nucleotide, Protein, GSS |
| `[Filter]`| `[FILT]` / `[SB]` | Фильтрация / Исключение | Все |
| `[Genome Project]`| `[GPRJ]` | Числовой идентификатор геномного проекта | Все |
| `[Issue]` | `[ISS]` | Номер журнала | Все |
| `[Journal]` | `[JOUR]` | Журнал | Все |
| `[Keyword]` | `[KYWD]` | Ключевое слово | Все |
| `[Language]` | `[LANG]` | Язык публикации | PubMed |
| `[Major Topic]` | `[MAJR]` | Основная тема | PubMed |
| `[MeSH Terms]` | `[MESH]` | MeSH термины | PubMed |
| `[Modification Date]` | `[MDAT]` | Дата последнего изменения | Все |
| `[Molecular Weight]` | `[MOLWT]` | Молекулярный вес | Protein |
| `[Organism]` | `[ORGN]` | Латинское или народное название организма | Все |
| `[Page Number]` | `[PAGE]` | Страница | Все |
| `[Primary Accession]` | `[PACC]` | Основной идентификатор | Все |
| `[Primary Organism]` | `[PORGN]` | Основной организм | Все |
| `[Properties]` | `[PROP]` | Свойства | Все |
| `[Protein Name]` | `[PROT]` | Название белка | Все |
| `[Publication Date]` | `[PDAT]` | Дата публикации | Все |
| `[Publication Type]` | `[PTYP]` | Тип публикации | PubMed |
| `[SeqID String]` | `[SQID]` | Идентификатор последовательности | Все |
| `[Sequence Length]` | `[SLEN]` | Длина последовательности | Все |
| `[Subheading]` | `[SUBH]` | Подзаголовок | PubMed |
| `[Substance Name]` | `[SUBS]` | Название вещества | Все |
| `[Text Word]` | `[WORD]` | Описание | Все |
| `[Title]` | `[TI]` / `[TITL]` | Заголовок | Все |
| `[Title/Abstract]` | `[TIAB]` | Заголовок/абстракт | PubMed |
| `[Volume]` | `[VOL]` | Том | Все |
| `[Unique identifier]` | `[UID]` | Уникальный номер записи | Все |



