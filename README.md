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