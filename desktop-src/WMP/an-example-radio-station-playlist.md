---
title: Una playlist di esempio di Radio Station
description: Una playlist di esempio di Radio Station
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Playlist Windows Media Metafile, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Playlist Windows Media Metafile, esempio di playlist della stazione radio
- playlist, esempio di playlist della stazione radio
- playlist di metafile, esempio di playlist della stazione radio
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Esempio di playlist di Windows Media Player, Radio Station
- esempi di playlist
- playlist di esempio
- playlist di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395739"
---
# <a name="an-example-radio-station-playlist"></a>Una playlist di esempio di Radio Station

Il codice di esempio seguente illustra come creare una playlist per analizzare tre stazioni radio rock. Il marchio di radio Adventure Works fittizio si trova nella playlist e in tutti i singoli flussi all'interno della playlist. Quando si scrive il codice, modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.

Viene creata una playlist per ogni stazione. Una quarta playlist analizza i primi tre. Le playlist vengono create per fare riferimento a inserzioni generate in modo dinamico e hanno la personalizzazione di Adventure Works radio.

Una delle playlist che rappresenta una stazione radio potrebbe essere simile alla seguente.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



La playlist può quindi essere costruita con riferimenti alle singole playlist.

Codice di esempio


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



In questo esempio viene riprodotto un annuncio seguito da 30 secondi di ognuna delle tre stazioni a cui viene fatto riferimento, una dopo l'altra. Questo ciclo si ripete per un periodo illimitato perché l'attributo **count** dell'elemento **Repeat** non è definito.

-   Ogni riferimento a società, organizzazioni, prodotti, persone ed eventi utilizzati negli esempi è puramente casuale e ha il solo scopo di illustrare l'uso del prodotto Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




