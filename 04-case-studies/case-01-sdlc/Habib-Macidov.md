# SDLC düzgün qurulmayanda nə baş verir?

**Tələbə:** Həbib Məcidov  
**Qrup:** A2325A  
**Tarix:** 30.10.2026

## Problem

Proqram təminatının inkişaf həyat dövrü (SDLC) düzgün qurulmayanda layihə ya gecikir, ya büdcədən çıxır, ya da hazır məhsulda təhlükəsizlik boşluqları ortaya çıxır. Çox vaxt isə bunların üçü birlikdə olur. Bu iş üçün dörd məqalə oxudum. Məqsədim bu problemlərin haradan başladığını, nəyə gətirib çıxardığını və müəlliflərin hansı həll yollarını təklif etdiyini anlamaq idi.

## 1. Medium məqalələri

### 1.1. Why Most Software Projects Fail Without Process

- **Link:** https://hardikgp.medium.com/why-most-software-projects-fail-without-process-d7a64310510a

**Qısa məzmun.** Müəllif deyir ki, layihələrin çoxu pis proqramçılara görə yox, işin düzgün təşkil olunmamasına görə uğursuz olur. Tələblər hələ tam aydın deyil, amma kod yazılmağa başlanır. Yeni ideyalar gəldikcə heç bir prioritet olmadan işə əlavə edilir. Kimin nəyə cavab verdiyi bəlli olmur, qəbul edilən qərarlar heç yerdə yazılmır. Test və release qaydası da zəif olur. Nəticədə son tarixlər keçir, funksiyalar istifadəçidə xarab olur, texniki borc yığılır və komanda yorulur.

Müəllif həll yolu kimi SDLC mərhələlərinə əməl etməyi təklif edir: tələblərin toplanması, dizayn, inkişaf, test, buraxılış və dəstək. Bundan başqa, tələbləri erkən yoxlamağı, arxitektura qərarlarını sənədləşdirməyi, testi sona saxlamamağı və CI/CD qurmağı məsləhət görür. Agile haqqında da maraqlı bir fikri var: Agile-ın da öz strukturu var, o, nizamsız işləmək demək deyil.

**Mənim nəticəm.** Bu məqalədən sonra başa düşdüm ki, problemlərin böyük hissəsi hələ kod yazılmamış, planlama və tələblər mərhələsində yaranır. Komandalarda tez-tez "proses bizi ləngidir" deyirlər, amma əslində tam tərsi olur. Səhvi sonradan düzəltmək həmişə daha çox vaxt və pul aparır.

### 1.2. Stop doing security the 'right' way

- **Link:** https://code4thought.medium.com/stop-doing-security-the-right-way-ee7db0136bbc

**Qısa məzmun.** Bu məqalə təhlükəsizlik haqqındadır. Müəllifin fikrincə, şirkətlərin çoxu təhlükəsizliyə hələ də köhnə waterfall üsulu ilə baxır, yəni onu SDLC-nin ən sonunda yoxlayır. Adətən release-dən əvvəl bir penetrasiya testi edirlər və bununla kifayətlənirlər. Problem ondadır ki, bu yoxlama həm gec gəlir, həm də hər şeyi görmür. Üçüncü tərəf kitabxanalarındakı boşluqlar, biznes məntiqindəki səhvlər və loqlama problemləri çox vaxt gözdən qaçır. Məqalədə yazılıb ki, təhlükəsizlik insidentlərinin 75%-dən çoxu proqramdakı səhvlərdən yaranır. Səbəb kimi bunlar göstərilir: proqramçılar OWASP Top 10 kimi riskləri yaxşı bilmir, internetdən kod yoxlamadan köçürülür, təhlükəsizlik komandası isə prosesə çox gec qoşulur.

Müəllif altı addım təklif edir. Proqramçılara təhlükəsiz kod yazmağı öyrətmək, dil və kitabxana seçimi üçün qaydalar qoymaq, kodu təmiz saxlamaq, OWASP ASVS kimi bir standarta əməl etmək, yoxlamaları SAST, SCA və DAST alətləri ilə avtomatlaşdırmaq və təhlükəsizlik mütəxəssislərini dizayn mərhələsindən işə cəlb etmək.

**Mənim nəticəm.** Əvvəllər təhlükəsizliyi sonda edilən ayrıca bir yoxlama kimi düşünürdüm. İndi görürəm ki, o, hər mərhələnin içində olmalıdır. Bir də maraqlı bir əlaqə gördüm: təhlükəsizliyi sona saxlamaq gecikməyə də səbəb olur. Boşluq gec tapılır, onu düzəltmək vaxt aparır, release təxirə düşür. Yəni bu iki problem bir-birindən ayrı deyil.

## 2. LinkedIn məqaləsi

### Managing Project Scope Creep

