---
title: Uso di parametri e comandi personalizzati
description: Uso di parametri e comandi personalizzati
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Playlist Windows Media Metafile, parametri personalizzati
- playlist, parametri personalizzati
- playlist di metafile, parametri personalizzati
- Playlist Windows Media Metafile, comandi personalizzati
- playlist, comandi personalizzati
- playlist di metafile, comandi personalizzati
- Playlist di Windows Media Metafile, parametri
- playlist, parametri
- playlist di metafile, parametri
- parametri personalizzati
- comandi personalizzati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856326"
---
# <a name="using-custom-parameters-and-commands"></a>Uso di parametri e comandi personalizzati

È possibile creare parametri personalizzati per passare metadati aggiuntivi in una playlist di metafile usando l'elemento **param** . Usare l'attributo **Name** dell'elemento **param** per definire il nome del parametro personalizzato. Utilizzare l'attributo **value** per definire il valore per il parametro personalizzato denominato.

Recuperare i metadati **param** usando i metodi **GetItemInfo** degli oggetti **media** e **playlist** . Per un esempio di utilizzo di questi metodi per recuperare i metadati, vedere il metodo [attributeCount](playlist-attributecount.md) dell'oggetto **playlist** .

La playlist del metafile di esempio seguente illustra l'uso dell'elemento **param** per definire parametri personalizzati.


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




