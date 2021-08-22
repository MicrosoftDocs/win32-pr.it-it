---
title: Uso di parametri e comandi personalizzati
description: Uso di parametri e comandi personalizzati
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows playlist metafile multimediali,parametri personalizzati
- playlist, parametri personalizzati
- playlist di metafile, parametri personalizzati
- Windows playlist metafile multimediali,comandi personalizzati
- playlist, comandi personalizzati
- playlist di metafile, comandi personalizzati
- Windows playlist metafile multimediali,parametri
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
ms.openlocfilehash: d6848131c58dabfa465a202bd39b061997e2a9bbda3e8004133f1ef1ce1d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830937"
---
# <a name="using-custom-parameters-and-commands"></a>Uso di parametri e comandi personalizzati

È possibile creare parametri personalizzati per passare metadati aggiuntivi in una playlist di metafile usando **l'elemento PARAM.** Usare **l'attributo NAME** **dell'elemento PARAM** per definire il nome del parametro personalizzato. Usare **l'attributo VALUE** per definire il valore per il parametro personalizzato denominato.

Recuperare **i metadati PARAM** usando i **metodi getItemInfo** degli **oggetti Media** e **Playlist.** Per un esempio sull'uso di questi metodi per recuperare i metadati, vedere il [metodo attributeCount](playlist-attributecount.md) dell'oggetto **Playlist.**

La playlist di metafile di esempio seguente illustra l'uso **dell'elemento PARAM** per definire parametri personalizzati.


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

[**Uso di playlist metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




