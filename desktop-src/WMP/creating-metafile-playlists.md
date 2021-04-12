---
title: Creazione di playlist di metafile
description: Creazione di playlist di metafile
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Playlist Windows Media Metafile, creazione
- playlist, creazione
- playlist di metafile, creazione
- creazione di playlist Windows Media Metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221782"
---
# <a name="creating-metafile-playlists"></a>Creazione di playlist di metafile

È possibile creare una playlist utilizzando qualsiasi editor di testo, ad esempio Blocco note di Microsoft. Aprire l'editor di testo. Digitare le voci di script che si desidera implementare. Al termine della digitazione nel blocco note, salvare il file con un nome file e un'estensione di file appropriati. Per altre informazioni sulle estensioni, vedere [linee guida sull'estensione metafile](metafile-extension-guidelines.md). Il nome file è in genere il nome del file o del flusso di Windows Media seguito da un'estensione di. Wax,. wvx o. asx. Se, ad esempio, il contenuto multimediale è un file audio Windows Media con estensione WMA, utilizzare l'estensione cera quando si assegna un nome alla playlist. Le playlist non devono includere codici di formattazione da un elaboratore di testo, ad esempio Microsoft Word. Per assicurarsi che nella playlist non siano inclusi codici di formattazione, salvare il file come file di testo normale o ASCII.

> [!Note]  
> Elementi e attributi non fanno distinzione tra maiuscole e minuscole. Il testo usato nella playlist per definire un elemento o un attributo può essere maiuscolo o minuscolo o una combinazione di entrambi.

 

Se un elemento non dispone di elementi figlio (quelli che modificano o sono contenuti all'interno di un altro elemento), è possibile usare una singola barra (/) alla fine del tag di apertura, immediatamente prima di ">", al posto di un tag di chiusura. Gli elementi figlio di un elemento devono essere visualizzati tra il tag di apertura e di chiusura per l'elemento. in caso contrario, non si tratta di elementi figlio per l'elemento e vengono ignorati o generano un errore nella sintassi della playlist.

I primi quattro caratteri di una playlist devono essere " &lt; ASX". L'elemento **ASX** viene usato in tutte le playlist se la relativa estensione è. Wax,. wvx o. asx. Deve essere presente un solo elemento **ASX** per playlist. Questo elemento identifica il file come playlist Windows Media Metafile. Non specifica il tipo di playlist.

L'elemento **ASX** ha tre attributi possibili:

**VERSION**

L'attributo **Version** è obbligatorio e deve essere seguito immediatamente dopo l'elemento **ASX** , ad esempio "<ASX Version =" 3,0 " &gt; ". Il numero di versione corrente è 3,0. Windows Media Player supporta tutte le versioni precedenti. I valori accettabili per l'attributo **Version** includono sia 3,0 che 3 (senza virgola decimale).

**PREVIEWMODE**

L'attributo **PREVIEWMODE** è facoltativo. Fornisce un altro meccanismo per specificare per quanto tempo eseguire il rendering di un clip. Se il valore dell'attributo **PREVIEWMODE** è sì, Windows Media Player eseguirà il rendering di ogni clip per la durata specificata dall'elemento **PREVIEWDURATION**. Ogni clip può avere un **PREVIEWDURATION** specificato.

**BANNERBAR**

L'attributo facoltativo **BANNERBAR** definisce se il controllo Media Player Windows riserva spazio per una rappresentazione grafica del banner. (Usare l'elemento **banner** per specificare l'immagine da visualizzare). Se il valore di **BANNERBAR** è fixed, Windows Media Player riserva lo spazio del banner per la visualizzazione e per ogni clip, indipendentemente dal fatto che la playlist del metafile specifichi un banner per la visualizzazione o la clip. In questo modo, le dimensioni della finestra di Media Player di Windows vengono mantenute uguali (tranne quando le dimensioni del video cambiano) indipendentemente dall'assenza o dalla presenza di un grafico del banner. Se alla Mostra o alla clip non è associato alcun banner, lo spazio riservato per uno è nero. Se il valore dell'attributo **BANNERBAR** è auto, Windows Media Player riserva spazio per il banner solo quando la visualizzazione o la clip ne include una.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Per ulteriori informazioni sui tre attributi dell'elemento **ASX** , vedere la voce di riferimento per l' [elemento ASX](asx-element.md).

Un elemento **ASX** contiene elementi figlio **entry** che definiscono informazioni sui file multimediali a cui accedere. Ogni elemento **entry** deve contenere un elemento **ref** che specifica il percorso del file multimediale da trasmettere. È necessario che sia presente almeno un elemento **entry** o **ENTRYREF** all'interno di un elemento **ASX** .

Gli altri elementi definiti nell'ambito dell'elemento **ASX** , ad esempio **titolo** e **autore**, sono associati ai metadati visualizzati da Windows Media Player.

Le playlist più semplici vengono create aggiungendo più elementi **entry** con un singolo elemento **ref** a un metafile. Ogni elemento **entry** in una playlist di metafile viene sottoposto a rendering nell'ordine in cui viene visualizzato nel file come se l'utente avesse aperto manualmente ogni clip.

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



Assicurarsi che la playlist funzioni facendo doppio clic su di essa in Esplora risorse. Windows Media Player dovrebbe aprire e avviare lo streaming del contenuto multimediale. Dopo aver verificato il corretto funzionamento della playlist, salvarla nel server Web insieme alle pagine Web e collegarla tramite un elemento **href** oppure incorporarla in una pagina Web usando l'elemento **oggetto** di Windows Media Player.

Le sezioni seguenti contengono ulteriori informazioni:

-   [Annidamento di metafile](nesting-metafiles.md)
-   [Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




