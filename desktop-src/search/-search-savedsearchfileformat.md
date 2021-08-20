---
description: Windows utenti possono salvare le ricerche come cartella di ricerca generata da un file XML che archivia la query in un modulo che può essere usato dal sottosistema di ricerca Windows ricerca.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Formato del file di ricerca salvato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863724"
---
# <a name="saved-search-file-format"></a>Formato del file di ricerca salvato

In Windows Vista e versioni successive gli utenti possono salvare le ricerche come cartella di ricerca generata da un file XML che archivia la query in un modulo che può essere usato dal sottosistema di ricerca Windows. Questo argomento descrive il formato di file ( \* .search-ms) e include le sezioni seguenti:

- [Panoramica delle ricerche salvate](#overview-of-saved-searches)
- [\<viewInfo> Elemento](/windows)
  - [\<viewInfo> Attributi](/windows)
  - [\<viewInfo> Elementi figlio](/windows)
- [\<query> Elemento](/windows)
  - [\<query> Elementi figlio](/windows)
- [\<properties> Elemento](/windows)
- [Specifica completa del formato di file search-ms](#full-specification-of-the-search-ms-file-format)
- [Esempi di ricerche salvate](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Panoramica delle ricerche salvate

Gli utenti possono salvare una query di ricerca come cartella di ricerca, una cartella virtuale visualizzata in Windows Explorer nella cartella Ricerche. L'apertura di una cartella di ricerca esegue la ricerca salvata e visualizza risultati aggiornati. Il file di ricerca salvato archivia la query in un formato Windows ricerca può agire, specificando cosa cercare, dove eseguire la ricerca e come presentare i risultati.

La ricerca salvata viene generata da un file XML ( \* .search-ms) nella cartella %userprofile% \\ Searches. I dati sono suddivisi in tre elementi principali nel file XML:

- \<viewInfo> specifica le informazioni di presentazione
- \<query> specifies (cerca informazioni sulle query)
- \<properties> specifica le proprietà del \* file con estensione search-ms stesso

L'esempio seguente illustra la struttura di alto livello di un file di ricerca salvato.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>\<viewInfo> Elemento

\<viewInfo>L'elemento specifica il modo in cui i risultati vengono presentati all'utente finale. Nell'esempio seguente viene illustrata la struttura dell'elemento .

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Attributi

La tabella seguente descrive gli attributi dell'elemento \<viewInfo>.

| Attributo     | Descrizione                                                                     | Valori                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| Viewmode      | Specifica la visualizzazione cartelle.                                                      | Riquadri \| delle icone \| dei dettagli  |
| iconSize      | Controlla le dimensioni predefinite delle icone e delle anteprime per gli elementi quando non sono sovrapposti. | Numero intero compreso tra 16 e 256 |
| stackIconSize | Solo per uso interno. Non usare.                                              | n/d                        |
| displayName   | Solo per uso interno. Non usare.                                              | n/d                        |
| autoListFlags | Solo per uso interno. Non usare.                                              | n/d                        |
| folderFlags   | Solo per uso interno. Non usare.                                              | n/d                        |
| taskFlags     | Solo per uso interno. Non usare.                                              | n/d                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Elementi figlio

Gli elementi figlio dell'elemento specificano quali colonne vengono visualizzate nei risultati della ricerca Windows Explorer e come vengono raggruppati \<viewInfo> e ordinati i risultati. Ogni elemento figlio contiene un set ordinato di colonne, identificate da nomi canonici delle proprietà di sistema, ad esempio System.DisplayName. Se non è definito nel file di ricerca salvato, i risultati della ricerca vengono presentati con un set predefinito di colonne appropriate per i tipi di file visualizzati.

| Elemento               | Descrizione                                                                                        | Valori                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| oggetti visibleColumns        | Specifica un elenco ordinato di colonne da visualizzare nella visualizzazione risultati. L'utente può modificare questo elenco. | Qualsiasi proprietà di sistema.                                         |
| frequentlyUsedColumns | Solo per uso interno. Non usare.                                                                 | n/d                                                          |
| columnChooserColumns  | Solo per uso interno. Non usare.                                                                 | n/d                                                          |
| Groupby               | Specifica una singola proprietà di sistema in base alla quale raggruppare i risultati. L'utente può modificare questo valore.  | Qualsiasi proprietà di sistema.                                         |
| sortList              | Specifica un elenco ordinato di colonne in base a cui ordinare i risultati.                                       | Fino a quattro proprietà di sistema. L'utente può modificare questo elenco. |
| stackList             | Solo per uso interno. Non usare.                                                                 | n/d                                                          |

## <a name="query-element"></a>\<query> Elemento

\<query>L'elemento specifica gli attributi che definiscono la modalità di esecuzione delle query sui risultati. Nell'esempio seguente viene illustrata la struttura dell'elemento .

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Elementi figlio

La tabella seguente descrive gli elementi figlio dell'elemento \<scope>.

| Elemento    | Descrizione                                                                                                               | Valore                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| provider  | Solo per uso interno. Non usare.                                                                                        | n/d                                                                                                                                                                                                                                                            |
| Sottoquery | Solo per uso interno. Non usare.                                                                                        | n/d                                                                                                                                                                                                                                                            |
| Ambito      | Identifica le posizioni da includere o escludere nella ricerca.                                                                 | Un percorso o un [ID di cartella](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) noto del percorso da includere o escludere. Questo elemento può anche specificare se la ricerca deve includere/escludere percorsi figlio (una ricerca superficiale o approfondita). |
| kindList   | Identifica il tipo di file da cercare.                                                                             | Qualsiasi valore System.Kind.                                                                                                                                                                                                                                         |
| condizioni | Specifica le regole per filtrare i risultati. Ad esempio, i risultati potrebbero essere limitati ai messaggi di posta elettronica inviati da o a una determinata persona. | andCondition, orCondition, notCondition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope> Elemento

\<scope>L'elemento identifica le posizioni da includere o escludere dalla ricerca. \<scope>L'elemento deve contenere almeno \<include> un elemento figlio presente e zero o più elementi \<exclude> . I percorsi possono essere specificati come percorso (le variabili di ambiente sono supportate) o come identificatore [di cartella noto.](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) Inoltre, ognuno di questi percorsi può essere specificato per la ricerca approfondita o superficiale impostando nonRecursive su "true" o "false" (il valore predefinito è ricorsivo). È possibile escludere parti dell'elenco di posizioni incluse specificando elementi exclude.

Di seguito è riportato un elemento che consente di eseguire la ricerca nella cartella speciale dei documenti, ma non nei relativi elementi figlio, nel volume "E:" e nei relativi elementi figlio, ma non nella \<scope> directory "E: windows" o in uno dei relativi elementi \\ figlio:

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>\<kindList> Elemento

Questi elementi definiscono l'unione del "tipo" di elementi che devono essere visualizzati nella libreria. I valori validi sono:

- calendario
- communication
- contact
- documento
- email
- feed
- folder
- Gioco
- messaggio istantaneo
- Gazzetta
- link
- Film
- music
- nota
- picture
- programma
- recordedtv
- searchfolder
- attività
- Video
- webhistory
- item
- altro

### <a name="conditions-element"></a>\<conditions> Elemento

Le condizioni sono filtri rispetto ai quali vengono confrontati i risultati della ricerca. Ad esempio, è possibile filtrare i risultati che soddisfano determinati criteri, ad esempio il nome dell'autore o le dimensioni del file. Il set di condizioni viene compilato in un singolo albero delle condizioni con rami LOGICI AND, OR e NOT.

Nell'esempio seguente viene illustrata la struttura \<condition> dell'elemento .

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

Il tipo di condizione può essere uno dei seguenti:

| Tipo          | Descrizione                                 | Attributi disponibili                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| andCondition  | Congiunzione di due o più condizioni figlio | n/d                                                |
| OrCondition   | Disgiunzione di due altre condizioni figlio | n/d                                                |
| notCondition  | Negazione di una condizione figlio               | n/d                                                |
| leafCondition | Confronta una proprietà con il valore                | property, propertyType, operator, value, valuetype |

Gli \<leafCondition> attributi dell'elemento identificano le proprietà e i valori in base ai quali vengono filtrati i risultati.

### <a name="example-conditions-element"></a>Esempio: \<conditions> Elemento

L'esempio seguente filtra i risultati per tutti gli elementi non letti creati da John. In altre informazioni, la proprietà System.IsRead è false e la stringa "john" viene visualizzata nelle proprietà System.Author o System.ItemAuthors.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>\<properties> Elemento

\<properties>L'elemento descrive le proprietà della ricerca salvata stessa. I file di ricerca salvati supportano quattro \<author> proprietà: \<kind> , , e \<description> \<tags> . Sono solo per uso interno.

## <a name="full-specification-of-the-search-ms-file-format"></a>Specifica completa del formato di file search-ms

Di seguito è riportato un esempio del codice XML completo per un file di ricerca salvato.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Esempi di ricerche salvate

Di seguito sono riportati esempi \* di file con estensione search-ms.

### <a name="recent-documentssearch-ms"></a>Recent Documents.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>File Musica.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Recently Shared by Me.search-ms

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
