---
description: Questo argomento presenta il linguaggio di query dei metadati per Windows Imaging Component (WIC).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Panoramica del linguaggio di query sui metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c69effefd288f13c72239a41c5ace1a518775337cc496a2defa864d179cd6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668234"
---
# <a name="metadata-query-language-overview"></a>Panoramica del linguaggio di query sui metadati

Questo argomento presenta il linguaggio di query dei metadati per Windows Imaging Component (WIC). Usare il linguaggio di query dei metadati per creare espressioni che trovano dati specifici (elementi di metadati) e posizioni (blocchi di metadati) all'interno dei metadati di un'immagine.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Anatomia di un'espressione di percorso](#anatomy-of-a-path-expression)
    -   [Selezione blocco](#block-selection)
    -   [Selezione dell'elemento](#item-selection)
    -   [Carattere di escape](#escape-character)
    -   [Espressioni di esempio](#sample-expressions)
-   [Espressioni dei criteri dei metadati delle foto](#photo-metadata-policy-expressions)
-   [Riepilogo del linguaggio di query sui metadati](#metadata-query-language-summary)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati [WIC,](-wic-about-metadata.md) come descritto in Panoramica dei metadati WIC e accesso ai metadati, come descritto in [Panoramica](-wic-codec-readingwritingmetadata.md)della lettura e della scrittura di metadati immagine .

## <a name="introduction"></a>Introduzione

Si interagisce con la piattaforma di metadati principalmente tramite due componenti Component Object Model (COM): un lettore di query, rappresentato [**dall'interfaccia IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e un writer di query, rappresentato dall'interfaccia [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Questi componenti consentono di leggere o scrivere metadati usando il linguaggio di query dei metadati. Il linguaggio di query descrive la sintassi di un'espressione di percorso e i componenti di query usano questa espressione di percorso per accedere ai metadati desiderati. Questa espressione di percorso descrive la posizione di un blocco o di un elemento di metadati.

Un blocco di metadati è un gruppo denominato di metadati in un formato specifico. Un blocco di metadati può contenere singoli elementi di metadati, ad esempio un autore o un'ora di creazione e blocchi di metadati aggiuntivi. Il nome di un blocco di metadati è determinato dal formato. Ad esempio, un blocco di metadati contenente i metadati app1 sarà denominato "app1". I formati di metadati comuni includono App1, Exif, IFD e XMP.

Un elemento di metadati è una coppia nome/valore che descrive caratteristiche come autore, titolo e classificazione.

Un'espressione di percorso contiene uno o più nomi di blocchi di metadati. Può anche specificare un elemento di metadati all'interno di un blocco di metadati. L'espressione di percorso seguente rappresenta un blocco App1 che contiene un blocco IFD che contiene l'elemento di metadati:

-   /app1/ifd/{ushort=18249}

Il diagramma seguente illustra la struttura di un'immagine JPEG di esempio con quattro blocchi di metadati radice: App0, App1, XMP e un blocco sconosciuto. Ogni elemento evidenziato annota il tipo di metadati (blocco o elemento) e l'espressione di query usata per recuperare i dati.

![Immagine jpeg con callout di metadati](graphics/jpegwithcallouts.png)

> [!Note]  
> Il contenuto di questo diagramma viene fatto riferimento in tutto il documento e viene usato in molti esempi.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomia di un'espressione di percorso

Per accedere ai metadati usando le API WIC, nella maggior parte dei casi è necessario usare un'espressione di query completa. Questo argomento illustra le espressioni completamente qualificate per l'accesso ai metadati. Se sono necessarie informazioni sui casi in cui vengono usate espressioni non completamente qualificate, vedere la sezione Espressione criteri metadati foto più avanti in questo documento.

Che cos'è un'espressione di query completa? In WIC un'espressione completa è una stringa che inizia con la barra del carattere di percorso (/), seguita da un percorso di navigazione a un blocco di metadati o a un elemento di metadati specifico. Ogni passaggio all'interno del percorso di navigazione è separato da una barra, formando un'espressione per accedere a un blocco di metadati o a un elemento di metadati. Ad esempio, di seguito è riportata un'espressione di query completa che accede a Microsoft Photo Rating in un blocco IFD annidato in un blocco App1:

-   /app1/ifd/{ushort=18249}

Quando WIC analizza questa espressione, cerca innanzitutto il blocco di metadati App1 all'interno dei metadati dell'immagine. Se viene trovato il blocco App1, continua la ricerca del blocco di metadati IFD annidato. Se viene trovato il blocco IFD, cerca l'elemento di metadati specifico, in questo caso la classificazione MicrosoftPhoto sotto il tag 18249, all'interno del blocco di metadati IFD. Se in qualsiasi momento WIC non trova un blocco di metadati o un elemento, interrompe la query.

### <a name="block-selection"></a>Selezione blocco

L'espressione di query dei metadati WIC più semplice è un'espressione per ottenere un lettore/writer di query per un blocco di metadati specifico. L'ottenimento di un lettore/writer di query consente di indirizzare le query successive direttamente a un blocco di metadati annidato senza gestire il relativo blocco padre. Un'espressione di query di selezione del blocco è un percorso di navigazione al blocco di metadati desiderato. Ad esempio, nella figura precedente sono presenti cinque blocchi di metadati, due dei quali sono annidati in altri blocchi di metadati. Di seguito sono riportate le espressioni di percorso per ogni blocco di metadati nell'esempio JPEG:

-   /app0
-   /app1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Quando si usa un lettore/writer di query per eseguire una query, restituisce un nuovo lettore/writer di query che esegue query nell'ambito del blocco di metadati specificato. Ad esempio, se si esegue la query "/app1", viene ottenuto un nuovo lettore di query e le query al nuovo lettore sono relative al blocco App1. Ciò significa che la query "/ifd" è valida per il nuovo lettore perché il blocco App1 contiene un blocco IFD. Tuttavia, "/xmp" non funziona perché questo blocco App1 non contiene un blocco di metadati XMP.

Il linguaggio di query supporta anche una notazione di indice. La notazione dell'indice fornisce l'accesso a un blocco di metadati specifico quando esistono più blocchi dello stesso tipo. Per l'esempio JPEG, è possibile usare l'espressione di percorso indicizzato seguente:

-   /\[0 \] \[ app1/0 \] ifd

Nel linguaggio di query tutti gli indici iniziano da zero. Nell'espressione precedente il primo zero esegue query per il primo blocco App1 e il secondo zero esegue una query sul primo blocco IFD annidato. La notazione dell'indice può comunque essere usata anche quando non esistono più blocchi dello stesso tipo. Se l'esempio JPEG includesse un secondo blocco App1 con un blocco IFD incorporato, l'espressione "/ \[ 1 app1/ifd" verrebbe usata per accedere al secondo \] blocco App1.

La notazione dell'indice diventa più comune quando si gestiscono blocchi TEXt PNG perché è probabile che l'immagine PNG abbia più di un blocco tEXt.

> [!Note]  
> Gli indici di matrici multidimensionali non sono supportati.

 

### <a name="item-selection"></a>Selezione dell'elemento

È possibile accedere agli elementi di metadati in un blocco di metadati compilando le espressioni di selezione del blocco. Si considerino le proprietà di classificazione XMP e Microsoft Photo nell'esempio JPEG. Questi metadati sono presenti in due blocchi di metadati: i blocchi App1/IFD e XMP. Pertanto, è possibile usare più di un'espressione per accedere agli stessi dati. L'espressione seguente accede alla classificazione MicrosoftPhoto nel blocco XMP:

-   /xmp/xmp:Rating

La parte "xmp:" dell'espressione è un identificatore descrittivo dello schema. XMP è uno standard estendibile e consente alle entità di terze parti di pubblicare i propri schemi che definiscono come archiviare determinati elementi di metadati. Uno schema XMP è completamente identificato da un URL, ma WIC fornisce un set di identificatori descrittivi per schemi noti. Per altre informazioni, vedere [l'argomento Query sui metadati del formato immagine](-wic-native-image-format-metadata-queries.md) nativa.

Per le immagini JPEG, le informazioni sulla classificazione possono essere archiviate anche all'interno del blocco IFD annidato app1. Tuttavia, a differenza dell'esempio di classificazione XMP, il blocco IFD non usa un nome di schema per accedere alle informazioni sulla classificazione. Si usa invece un'espressione dati. L'espressione seguente viene usata per accedere alla classificazione MicrosoftPhoto nel blocco IFD annidato App1:

-   /app1/ifd/{ushort=18249}

In questa espressione, la parte "/app1/ifd" dell'espressione è il percorso di navigazione del blocco IFD (come descritto in precedenza nella sezione Selezione blocco). La seconda parte dell'espressione "/{ushort=18249}" accede ai dati. Questa parte dell'espressione indica al parser di query di trovare i dati incorporati nel tag short senza segno con l'identificatore di tag 18249.

> [!Note]  
> Per un elenco dei formati di metadati comuni supportati da ogni formato di immagine, vedere l'argomento Query sui metadati del formato [immagine](-wic-native-image-format-metadata-queries.md) nativa.

 

{ushort=18249} è un'espressione dati e può assumere diverse forme. Un'espressione dati è un'espressione in due parti contenente il tag o la chiave dei metadati richiesti, in questo caso "18249" e il tipo di dati della chiave, in questo caso "ushort". Le due parti sono separate da un segno di uguale (=). WICsporta la maggior parte dei tipi di dati C/C++ comuni. Il linguaggio di query accetta i tipi di dati seguenti:

-   char
-   uchar
-   short
-   ushort
-   long
-   ulong
-   int
-   uint
-   longlong
-   float
-   double
-   str
-   wstr
-   guid
-   bool

> [!Note]  
> Questo elenco specifica solo i tipi di dati supportati dal linguaggio di query dei metadati. Usare questi tipi di dati durante la creazione di un'espressione di dati di query dei metadati, ad esempio {ushort=18249}. WiC restituisce il valore dell'elemento di metadati sotto forma di PROPVARIANT, che definisce il proprio sistema di tipi.

 

"18249" nell'esempio è il tag data. Questo particolare numero è definito da Microsoft per contenere la classificazione MicrosoftPhoto. Il tag dei dati può essere qualsiasi numero, stringa o GUID a seconda dell'elemento di dati che si sta cercando

A differenza dell'esempio XMP Rating, non è presente alcun conflitto di nomi per il valore di classificazione nel blocco App1/IFD. Questo perché il valore di classificazione XMP viene effettivamente archiviato in un tag ushort diverso, 18246. Di conseguenza, l'espressione per accedere alla classificazione XMP nel blocco App1/IFD è:

-   /app1/ifd/{ushort=18246}

> [!Note]  
> Per una descrizione formale del linguaggio di query dei metadati, vedere la sezione Riepilogo del linguaggio di query sui metadati più avanti in questo documento.

 

### <a name="escape-character"></a>Carattere escape

Il linguaggio di query non fa distinzione tra maiuscole e minuscole e considera tutti i caratteri come caratteri minuscoli. Alcuni formati di metadati, ad esempio XMP, tuttavia, fa distinzione tra maiuscole e minuscole. Quando si usa un formato di metadati con distinzione tra maiuscole e minuscole, usare la barra rovesciata ( ) quando si vuole specificare un \\ carattere maiuscolo.

Il carattere di escape viene utilizzato dal parser del linguaggio e il carattere seguente che lo segue viene interpretato direttamente. Ad esempio, l'espressione {char= } viene risolta come \\ \\ ' \\ 'e {char= C} viene risolta come C \\ maiuscola. Senza il carattere di escape, {char= } sarebbe un'espressione non valida e {char=C} verrebbe interpretato come un \\ carattere c minuscolo. Assicurarsi di usare il carattere di escape barra rovesciata prima di tutte le lettere maiuscole nei formati di metadati con distinzione tra maiuscole e minuscole.

### <a name="sample-expressions"></a>Espressioni di esempio

Nella tabella seguente vengono fornite alcune espressioni di esempio e descrizioni delle relative interpretazioni da parte del parser del linguaggio di query. 

| Expression                     | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ifd/xmp/exif:Author            | Corrisponde al percorso di navigazione seguente: IFD block -> XMP block -> "Author" nello schema "Exif".                                                                                                                                                                                                                                            |
| /\[1 \] ifd/ \[ 0 \] xmp/exif:Author | Uguale al primo elemento in questa tabella, ad eccezione del fatto che il prefisso descrive l'elemento da esplorare \[ \# \] in caso di conflitto di nomi.                                                                                                                                                                                                                                |
| /ifd/{ushort=700}/Author       | Uguale al primo elemento di questa tabella, ad eccezione del fatto che usa un'espressione dati per fare riferimento al blocco XMP anziché al nome di blocco "xmp" (il blocco XMP è incorporato nell'identificatore di tag breve senza segno 700). Inoltre, la proprietà "Author" non specifica uno schema. Il parser di query tenterà di trovare la corrispondenza con la proprietà in tutti gli schemi e restituirà la prima corrispondenza. |
| /ifd/xmp                       | Fornisce un percorso di navigazione a un blocco di metadati. Se il blocco viene trovato, viene restituito un nuovo reader/writer di metadati.                                                                                                                                                                                                                                                 |
| /\[\*\]tEXt/Keyword            | Ottiene o imposta la proprietà Keyword per un blocco PNG. Poiché la specifica dei metadati PNG consente più blocchi di un determinato tipo, la \[ \* notazione ottiene/imposta il blocco PNG di dati \] con la proprietà appropriata. In base alla specifica PNG, due blocchi non possono avere le stesse proprietà.                                                                |



 

Ogni blocco di metadati viene inoltre identificato in modo univoco dal GUID dei metadati che può essere usato al posto del nome descrittivo del blocco. È possibile usare la sintassi seguente al posto dei nomi dei blocchi: "/{guid=GUID}/ \[ n \] {guid=GUID}/schema:tagidentifier"

La tabella seguente fornisce alcuni esempi non validi e i motivi per cui verrebbero rifiutati. 

| Espressione non valida         | Descrizione del rifiuto                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /ifd/ \[ 0 \] \[ 2 \] exif/       | Rifiutato perché gli indici di matrici multidimensionali non sono supportati.                                                                                                    |
| /ifd/{ushort=1}/{ushort=2} | Rifiutato a meno che l'IFD non abbia un tagID=1, ovvero un gestore di metadati che contiene un elemento di metadati con tagID=2.                                                        |
| /{ushort=1}                | Rifiutato se l'elaborazione della query è relativa a un livello superiore della gerarchia dei metadati. Ciò è dovuto al fatto che il livello superiore contiene solo blocchi di metadati e non elementi di dati. |



 

## <a name="photo-metadata-policy-expressions"></a>Espressioni di criteri di metadati foto

Come indicato in precedenza, un'espressione di query completa inizia con una barra (/). Le espressioni che non iniziano con la barra vengono valutate come espressioni di criteri. Un'espressione dei criteri consente di eseguire una query sui metadati delle foto per ottenere informazioni relative Windows [proprietà della shell.](https://msdn.microsoft.com/library/ms788673(VS.85).aspx) Nella sezione Selezione dati più indietro in questo documento è stata usata l'espressione "/xmp/xmp:Rating" per accedere alla proprietà rating XMP. È anche possibile eseguire query su questa proprietà usando l'espressione di criteri seguente:

-   System.SimpleRating

Per accedere alla proprietà rating dallo schema MicrosoftPhoto, è possibile usare l'espressione di query seguente:

-   System.Rating

Le espressioni di criteri dei metadati foto si comportano in modo diverso rispetto alle query di metadati completi in alcuni modi.

In primo luogo, quando si accede ai metadati usando un'espressione di criteri, WIC esegue l'arbitraggio e la risoluzione dei conflitti nel caso in cui la stessa proprietà sia disponibile in più blocchi di metadati. Ad esempio, i valori di classificazione MicrosoftPhoto e XMP vengono archiviati sia nel blocco App1/IFD che nel blocco XMP. I criteri dei metadati delle foto determinano la precedenza per cui viene restituito il valore del blocco durante la lettura dei metadati. Quando si scrivono metadati, i criteri dei metadati delle foto assicurano la coerenza delle stesse proprietà in blocchi diversi. Se si usa una query di metadati, ad esempio "/xmp/xmp:Rating", l'utente è responsabile dell'arbitraggio tra le varie posizioni dei metadati.

> [!Note]  
> Per un elenco delle espressioni di criteri supportate e dei relativi criteri di mapping, vedere [l'argomento Criteri dei metadati delle](photo-metadata-policies.md) foto.

 

In secondo momento, le espressioni di criteri dei metadati delle foto sono indipendenti dal formato dell'immagine, mentre le query sui metadati completi non lo sono. Ad esempio, la query "/xmp/xmp:Rating" è specifica del formato JPEG. Le immagini TIFF supportano anche i metadati XMP, ma vengono archiviate in modo diverso rispetto a JPEG, quindi la query TIFF sarà "/ifd/xmp/xmp:Rating". Tuttavia, in entrambi i casi l'espressione dei criteri sarebbe "System.SimpleRating".

Le espressioni di criteri dei metadati foto offrono un livello più elevato di astrazione e semplicità rispetto alle query di metadati completi e pertanto dovrebbero essere preferibili nei casi in cui non è necessario l'accesso ai metadati di basso livello. Tuttavia, le espressioni di criteri forniscono l'accesso solo a un set limitato di metadati dell'immagine, mentre il linguaggio di query dei metadati fornisce l'accesso a quasi tutti i metadati archiviati all'interno di un file di immagine.

## <a name="metadata-query-language-summary"></a>Riepilogo del linguaggio di query sui metadati

La tabella seguente è una definizione formale del linguaggio di query dei metadati WIC. Ogni simbolo di grammatica rappresenta un'espressione che è costituito da altri simboli. L'espressione può essere un altro simbolo o una sequenza di altri simboli separati dalla barra verticale ( \| ), che indica una scelta "or". L'intera espressione a destra è una possibile sostituzione per il simbolo specificato a sinistra. 

| Simbolo                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | '<' \<name> '>'                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | 'char' \| 'uchar' \| 'short' \| 'ushort' \| 'long' \| 'ulong' \| 'int' \| 'uint' \| 'longlong' \| 'ulonglong' \| 'float' \| \| 'double' 'str' \| 'wstr' \| 'guid' \| 'bool' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | d'acquisto                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: Codificare nuovamente un'immagine JPEG con metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



