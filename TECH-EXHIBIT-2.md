# Приложение № 2. Поддерживаемые форматы импорта данных

Система интеграции данных [Национальной цифровой (Электронной) библиотеки][NDL] (далее [СИД][13]) поддерживает следующие форматы импорта данных:

1. Данные соответствующие экосистеме [Linked Data]:
  
  В этой форме ожидается поставка данных о классификационных системах, словари, глоссарии, онтологии, фактологические и прочие виды связей между сущностями.
  
  * Форматы сериализации:
    1.1. [JSON-LD], [RFC8259]
    1.2. [N-Quads]
  * Автоматически интерпретируемые коды RDF namespaces:
    
    | Имя namespace | URI |
    | --- | --- | 
    | ore | [http://www.openarchives.org/ore/terms/](http://www.openarchives.org/ore/terms/) |
    | skos | [http://www.w3.org/2004/02/skos/core#](http://www.w3.org/2004/02/skos/core#) |
    | dc | [http://purl.org/dc/elements/1.1/](http://purl.org/dc/elements/1.1/) |
    | edm | [http://www.europeana.eu/schemas/edm/](http://www.europeana.eu/schemas/edm/) |
    | rdf | [http://www.w3.org/1999/02/22-rdf-syntax-ns#](http://www.w3.org/1999/02/22-rdf-syntax-ns#) |
    | dcterms | [http://purl.org/dc/terms/](http://purl.org/dc/terms/) |
    | foaf | [http://xmlns.com/foaf/0.1/](http://xmlns.com/foaf/0.1/) |
    | geo | [http://www.w3.org/2003/01/geo/wgs84_pos#](http://www.w3.org/2003/01/geo/wgs84_pos#) |
    | bbk | [http://lod.rsl.ru/bbkgsk/concepts/](http://lod.rsl.ru/bbkgsk/concepts/) |
    | bbk | [http://10.250.98.18:8080/fuseki/bbk#](http://10.250.98.18:8080/fuseki/bbk#) |
    | udc | [http://udcdata.info/](http://udcdata.info/) |

  * Ожидаемые онтологии:
    * [SKOS]
        Система будет учитывать следующие типы и аттрибуты:
        
        * [skos:ConceptScheme](https://www.w3.org/2009/08/skos-reference/skos.html#ConceptScheme)
        * [skos:Concept](https://www.w3.org/2009/08/skos-reference/skos.html#Concept)
            * Отношение к схеме:
                * [skos:inScheme](https://www.w3.org/2009/08/skos-reference/skos.html#inScheme)
            * Описание концепта:
                * [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) - в моноязычной или мультиязычной форме
                * [skos:altLabel](https://www.w3.org/2009/08/skos-reference/skos.html#altLabel) - в моноязычной или мультиязычной форме
                * [skos:definition](https://www.w3.org/2009/08/skos-reference/skos.html#definition) - в моноязычной или мультиязычной форме
                * [skos:example](https://www.w3.org/2009/08/skos-reference/skos.html#example) - в моноязычной или мультиязычной форме
                * [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) - в моноязычной или мультиязычной форме
            * Семантические связи:
                * [skos:hasTopConcept](https://www.w3.org/2009/08/skos-reference/skos.html#hasTopConcept)
                * [skos:topConceptOf](https://www.w3.org/2009/08/skos-reference/skos.html#topConceptOf)
                * [skos:broader](https://www.w3.org/2009/08/skos-reference/skos.html#broader)
                * [skos:broaderTransitive](https://www.w3.org/2009/08/skos-reference/skos.html#broaderTransitive)
                * [skos:narrower](https://www.w3.org/2009/08/skos-reference/skos.html#narrower)
                * [skos:narrowerTransitive](https://www.w3.org/2009/08/skos-reference/skos.html#narrowerTransitive)
                * [skos:related](https://www.w3.org/2009/08/skos-reference/skos.html#related)
                * [skos:relatedMatch](https://www.w3.org/2009/08/skos-reference/skos.html#relatedMatch)
    * [BIBFRAME 2]
        * Сущности:
            * [bf:Topic](http://id.loc.gov/ontologies/bibframe/Topic)
            * [bf:Classification](http://id.loc.gov/ontologies/bibframe/Classification)
            * [bf:Source](http://id.loc.gov/ontologies/bibframe/Classification)
            * [bf:classificationPortion](http://id.loc.gov/ontologies/bibframe/classificationPortion)
        * Отношения:
            * [bf:relatedTo](https://id.loc.gov/ontologies/bibframe.html#relatedTo)
            * [bf:hasPart](https://id.loc.gov/ontologies/bibframe.html#hasPart)
            * [bf:partOf](https://id.loc.gov/ontologies/bibframe.html#partOf)
            * [bf:dataSource](https://id.loc.gov/ontologies/bibframe.html#dataSource)
    * [Schema.org]

    * [WordNet] (глоссарий [WordNet Glossary]) для определения полисемических соответствий и семантических отношений:
        
      Список отношений, которые влияют на результат работы системы:
       
        | Прямое отношение | Обратное отношение |
        | --- | --- |
        | Antonym | Antonym |
        | Hyponym | Hypernym |
        | Hypernym | Hyponym |
        | Instance Hyponym | Instance Hypernym |
        | Instance Hypernym | Instance Hyponym |
        | Holonym | Meronym |
        | Meronym | Holonym |
        | Similar to | Similar to |
        | Attribute | Attribute |
        | Verb Group | Verb Group |
        | Derivationally Related | Derivationally Related |
        | Domain of synset | Member of Doman |
 
    * [IANA link relation codes] в соответствии с [RFC 8288]
2. Семейство стандартов описания и технических форматов MARC
  * Технические форматы: 
      * [ISO 2709:2008] (локальная адаптация: [ГОСТ 7.14-98 (ИСО 2709-96) СИБИД]). Формат для обмена информацией. Структура записи
      * [MARCXML]
  * Стандарты описания:
      * [MARC 21 Bibliographic]
      * [MARC 21 Authority]
      * [MARC 21 Holdings]
      * [RUSMARC bibliographic]
      * [UNIMARC bibliographic]
3. [ONIX for books]
  * [ONIX for books 3.0]
  * [ONIX for books 2.x] (частичная поддержка, не рекомендуется для использования)
  
4. [TSV] фиксированного формата.

    Поставляемые данные должны соответствовать одному из двух форматов:
    
    Концепты/Классы/Категории:
        ```tsv
|         kind | source |	| key | description.skos:prefLabel@ru |	time_source
|         skos:Concept | bbkgsk |	| Я23(4Бл) | Литература универсального содержания -- Справочные издания -- Страноведческие справочники. Путеводители. Адресные книги. Адрес-календари -- Отдельные зарубежные страны -- Европа -- Болгария |	2020-12-07T23:20:35.082Z
|         skos:Concept | bbkgsk |	| Я23(4Бл-2) | Литература универсального содержания -- Справочные издания -- Страноведческие справочники. Путеводители. Адресные книги. Адрес-календари -- Отдельные зарубежные страны -- Европа -- Болгария -- Города |	2020-12-07T23:20:35.082Z
        ```
        
    Связи и отношения как в пределах поставляемой классификационной системы, так и с другими объектами СИД
        ```tsv
|         kind_from | source_from |	| key_from | relation_kind |	| kind_to | source_to |	| key_to | time_source |
|         skos:Concept | bbkgsk |	| Я23(4Бл) | skos:narrower |	| skos:Concept | bbkgsk |	| Я23(4Бл-2) | 2020-12-07T23:20:35Z |
|         skos:Concept | bbkgsk |	| Я23(4Бл) | skos:relatedTp |	| bf:Instance | RuMoRGB |	| 008869301 | 2020-12-07T23:30:15Z |
        ```
    При подготовке материала следует учитывать перечисленные ниже особенности импорта СИД:
    
    * Система будет воспринимать последовательности символов ` -- `, `\t` и `|` как внутренние разделители и это будет отражаться на результатах авторубрикации
    
    * Метки времени должны имет формат [ГОСТ Р 7.0.64-2018] / [ISO 8601].
      
    * Желательно использовать нулевую временную зону `Z` в противном случае указывать временную зону в явном виде, используя синтаксис ISO 8601.
      
    * Можно использовать не-целочисленный квантификатор для секундв для указания количества милли- и микросекунд. 
    		
5. Цифровые документы в формате семейства [HTML]
    * [HTML 5]
    * [XHTML 1.1]
    * [hOCR 1.2]
    * [W3C Publication Manifest] разметка

6. [EPUB 3.X]

7. Оцифрованные материалы в формате [PDF/A Соответствие на уровне B ISO 19005-1:2005][ISO 19005-1:2005]
8. Оцифрованные материалы в формате [METS]
9. Текст с разметкой [reStructuredText]
10. Текст с разметкой [MarkDown]


11. `Обычный текстовй файл`, при формировании которого учтены следующие особенности импорта:
  
  * Кодировка: [ISO 10646]
  * Первая строка будет считаться заглавием
  * Символ `\n` будет считаться началом параграфа

Также для импорта возможны форматы локальных поставщиков:
12. [Yandex Market Language] компании [Yandex]

13. Платформа публикаций РАН [JES]



[NDL]: https://rusneb.ru (Национальная цифровая \(электронная\) библиотека \(НЭБ\))

[13]: https://catalog.rusneb.ru (Система интеграции данных НЭБ)

[ГОСТ Р 7.0.64-2018]: http://protect.gost.ru/document.aspx?control=7&id=230880 (ГОСТ Р 7.0.64-2018 \(ИСО 8601:2004\))
[ГОСТ Р 7.0.12-2011]: http://protect.gost.ru/document.aspx?control=7&id=17958 (ГОСТ Р 7.0.64-2018 \(ИСО 8601:2004\))
[ГОСТ 7.14-98]: http://docs.cntd.ru/document/1200004278 (ГОСТ 7.14-98 \(ИСО 2709-96\) СИБИД)
[ISO 8601]: https://www.iso.org/iso-8601-date-and-time-format.html (ISO 8601 - Date and Time Formats)
[ISO 19005-1:2005]: https://www.iso.org/obp/ui#iso:std:iso:19005:-1:ed-1:v1:ru (ISO 19005-1:2005 - PDF/A Соответствие на уровне B)
[ISO 10646]: https://home.unicode.org/ (ISO 10646 - UTF-8)
[ISO 2709:2008]: https://www.iso.org/standard/41319.html (ISO 2709:2008 - Information and documentation — Format for information exchange)
[RFC8288]: https://www.rfc-editor.org/info/rfc8288 (Nottingham, M., "Web Linking", RFC 8288, DOI 10.17487/RFC8288, October 2017)
[RFC8259]: https://tools.ietf.org/html/rfc8259 (RFC 8259 - JSON)
[RFC4329]: https://tools.ietf.org/html/rfc4329 (RFC 4329 - Scripting media types)
[RFC4809]: https://tools.ietf.org/html/rfc4329 (RFC 4809 - N. Freed; J. Klensin. Multipurpose Internet Mail Extensions \(MIME\) Part Four: Registration Procedures. December 2005. Best Current Practice.)

[HTML 5]: https://html.spec.whatwg.org/  (HTML 5)
[XHTML 1.1]: https://www.w3.org/TR/xhtml11/  (XHTML 1.1 - Module-based XHTML - Second Edition)
[hOCR 1.2]: http://kba.cloud/hocr-spec/1.2/ (hOCR версии 1.2)
[HTML]: https://www.w3.org/html/ (HTML)

[reStructuredText]: https://docutils.sourceforge.io/docs/ref/rst/restructuredtext.html (reStructuredText)
[EPUB 3.X]: https://www.w3.org/publishing/epub32/epub-spec.html (EPUB Версий 3.X)
[MarkDown]: https://daringfireball.net/projects/markdown/ (MarkDown)

[MARCXML]: http://www.loc.gov/standards/marcxml/ (MARCXML)
[MARC 21 Bibliographic]: https://www.loc.gov/marc/bibliographic/  (MARC 21 Bibliographic)
[MARC 21 Authority]: https://www.loc.gov/marc/authority/ (MARC 21 Authority)
[MARC 21 Holdings]: https://www.loc.gov/marc/holdings/ (MARC 21 Holdings)
[RUSMARC Bibliographic]: http://www.rusmarc.ru/ (RUSMARC)
[UNIMARC Bibliographic]: https://www.ifla.org/publications/unimarc-formats-and-related-documentation (UNIMARC)
[METS]: http://www.loc.gov/standards/mets/ (LoC METS XML 1.X)
[ONIX for books]: https://www.editeur.org/83/Overview/
[ONIX for books 3.0]: https://www.editeur.org/93/Release-3.0-Downloads/

[WordNet]: https://wordnet.princeton.edu/ (George A. Miller \(1995\). WordNet: A Lexical Database for English. Communications of the ACM Vol. 38, No. 11: 39-41. Christiane Fellbaum \(1998, ed.\) WordNet: An Electronic Lexical Database. Cambridge, MA: MIT Press.)
[WordNet Glossary]: https://wordnet.princeton.edu/documentation/wngloss7wn (глоссарий WordNet)


[TSV]: https://www.iana.org/assignments/media-types/text/tab-separated-values (Набор значений, разделенных символом табуляции \(IANA tab-separated-values\))
[JSON-LD]: https://www.w3.org/TR/json-ld11/ (JSON-LD 1.1 - A JSON-based Serialization for Linked Data)
[W3C Publication Manifest]: https://w3c.github.io/pub-manifest/ (W3C Publication Manifest draft 2020)
[N-Quads]: https://www.w3.org/TR/n-quads/ (RDF 1.1 N-Quads)

[Linked Data]: http://www.w3.org/DesignIssues/LinkedData.html (Linked Data)

[SKOS]: https://www.w3.org/TR/skos-reference/ (W3C SKOS - Simple Knowledge Organization System
Reference)
[BIBFRAME 2]: https://www.loc.gov/bibframe/ (Library of Congress BIBFRAME 2)
[Schema.org]: https://schema.org/ (Schema.org)
[IANA link relation codes]: https://www.iana.org/assignments/link-relations/link-relations.xhtml#link-relations-1 (IANA link relation codes()


[Yandex Market Language]: https://yandex.ru/support/partnermarket/export/yml.html (Yandex Market Language)
[Yandex]: https://yandex.ru/ (Yandex LLC)
[JES]: https://ras.jes.su/ (Формат метаданных платформы РАН JES \(Publishing LLC «I-PC»\))

