---
title: Creazione di playlist di metafile
description: Creazione di playlist di metafile
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows playlist di metafile multimediali, creazione
- playlist, creazione
- playlist di metafile, creazione
- creazione Windows playlist di metafile multimediali
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 765d8ab507c2ce502f1cad021696b0fc2ecfd110da8dfa95ccc84a43a8987561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750468"
---
# <a name="creating-metafile-playlists"></a>Creazione di playlist di metafile

È possibile creare una playlist usando qualsiasi editor di testo, ad esempio Microsoft Blocco note. Aprire l'editor di testo. Digitare le voci di script da implementare. Dopo aver terminato di digitare in Blocco note, salvare il file con un nome file e un'estensione di file appropriati. Per altre informazioni sulle estensioni, vedere [Linee guida per le estensioni dei metafile.](metafile-extension-guidelines.md) Il nome del file è in genere il nome del flusso o del file multimediale Windows seguito da un'estensione di file con estensione .più, .wvx o .asx. Ad esempio, se il contenuto multimediale è un file audio di Windows Media con estensione wma, usare l'estensione .extension per denominare la playlist. Le playlist non devono includere codici di formattazione di un elaboratore di testo, ad esempio Microsoft Word. Per assicurarsi che nella playlist non siano inclusi codici di formattazione, salvare il file come file di testo normale o ASCII.

> [!Note]  
> Gli elementi e gli attributi non supportano la distinzione tra maiuscole e minuscole. Il testo usato nella playlist per definire un elemento o un attributo può essere maiuscolo o minuscolo o una combinazione di entrambi.

 

Se un elemento non ha elementi figlio (quelli che modificano o sono contenuti all'interno di un altro elemento), è possibile usare un singolo carattere barra (/) alla fine del tag di apertura, subito prima del tag ">", al posto di un tag di chiusura. Gli elementi figlio di un elemento devono essere presenti tra il tag di apertura e quello di chiusura dell'elemento; in caso contrario, non sono elementi figlio per tale elemento e vengono ignorati o causano un errore nella sintassi della playlist.

I primi quattro caratteri di una playlist devono essere &lt; "ASX". **L'elemento ASX** viene usato in tutte le playlist, indipendentemente dal fatto che l'estensione sia .tutto, .wvx o .asx. Deve essere presente un solo **elemento ASX** per playlist. Questo elemento identifica il file come playlist di metafile Windows media. Non specifica il tipo di playlist.

**L'elemento ASX** ha tre attributi possibili:

**VERSION**

**L'attributo VERSION** è obbligatorio e deve seguire immediatamente dopo l'elemento **ASX,** ad esempio "<ASX version = "3.0" &gt; ". Il numero di versione corrente è 3.0. Windows Media Player supporta tutte le versioni precedenti. I valori accettabili per **l'attributo VERSION** includono sia 3.0 che 3 (senza separatore decimale).

**MODALITÀ DI ANTEPRIMA**

**L'attributo PREVIEWMODE** è facoltativo. Fornisce un altro meccanismo per specificare per quanto tempo eseguire il rendering di una clip. Se il valore **dell'attributo PREVIEWMODE** è YES, Windows Media Player eseguirà il rendering di ogni clip per la durata specificata dall'elemento **PREVIEWDURATION.** Per ogni clip può essere **specificata un'opzione PREVIEWDURATION.**

**BARRA BANNER**

**L'attributo BANNERBAR facoltativo** definisce se il Windows Media Player riserva spazio per un'immagine banner. Usare **l'elemento BANNER** per specificare l'elemento grafico da visualizzare. Se il valore di **BANNERBAR** è FIXED, Windows Media Player riserva spazio banner per la visualizzazione e per ogni clip, indipendentemente dal fatto che la playlist del metafile specifichi un banner per la presentazione o il clip. In questo modo le dimensioni della finestra Windows Media Player verranno conservate allo stesso modo (tranne quando le dimensioni del video cambiano) indipendentemente dall'assenza o dalla presenza di un banner grafico. Se alla visualizzazione o al clip non è associato un banner, lo spazio riservato per uno è nero. Se il valore **dell'attributo BANNERBAR** è AUTO, Windows Media Player riserva spazio per il banner solo quando la visualizzazione o il clip ne include uno.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Per altre informazioni sui tre attributi **dell'elemento ASX,** vedere la voce di riferimento per l'elemento [ASX](asx-element.md).

Un **elemento ASX** contiene **elementi figlio ENTRY** che definiscono le informazioni sui file multimediali a cui accedere. Ogni **elemento ENTRY** deve contenere un elemento **REF** che specifica il percorso del file multimediale da trasmettere. In un elemento **ASX** deve essere presente almeno un elemento **ENTRY** o **ENTRYREF.**

Altri elementi definiti nell'ambito dell'elemento **ASX,** ad esempio **TITLE** e **AUTHOR,** sono associati ai metadati visualizzati da Windows Media Player.

Le playlist più semplici vengono create aggiungendo più **elementi ENTRY** con un singolo **elemento REF** a un metafile. Il **rendering di** ogni elemento ENTRY in una playlist di metafile viene eseguito nell'ordine in cui appare nel file come se l'utente avesse aperto manualmente ogni clip.

Codice di esempio


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



Assicurarsi che la playlist funzioni facendo doppio clic su di essa in Windows Explorer. Windows Media Player aprire e avviare lo streaming del contenuto multimediale. **Dopo** aver confermato il funzionamento della playlist, salvarla nel server Web insieme alle pagine Web e collegarla tramite un elemento **HREF** oppure incorporarla in una pagina Web usando l'elemento OBJECT Windows Media Player.

Le sezioni seguenti contengono altre informazioni:

-   [Annidamento di metafile](nesting-metafiles.md)
-   [Uso di pagine ASP per creare in modo Windows playlist di metafile multimediali](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




