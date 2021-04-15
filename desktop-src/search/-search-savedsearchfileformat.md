---
description: Gli utenti di Windows possono salvare le ricerche come una cartella di ricerca generata da un file XML che archivia la query in un modulo che può essere utilizzato dal sottosistema di ricerca di Windows.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Formato file di ricerca salvato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19cf936f78b045814bf7cba31a123c40d61927a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525495"
---
# <a name="saved-search-file-format"></a>Formato file di ricerca salvato

In Windows Vista e versioni successive, gli utenti possono salvare le ricerche come una cartella di ricerca generata da un file XML in cui è archiviata la query in un modulo che può essere utilizzato dal sottosistema di ricerca di Windows. In questo argomento viene descritto il formato di file ( \* . search-ms) e sono incluse le sezioni seguenti:

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

Gli utenti possono salvare una query di ricerca come cartella di ricerca, una cartella virtuale visualizzata in Esplora risorse sotto la cartella ricerche. Aprendo una cartella di ricerca viene eseguita la ricerca salvata e vengono visualizzati i risultati aggiornati. Il file di ricerca salvato archivia la query in un formato in cui Windows Search può agire, specificando gli elementi da cercare, dove eseguire la ricerca e come presentare i risultati.

La ricerca salvata viene generata da un file XML ( \* con estensione search-ms) nella cartella% UserProfile% search \\ . I dati sono divisi in tre elementi primari nel file XML:

