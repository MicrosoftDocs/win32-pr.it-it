---
description: In questo argomento viene presentato il linguaggio di query dei metadati per Windows Imaging Component (WIC).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Cenni preliminari sul linguaggio di query dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b55bdc7079565f98411e28977d3d8c41e191f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555199"
---
# <a name="metadata-query-language-overview"></a>Cenni preliminari sul linguaggio di query dei metadati

In questo argomento viene presentato il linguaggio di query dei metadati per Windows Imaging Component (WIC). Il linguaggio di query dei metadati viene utilizzato per creare espressioni che consentono di individuare dati specifici (elementi di metadati) e percorsi (blocchi di metadati) all'interno dei metadati di un'immagine.

In questo argomento sono contenute le sezioni seguenti.

-   [Prerequisiti](#prerequisites)
-   [Introduzione](#introduction)
-   [Anatomia di un'espressione di percorso](#anatomy-of-a-path-expression)
    -   [Selezione blocco](#block-selection)
    -   [Selezione elemento](#item-selection)
    -   [Carattere di escape](#escape-character)
    -   [Espressioni di esempio](#sample-expressions)
-   [Espressioni di criteri dei metadati foto](#photo-metadata-policy-expressions)
-   [Riepilogo del linguaggio di query dei metadati](#metadata-query-language-summary)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati WIC, come descritto in [Panoramica dei metadati di WIC](-wic-about-metadata.md) e accesso ai metadati, come descritto nella [Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).

## <a name="introduction"></a>Introduzione

Si interagisce con la piattaforma di metadati principalmente tramite due componenti Component Object Model (COM): un lettore di query, rappresentato dall'interfaccia [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , e un writer di query, rappresentato dall'interfaccia [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Questi componenti consentono di leggere o scrivere metadati utilizzando il linguaggio di query dei metadati. Il linguaggio di query descrive la sintassi di un'espressione di percorso e i componenti della query utilizzano questa espressione di percorso per accedere ai metadati desiderati. Questa espressione di percorso descrive la posizione di un blocco o di un elemento di metadati.

Un blocco di metadati è un gruppo denominato di metadati in un formato specifico. Un blocco di metadati può contenere singoli elementi di metadati, ad esempio un autore o un'ora di creazione e blocchi di metadati aggiuntivi. Il nome di un blocco di metadati è determinato dal formato. Un blocco di metadati che contiene i metadati App1, ad esempio, verrebbe denominato "app1". I formati di metadati comuni includono App1, EXIF, IFD e XMP.

Un elemento dei metadati è una coppia nome/valore che descrive caratteristiche quali autore, titolo e classificazione.

Un'espressione di percorso contiene uno o più nomi di blocchi di metadati. Può inoltre specificare un elemento di metadati all'interno di un blocco di metadati. L'espressione di percorso seguente rappresenta un blocco App1 che contiene un blocco IFD che contiene l'elemento dei metadati:

-   /App1/IFD/{ushort = 18249}

Il diagramma seguente illustra il trucco di un'immagine JPEG di esempio con quattro blocchi di metadati radice: APP0, App1, XMP e un blocco sconosciuto. Ogni elemento evidenziato rileva il tipo di metadati (blocco o elemento) e l'espressione di query utilizzata per recuperare i dati.

![immagine JPEG con callout di metadati](graphics/jpegwithcallouts.png)

> [!Note]  
> In questo documento viene fatto riferimento al contenuto di questo diagramma e vengono utilizzati in molti degli esempi.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomia di un'espressione di percorso

Per accedere ai metadati usando le API WIC, nella maggior parte dei casi è necessario usare un'espressione di query completa. In questo argomento vengono illustrate le espressioni complete per l'accesso ai metadati. Per informazioni sui casi in cui vengono usate espressioni non complete, vedere la sezione espressione di criteri di metadati foto più avanti in questo documento.

Che cos'è un'espressione di query completa? In WIC un'espressione completa è una stringa che inizia con la barra (/) del carattere del percorso, seguita da un percorso di navigazione a un blocco di metadati o a un elemento di metadati specifico. Ogni passaggio all'interno del percorso di navigazione è separato da una barra, formando un'espressione per l'accesso a un blocco di metadati o a un elemento di metadati. Ad esempio, di seguito è riportata un'espressione di query completa che accede a Microsoft Photo rating in un blocco IFD annidato in un blocco App1:

-   /App1/IFD/{ushort = 18249}

Quando WIC analizza questa espressione, cerca innanzitutto il blocco di metadati App1 nei metadati dell'immagine. Se il blocco App1 viene trovato, la ricerca continua la ricerca del blocco di metadati annidati di IFD. Se il blocco IFD viene trovato, Cerca l'elemento di metadati specifico, in questo caso la classificazione MicrosoftPhoto sotto il tag 18249, all'interno del blocco di metadati IFD. Se in qualsiasi momento WIC non trova un blocco o un elemento di metadati, la query viene interrotta.

### <a name="block-selection"></a>Selezione blocco

L'espressione di query dei metadati WIC più semplice è un'espressione per ottenere un Reader o un writer di query per un blocco di metadati specifico. Il recupero di un reader/writer di query consente di indirizzare le query successive direttamente a un blocco di metadati annidati senza gestire il relativo blocco padre. Un'espressione di query di selezione blocco è un percorso di navigazione al blocco di metadati desiderato. Nell'illustrazione precedente, ad esempio, sono presenti cinque blocchi di metadati, due dei quali sono annidati in altri blocchi di metadati. Di seguito sono riportate le espressioni di percorso per ogni blocco di metadati nell'esempio JPEG:

-   /app0
-   /App1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Quando si utilizza un Reader o un writer di query per eseguire una query, viene restituito un nuovo reader/writer di query che esegue le query nell'ambito del blocco di metadati specificato. Se ad esempio si esegue la query "/app1", viene ottenuto un nuovo Reader di query e le query al nuovo Reader sono relative al blocco App1. Ciò significa che la query "/IFD" è valida per il nuovo Reader perché il blocco App1 contiene un blocco IFD. Tuttavia, "/XMP" non funziona perché questo blocco App1 non contiene un blocco di metadati XMP.

Il linguaggio di query supporta inoltre la notazione di un indice. La notazione dell'indice fornisce l'accesso a un blocco di metadati specifico quando esistono più blocchi dello stesso tipo. Per l'esempio JPEG, è possibile usare l'espressione di percorso indicizzata seguente:

-   /\[0 \] App1/ \[ 0 \] IFD

Nel linguaggio di query tutti gli indici iniziano da zero. Nell'espressione precedente, la prima query zero per il primo blocco App1 e il secondo zero esegue una query sul primo blocco IFD annidato. La notazione dell'indice può comunque essere utilizzata anche quando non esistono più blocchi dello stesso tipo. Se nel file JPEG di esempio è incluso un secondo blocco App1 con un blocco IFD incorporato, \[ \] per accedere al secondo blocco App1 verrà utilizzata l'espressione "/1 App1/IFD".

La notazione dell'indice diventa più comune quando si gestiscono i blocchi di testo PNG perché è probabile che l'immagine PNG disponga di più di un blocco di testo.

> [!Note]  
> Gli indici di matrici multidimensionali non sono supportati.

 

### <a name="item-selection"></a>Selezione elemento

È possibile accedere agli elementi di metadati in un blocco di metadati compilando le espressioni di selezione dei blocchi. Prendere in considerazione le proprietà XMP e classificazione foto Microsoft nell'esempio JPEG. Questi metadati sono presenti in due blocchi di metadati, ovvero i blocchi App1/IFD e XMP. È pertanto possibile utilizzare più di un'espressione per accedere agli stessi dati. L'espressione seguente accede alla classificazione MicrosoftPhoto nel blocco XMP:

-   /XMP/XMP: valutazione

La parte "XMP:" dell'espressione è un identificatore descrittivo dello schema. XMP è uno standard estendibile e consente a entità di terze parti di pubblicare schemi propri che definiscono come archiviare determinati elementi di metadati. Uno schema XMP è completamente identificato da un URL, ma WIC fornisce un set di identificatori descrittivi per gli schemi noti. Per ulteriori informazioni, vedere l'argomento relativo alle [query di metadati in formato immagine nativo](-wic-native-image-format-metadata-queries.md) .

Per le immagini JPEG, le informazioni sulle classificazioni possono essere archiviate anche all'interno del blocco IFD annidato App1. Tuttavia, a differenza dell'esempio di classificazione XMP, il blocco IFD non usa un nome di schema per accedere alle informazioni di valutazione. Viene invece utilizzata un'espressione di dati. L'espressione seguente viene utilizzata per accedere alla classificazione MicrosoftPhoto nel blocco IFD annidato App1:

-   /App1/IFD/{ushort = 18249}

In questa espressione, la parte "/app1/IFD" dell'espressione è il percorso di navigazione del blocco IFD (come illustrato in precedenza nella sezione di selezione dei blocchi). La seconda parte dell'espressione "/{ushort = 18249}" accede ai dati. Questa parte dell'espressione indica al parser di query di trovare i dati incorporati nel tag short senza segno con l'identificatore di tag 18249.

> [!Note]  
> Per un elenco dei formati di metadati comuni supportati da ogni formato di immagine in, vedere l'argomento relativo alle [query di metadati in formato immagine nativo](-wic-native-image-format-metadata-queries.md) .

 

{Ushort = 18249} è un'espressione di dati e può assumere diverse forme. Un'espressione di dati è un'espressione a due parti contenente la chiave o il tag di metadati richiesto, in questo caso "18249", e il tipo di dati della chiave, in questo caso "ushort". Le due parti sono separate da un segno di uguale (=). WICsupports la maggior parte dei tipi di dati comuni di C/C++. I tipi di dati seguenti sono accettati dal linguaggio di query:

-   char
-   UCHAR
-   short
-   ushort
-   long
-   ulong
-   INT
-   uint
-   longlong
-   float
-   double
-   str
-   WSTR
-   guid
-   bool

> [!Note]  
> Questo elenco specifica solo i tipi di dati supportati dal linguaggio di query dei metadati. Usare questi tipi di dati quando si crea un'espressione di dati di query dei metadati, ad esempio {ushort = 18249}. WIC restituisce il valore dell'elemento dei metadati sotto forma di PROPVARIANT, che definisce il proprio sistema di tipi.

 

"18249" nell'esempio è il tag di dati. Questo numero specifico è definito da Microsoft per contenere la classificazione MicrosoftPhoto. Il tag dati può essere qualsiasi numero, stringa o GUID a seconda dell'elemento dati che si sta cercando

A differenza dell'esempio di classificazione XMP, non esiste alcun conflitto di nomi per il valore della classificazione nel blocco App1/IFD. Questo è dovuto al fatto che il valore della classificazione XMP viene effettivamente archiviato in un altro tag ushort, 18246. L'espressione per accedere alla classificazione XMP nel blocco App1/IFD è quindi:

-   /App1/IFD/{ushort = 18246}

> [!Note]  
> Per una descrizione formale del linguaggio di query dei metadati, vedere la sezione Riepilogo del linguaggio di query dei metadati più avanti in questo documento.

 

### <a name="escape-character"></a>Carattere escape

Il linguaggio di query non fa distinzione tra maiuscole e minuscole e considera tutti i caratteri come minuscoli. Tuttavia, alcuni formati di metadati, ad esempio XMP, fanno distinzione tra maiuscole e minuscole. Quando si utilizza un formato di metadati con distinzione tra maiuscole e minuscole, utilizzare il carattere barra rovesciata ( \\ ) quando si desidera specificare un carattere maiuscolo.

Il carattere di escape viene utilizzato dal parser del linguaggio e il carattere seguente che lo segue viene interpretato direttamente. Ad esempio, l'espressione {char = \\ \\ } viene risolta come ' \\ ' e {char = \\ C} viene risolta come una c maiuscola. Senza il carattere di escape, {char = \\ } potrebbe essere un'espressione non valida e {char = C} verrebbe interpretato come un C minuscolo. Assicurarsi di usare il carattere di escape barra rovesciata prima di tutte le lettere maiuscole nei formati di metadati con distinzione tra maiuscole e minuscole.

### <a name="sample-expressions"></a>Espressioni di esempio

Nella tabella seguente sono riportate alcune espressioni di esempio e descrizioni delle relative interpretazioni da parte del parser del linguaggio di query. 

| Expression                     | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IFD/XMP/EXIF: autore            | Corrisponde al percorso di navigazione seguente: IFD Block-> XMP Block-> proprietà "Author" nello schema "Exif".                                                                                                                                                                                                                                            |
| /\[1 \] IFD/ \[ 0 \] XMP/EXIF: Author | Uguale al primo elemento in questa tabella, ad eccezione del fatto che il \[ \# \] prefisso descrive l'elemento da esplorare in caso di conflitto di nomi.                                                                                                                                                                                                                                |
| /IFD/{ushort = 700}/Author       | Uguale al primo elemento in questa tabella, ad eccezione del fatto che usa un'espressione di dati per fare riferimento al blocco XMP anziché al nome del blocco "XMP" (il blocco XMP è incorporato nell'identificatore di tag breve senza segno 700). Inoltre, la proprietà "Author" non specifica uno schema. Il parser di query tenterà di trovare una corrispondenza tra la proprietà di tutti gli schemi e restituirà la prima corrispondenza. |
| /ifd/xmp                       | Fornisce un percorso di navigazione a un blocco di metadati. Se il blocco viene trovato, viene restituito un nuovo reader/writer di metadati.                                                                                                                                                                                                                                                 |
| /\[\*\]Testo/parola chiave            | Ottiene o imposta la proprietà keyword per un blocco PNG. Poiché la specifica dei metadati PNG consente più blocchi di un determinato tipo, la \[ \* \] notazione Ottiene o imposta il blocco png dei dati con la proprietà appropriata. Per la specifica PNG, due blocchi non possono avere le stesse proprietà.                                                                |



 

Ogni blocco di metadati viene inoltre identificato in modo univoco dal GUID dei metadati che può essere utilizzato al posto del nome descrittivo del blocco. Per fornire nomi di blocco, è possibile usare la sintassi seguente: "/{GUID = GUID}/ \[ n \] {GUID = Guid}/schema: tagidentifier"

Nella tabella seguente vengono forniti alcuni esempi non validi e i motivi per cui verranno rifiutati. 

| Espressione non valida         | Descrizione rifiuto                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /IFD/ \[ 0 \] \[ 2 \] EXIF/       | Rifiutato perché gli indici di matrici multidimensionali non sono supportati.                                                                                                    |
| /IFD/{ushort = 1}/{ushort = 2} | Rifiutato a meno che IFD non abbia tagID = 1, ovvero un gestore di metadati che contiene un elemento di metadati con tagID = 2.                                                        |
| /{ushort = 1}                | Rifiutato se l'elaborazione della query è relativa a un livello superiore della gerarchia dei metadati. Questo perché il livello principale contiene solo blocchi di metadati e non elementi di dati. |



 

## <a name="photo-metadata-policy-expressions"></a>Espressioni di criteri dei metadati foto

Come indicato in precedenza, un'espressione di query completa inizia con una barra (/). Le espressioni che non iniziano con la barra vengono valutate come espressioni di criteri. Un'espressione di criteri consente di eseguire una query sui metadati della foto per le [proprietà della shell](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)di Windows correlate all'immagine. Nella sezione relativa alla selezione dei dati riportata in precedenza in questo documento è stata usata l'espressione "/XMP/XMP: rating" per accedere alla proprietà rating XMP. È anche possibile eseguire query su questa proprietà usando l'espressione di criteri seguente:

-   System. SimpleRating

Per accedere alla proprietà rating dallo schema MicrosoftPhoto, è possibile usare l'espressione di query seguente:

-   System. rating

Le espressioni di criteri dei metadati delle foto si comportano in modo diverso rispetto alle query di metadati complete in pochi modi.

Per prima cosa, quando si accede ai metadati mediante un'espressione di criteri, WIC esegue l'arbitraggio e la risoluzione dei conflitti nel caso in cui la stessa proprietà sia disponibile in più blocchi di metadati. Ad esempio, i valori di MicrosoftPhoto e di classificazione XMP vengono archiviati sia nel blocco App1/IFD che nel blocco XMP. Il criterio dei metadati della foto determina la precedenza per cui viene restituito il valore di blocco durante la lettura dei metadati. Quando si scrivono i metadati, i criteri dei metadati delle foto garantiscono che le stesse proprietà in blocchi diversi siano coerenti. Se si utilizza una query di metadati, ad esempio "/XMP/XMP: rating", si è responsabili di arbitrali tra le varie posizioni dei metadati.

> [!Note]  
> Per un elenco delle espressioni di criteri supportate e dei relativi criteri di mapping, vedere l'argomento relativo ai [criteri di metadati della foto](photo-metadata-policies.md) .

 

In secondo luogo, le espressioni di criteri dei metadati delle foto sono indipendenti dal formato di immagine, mentre le query di metadati complete non lo sono. Ad esempio, la query "/XMP/XMP: rating" è specifica del formato JPEG. Le immagini TIFF supportano anche i metadati XMP, ma vengono archiviati in modo diverso rispetto a JPEG, quindi la query TIFF sarà "/IFD/XMP/XMP: rating". In entrambi i casi, tuttavia, l'espressione di criteri è "System. SimpleRating".

Le espressioni di criteri dei metadati delle foto forniscono un livello di astrazione e semplicità più elevato rispetto alle query di metadati complete e pertanto dovrebbero essere preferite nei casi in cui l'accesso ai metadati di basso livello non è necessario. Tuttavia, le espressioni di criteri forniscono solo l'accesso a un set limitato di metadati dell'immagine, mentre il linguaggio di query dei metadati consente di accedere a quasi tutti i metadati archiviati in un file di immagine.

## <a name="metadata-query-language-summary"></a>Riepilogo del linguaggio di query dei metadati

La tabella seguente è una definizione formale del linguaggio di query dei metadati WIC. Ogni simbolo di grammatica rappresenta un'espressione costituita da altri simboli. L'espressione può essere un altro simbolo o una sequenza di altri simboli separati dalla barra verticale ( \| ), che indica una scelta "or". L'intera espressione a destra è una possibile sostituzione per il simbolo specificato a sinistra. 

| Simbolo                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | ' <' \<name> ' >'                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | ' Char ' \| ' UCHAR '' \| Short ' \| ' ushort ' \| ' Long ' \| ' ulong ' \| ' int ' \| ' uint ' \| ' LONGLONG '' \| ULONGLONG '' \| float ' \| ' Double ' \| ' Str ' \| ' WSTR ' \| ' GUID ' \| ' bool ' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | d'acquisto                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> <dt>

[Panoramica della lettura e della scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Panoramica dell'estendibilità dei metadati](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Procedura: ricodificare un'immagine JPEG con i metadati](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



