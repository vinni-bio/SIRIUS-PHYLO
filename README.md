# ОСНОВЫ ВЫЧИСЛИТЕЛЬНОЙ БИОЛОГИИ И БИОИНФОРМАТИКИ (10-22 марта 2022)

## ПРАКТИКА #1. ФИЛОГЕНОМИКА: ВЫРАВНИВАНИЕ ПОСЛЕДОВАТЕЛЬНОСТЕЙ

### НЕОБХОДИМЫЕ ПРОГРАММЫ
* Текстовый редактор [SUBLIME TEXT 3](https://www.sublimetext.com/3) ИЛИ [Notepad++](https://notepad-plus-plus.org/downloads/) (только Windows)
* [MEGA X](http://www.megasoftware.net/)
* [Sequence Matrix](http://gaurav.github.io/taxondna/)

### РЕГИСТРАЦИЯ В CIPRES
* портал [CIPRES: Cyberinfrastructure for Phylogenetic Research](https://www.phylo.org/)
* необходимо создать аккаунт и подтвердить его

### A. Проверьте количество записей в Генном банке по исследуемой группе (например, медведи):
1. Зайдите на страницу Генного банка `http://www.ncbi.nlm.nih.gov`
2. Найдите кнопку **All Resources**  в левом меню
3. В списке баз данных выберите **Nucleotide Database**
4. В поисковой строке введите запрос и нажмите кнопку поиска **SEARCH**:
`all[filter]`
5. В левом меню найдите фильтр **_Species_** и нажмите кнопку **customize**
6. Добавьте исследуемую группу (`Ursidae`) и нажмите кнопку **add**
7. Сколько записей относится к исследуемой группе?

### Б. Загрузите на свой компьютер записи исследуемой группы для анализа:
1. Зайдите снова в Генный банк (**Nucleotide Database**)
2. В поисковой строке введите запрос `"Yu L"[AUTH] AND Ursidae[ORGN] AND irbp[TITL]`
3. Сохраните последовательности в формате 'FASTA':<br/>
[irbp-ursidae.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/irbp-ursidae.fasta)
4. В поисковой строке введите запрос `mitochondrion[filter] AND Ursidae[ORGN] AND "Talbot SL"[AUTH] AND 1140[SLEN]`
5. Сохраните последовательности в формате 'FASTA':<br/>
[cytb-ursidae.fasta](https://raw.githubusercontent.com/vinni-bio/WS-20160909/master/LAB1/cytb-ursidae.fasta)

### В. Выбор внешней группы
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

### Г. Выравнивание множественных последовательностей алгоритмом MUSCLE в MEGA
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

### Д. Конвертация формата последовательностей и объединение последовательностей 
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

### E. Ознакомьтесь с функцией белка *irbp* в базе данных UniProt 
1. Зайдите на страницу http://www.uniprot.org/
2. В меню поиска, введите:<br/>
`name:"interphotoreceptor retinoid binding"`
3. В меню поиска, введите:<br/>
`name:"interphotoreceptor retinoid binding” AND taxonomy:”Ursidae”`


## ПРИЛОЖЕНИЕ
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


### ПОЛЯ ЗАПРОСОВ NCBI

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