- \<viewInfo> Specifica le informazioni di presentazione
- \<query> specifica (Cerca informazioni sulle query
- \<properties> Specifica le proprietà del \* file con estensione search-ms.

Nell'esempio seguente viene illustrata la struttura di alto livello di un file di ricerca salvato.

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

L' \<viewInfo> elemento specifica il modo in cui i risultati vengono presentati all'utente finale. Nell'esempio seguente viene illustrata la struttura dell'elemento.

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
| viewMode      | Specifica la visualizzazione cartelle.                                                      | \|Riquadri icone Dettagli \|  |
| iconSize      | Controlla le dimensioni predefinite delle icone e delle anteprime per gli elementi quando non lo stack. | Intero compreso tra 16 e 256 |
| stackIconSize | Solo per uso interno. Non usare.                                              | n/d                        |
| displayName   | Solo per uso interno. Non usare.                                              | n/d                        |
| autoListFlags | Solo per uso interno. Non usare.                                              | n/d                        |
| folderFlags   | Solo per uso interno. Non usare.                                              | n/d                        |
| taskFlags     | Solo per uso interno. Non usare.                                              | n/d                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Elementi figlio

Gli elementi figlio dell' \<viewInfo> elemento specificano le colonne visualizzate nei risultati della ricerca in Esplora risorse e il modo in cui i risultati vengono raggruppati e ordinati. Ogni elemento figlio contiene un set ordinato di colonne, identificato dai nomi canonici delle proprietà di sistema, ad esempio System. DisplayName. Se non è definito nel file di ricerca salvato, i risultati della ricerca vengono presentati con un set predefinito di colonne appropriato per i tipi di file visualizzati.

| Elemento               | Descrizione                                                                                        | Valori                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | Specifica un elenco ordinato di colonne da visualizzare nella visualizzazione dei risultati. L'utente può modificare l'elenco. | Qualsiasi proprietà di sistema.                                         |
| frequentlyUsedColumns | Solo per uso interno. Non usare.                                                                 | n/d                                                          |
| columnChooserColumns  | Solo per uso interno. Non usare.                                                                 | n/d                                                          |
| groupBy               | Specifica una singola proprietà di sistema in base alla quale raggruppare i risultati. L'utente può modificare questo valore.  | Qualsiasi proprietà di sistema.                                         |
| sortList              | Specifica un elenco ordinato di colonne per ordinare i risultati in base a.                                       | Fino a quattro proprietà di sistema. L'utente può modificare l'elenco. |
| stackList             | Solo per uso interno. Non usare.                                                                 | n/d                                                          |

## <a name="query-element"></a>\<query> Elemento

L' \<query> elemento specifica gli attributi che definiscono il modo in cui vengono eseguite le query sui risultati. Nell'esempio seguente viene illustrata la struttura dell'elemento.

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
| Ambito      | Identifica le posizioni da includere o escludere nella ricerca.                                                                 | Un percorso o un [ID di cartella noto](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) della posizione da includere o escludere. Questo elemento consente inoltre di specificare se la ricerca deve includere/escludere percorsi figlio (ricerca superficiale o approfondita). |
| tipo di   | Identifica il tipo di file da cercare.                                                                             | Qualsiasi valore System. Kind.                                                                                                                                                                                                                                         |
| condizioni | Specifica le regole per filtrare i risultati. Ad esempio, i risultati potrebbero essere limitati ai messaggi di posta elettronica inviati da o a una determinata persona. | andCondition, orCondition, notCondition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope> Elemento

L' \<scope> elemento identifica i percorsi da includere o escludere dalla ricerca. L' \<scope> elemento deve contenere almeno un \<include> elemento figlio presente e zero o più \<exclude> elementi. I percorsi possono essere specificati come un percorso (le variabili di ambiente sono supportati) o come un [identificatore di cartella noto](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid). Inoltre, è possibile specificare ognuno di questi percorsi per eseguire una ricerca approfondita o superficiale impostando l'oggetto non ricorsivo su "true" o "false" (il valore predefinito è ricorsivo). Le parti dell'elenco di percorsi incluso possono essere escluse specificando gli elementi exclude.

Di seguito viene illustrato un \<scope> elemento che eseguirà la ricerca nella cartella speciale documenti, ma non nei relativi elementi figlio, nel volume "e:" e nei relativi elementi figlio, ma non nella directory "e: \\ Windows" o in uno dei relativi elementi figlio:

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

Questi elementi definiscono l'Unione del "tipo" di elementi che devono essere visualizzati nella libreria. I valori validi sono:

- calendario
- communication
- contact
- documento
- email
- feed
- folder
- gioco
- instantmessage
- Journal
- link
- film
- music
- nota
- picture
- programma
- recordedtv
- SearchFolder
- attività
- Video
- cronologia webhistory
- item
- altro

### <a name="conditions-element"></a>\<conditions> Elemento

Le condizioni sono filtri in base ai quali vengono confrontati i risultati della ricerca. Ad esempio, è possibile filtrare i risultati che soddisfano determinati criteri, come il nome dell'autore o le dimensioni del file. Il set di condizioni è incorporato in un singolo albero di condizione con rami AND, OR e NOT logici.

Nell'esempio seguente viene illustrata la struttura dell' \<condition> elemento.

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
| andCondition  | Combinazione di due o più condizioni figlio | n/d                                                |
| orCondition   | Disgiunzione di due di più condizioni figlio | n/d                                                |
| notCondition  | Negazione di una condizione figlio               | n/d                                                |
| leafCondition | Confronta una proprietà con value                | Proprietà, propertyType, operatore, valore, ValueType |

Gli \<leafCondition> attributi dell'elemento identificano le proprietà e i valori con i quali vengono filtrati i risultati.

### <a name="example-conditions-element"></a>Esempio: \<conditions> element

Nell'esempio seguente vengono filtrati i risultati per tutti gli elementi non letti creati da John. Ovvero la proprietà System. IsAuthorized è false e la stringa "John" viene visualizzata nelle proprietà System. Author o System. ItemAuthors.

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

L' \<properties> elemento descrive le proprietà della ricerca salvata. I file di ricerca salvati supportano quattro proprietà: \<author> , \<kind> , \<description> e \<tags> . Sono solo per uso interno.

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

Di seguito sono riportati alcuni esempi di \* file con estensione search-ms.

### <a name="recent-documentssearch-ms"></a>Documenti recenti. search-ms

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

### <a name="recent-musicsearch-ms"></a>Music recenti. search-ms

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

### <a name="recently-shared-by-mesearch-ms"></a>Condiviso recentemente da me. search-ms

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