- **Link:** https://www.linkedin.com/pulse/managing-project-scope-creep-sarah-mccasland

**Qısa məzmun.** Müəllif yazır ki, proqram hazırlananda hər zaman "bir az da əlavə edək" istəyi yaranır: daha yaxşı performans, yeni funksiyalar, planda olmayan başqa şeylər. Backlog artıq hazır olandan sonra bunlar plansız əlavə edilsə, layihə həm büdcədən, həm də vaxtdan çıxır. Müəllifə görə bu istək iki tərəfdən gəlir. Birincisi, proqramçılar özləri ən yeni texnologiyaları sınamaq istəyir, amma bunu sprintin ortasında etmək QA komandasının işini çətinləşdirir. İkincisi, sifarişçi tərəf çox vaxt qəbul testi (UAT) zamanı yeni tələblər gətirir. Bəzən isə tələb dizayn mərhələsində sadəcə unudulmuş olur. Müəllifin fikrincə, layihə meneceri və product owner güclü olsa və bu müzakirələri düzgün idarə etsə, release tarixi pozulmaz.

**Mənim nəticəm.** Bu məqalə gecikmə və büdcə probleminin konkret bir səbəbini göstərir. Mənim üçün yeni olan o idi ki, scope creep təkcə müştəridən gəlmir, komandanın özündən də gəlir. Deməli, həll sadəcə müştəriyə "yox" demək deyil. Dəyişikliklər üçün aydın bir qayda lazımdır. Hər yeni istəyin vaxta və büdcəyə nə qədər təsir edəcəyinə əvvəlcə baxılmalı, yalnız ondan sonra qərar verilməlidir.

## 3. Fərqli mənbədən məqalə

### Software Projects Don't Have to Be Late, Costly, and Irrelevant

- **Link:** https://www.bcg.com/publications/2024/software-projects-dont-have-to-be-late-costly-and-irrelevant

**Qısa məzmun.** Bu məqalə o birilərdən fərqlənir, çünki şəxsi təcrübəyə yox, şirkət rəhbərləri arasında aparılan sorğuya əsaslanır. Sorğuda iştirak edənlərin təxminən yarısı deyib ki, onların şirkətində texnologiya layihələrinin 30%-dən çoxu ya gecikir, ya da büdcəni aşır. Hər beş nəfərdən biri isə layihələrin yarıdan çoxunun nəticəsindən razı olmadığını bildirib. Rəhbərlər əsas səbəb kimi bunları göstəriblər: biznes və texniki komandaların hədəfləri bir-birinə uyğun gəlmir, vaxt planları real deyil, pul və proqramçı çatışmır.

Məqalədə məni ən çox təəccübləndirən tapıntı bu oldu: sadəcə Agile istifadə etmək layihənin uğurlu olmasına təsir göstərməyib. Ən böyük fərqi texniki rəhbərlərin layihəyə lap əvvəldən, strategiya mərhələsindən qoşulması yaradıb. Belə layihələrin uğur ehtimalı 154% yüksək olub. Problemləri erkən görməyə imkan verən xəbərdarlıq sistemi olan komandalarda uğur 16 faiz bəndinə qədər artıb. Bütün vacib vəzifələri dolu olan komandalar isə boş yerləri olan komandalardan 76% daha yaxşı nəticə göstərib. Müəlliflərin tövsiyələri bunlardır: tələblərin araşdırılmasına vaxt limiti qoymaq, ilk versiyanı 3-4 ay ərzində çıxarıb sonra genişləndirmək, işi KPI-larla və erkən xəbərdarlıq göstəriciləri ilə izləmək.

**Mənim nəticəm.** Bu məqalə əvvəlki üç məqalədə deyilənləri rəqəmlərlə təsdiqləyir. Agile ilə bağlı nəticə məni təəccübləndirdi, çünki çox vaxt Agile-ı hər problemin həlli kimi təqdim edirlər. Görünür, metodologiyanın adı o qədər də vacib deyil. Əsas odur ki, biznes və texniki tərəf əvvəldən birlikdə işləsin və problemlər böyüməmiş görünsün.

## 4. Dörd məqalənin müqayisəsi

| | Medium 1 (hardikgp) | Medium 2 (code4thought) | LinkedIn (McCasland) | BCG |
| --- | --- | --- | --- | --- |
| Əsas mövzu | Ümumi iş prosesi | Təhlükəsizlik | Scope creep | Gecikmə və büdcə |
| Əsas səbəb | Struktur yoxdur, tələblər aydın deyil | Təhlükəsizlik sona saxlanılır | Plansız əlavə olunan tələblər | Biznes və IT arasında uyğunsuzluq, real olmayan plan |
| Nəticə | Gecikmə, texniki borc | Boşluqlar, maddi itki, nüfuz itkisi | Vaxt və büdcə aşımı | Layihələrin 30%-dən çoxu gecikir |
| Təklif olunan həll | SDLC mərhələləri, davamlı test, CI/CD | Shift left, OWASP, avtomatik yoxlama | Dəyişikliklərə nəzarət, güclü PM və PO | Erkən cəlb etmə, qısa ilk versiya, KPI |
| Nəyə əsaslanır | Müəllifin təcrübəsi | Təcrübə və standartlar | Müəllifin təcrübəsi | Sorğu nəticələri |

