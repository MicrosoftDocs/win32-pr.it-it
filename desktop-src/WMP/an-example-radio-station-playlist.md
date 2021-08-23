---
title: Esempio di playlist di stazione radio
description: Esempio di playlist di stazione radio
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows playlist di metafile multimediali, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Windows playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows Playlist di metafile multimediali, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Windows Playlist di metafile multimediali, esempio di playlist di stazione radio
- playlist, esempio di playlist di stazione radio
- playlist di metafile, esempio di playlist di stazione radio
- Windows Media Player, esempi di playlist
- Windows Media Player,playlist di esempio
- Windows Media Player, playlist di esempio
- Windows Media Player,radio station playlist example
- Esempi di playlist
- playlist di esempio
- playlist di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6db52d8eb9f109df870e65f79906761cfadee4a7871f4776fae3122dd93c8605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055029"
---
# <a name="an-example-radio-station-playlist"></a>Esempio di playlist di stazione radio

Il codice di esempio seguente illustra come creare una playlist per analizzare tre stazioni radio di roccia. Il marchio fittizio Adventure Works Radio è nella playlist e in tutti i singoli flussi all'interno della playlist. Quando si scrive il codice, modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Windows Media Player.

Viene creata una playlist per ognuna delle stazioni. Una quarta playlist analizza i primi tre. Le playlist vengono create per fare riferimento agli annunci generati dinamicamente e hanno il marchio Adventure Works Radio.

Una delle playlist che rappresentano una stazione radio potrebbe essere simile alla seguente.


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



In questo esempio viene riprodotto un annuncio seguito da 30 secondi di ognuna delle tre stazioni a cui si fa riferimento, una dopo l'altra. Questo ciclo verrà ripetuto per un periodo illimitato perché **l'attributo COUNT** dell'elemento **REPEAT** non è definito.

-   Ogni riferimento a società, organizzazioni, prodotti, persone ed eventi utilizzati negli esempi è puramente casuale e ha il solo scopo di illustrare l'uso del prodotto Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