**Oxşarlıqlar.** Dörd məqalə də eyni nəticəyə gəlir: problem texnologiyada deyil, işin necə təşkil olunmasındadır. Hamısı səhvlərin layihənin əvvəlində, tələblər müəyyən edilərkən və planlama zamanı başladığını göstərir. Bir də hamısında belə bir fikir var: problem nə qədər gec aşkar olunursa, onu düzəltmək bir o qədər baha başa gəlir.

**Fərqlər.** Medium məqalələri və LinkedIn yazısı müəlliflərin öz təcrübəsinə əsaslanır, BCG-nin məqaləsi isə sorğu rəqəmlərinə. Code4thought əsasən təhlükəsizliyə baxır, digər üç məqalə isə daha çox vaxt və pul itkisindən danışır. LinkedIn məqaləsinin mövzusu ən dardır, yalnız scope creep haqqındadır, amma onu ən aydın izah edən də odur. Bir maraqlı məqam da var: BCG Agile-ın tək başına problemi həll etmədiyini deyir, birinci Medium məqaləsi də Agile-ın struktur tələb etdiyini yazır. Yəni fərqli mənbələr bu məsələdə eyni fikirdədir.

**Öz sözlərimlə yekun.** Bu araşdırmadan sonra belə qənaətə gəldim ki, gecikmə, büdcənin aşılması və təhlükəsizlik problemləri ayrı-ayrı problemlər deyil, hamısı eyni yerdən başlayır. O yer də budur: vacib qərarlar ya gec verilir, ya da ümumiyyətlə verilmir. Tələblər aydınlaşmamış kod yazılır, təhlükəsizlik sonraya saxlanılır, yeni istəklər düşünülmədən əlavə edilir, biznes tərəfi ilə texniki tərəf isə fərqli şeylər istəyir. Mənim fikrimcə bunun qarşısını almaq üçün üç şey xüsusilə vacibdir:

1. Layihənin əvvəlində tələbləri və hədəfi biznes və texniki komanda birlikdə müəyyən etməlidir.
2. Test və təhlükəsizlik yoxlamaları sona yox, hər mərhələyə daxil edilməli və mümkün qədər avtomatlaşdırılmalıdır.
3. Dəyişikliklərin necə qəbul olunacağına dair aydın qayda olmalı, layihənin vəziyyəti isə erkən xəbərdarlıq göstəriciləri ilə izlənilməlidir.

Waterfall, Agile və ya DevOps seçmək, məncə, ikinci dərəcəli məsələdir. Hansı model seçilsə də, ona ciddi əməl olunmasa, eyni problemlər yenə yaranacaq.

## 5. Əlavə video mənbələr

| Platforma | Video | Link | Hansı mövzuya aiddir |
| --- | --- | --- | --- |
| YouTube | Software Development Life Cycle: Explained (AltexSoft) | https://www.youtube.com/watch?v=SaCYkPD4_K0 | SDLC mərhələləri, Waterfall, Agile, DevOps (Medium 1) |
| YouTube | 10 Signs Your Software Project Is Heading For FAILURE (Dave Farley) | https://www.youtube.com/watch?v=-6KHhwEMtqs | Layihənin uğursuzluğa getdiyini göstərən əlamətlər (BCG, Medium 1) |
| TEDx | Vineeth Paleri: Demystifying Software Engineering (TEDxCUSAT) | https://www.ted.com/talks/vineeth_paleri_demystifying_software_engineering | Spesifikasiya və dizayna diqqət yetirilməməsi (Medium 1) |
| TEDx | Susanne Sommer, Helmut Wiland: Steering projects without long-term plans | https://www.ted.com/talks/susanne_sommer_helmut_wiland_steering_projects_without_long_term_plans_mission_impossible | Klassik planlamanın zəif tərəfləri və Agile (LinkedIn, BCG) |
| Vimeo | DevSecOps: Building Continuous Security Into IT & App Infrastructures | https://vimeo.com/237972697 | Təhlükəsizliyin DevOps prosesinə daxil edilməsi (Medium 2) |
| Vimeo | DevSecOps and AppSec – DevOps Unbound EP 2 | https://vimeo.com/451613420 | Tətbiq təhlükəsizliyi, OWASP (Medium 2) |
