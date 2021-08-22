---
title: Uso degli annunci
description: Uso degli annunci
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows playlist metafile multimediali,annunci
- playlist, annunci
- playlist di metafile, annunci
- Windows Media Player,annunci
- annunci
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 24408211f6ce708d380406026de45be0cce86521fdc188aaaf785ccf03790c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134384"
---
# <a name="using-announcements"></a>Uso degli annunci

Un annuncio è un file che contiene informazioni sull'URL per un flusso multimediale, inclusi l'indirizzo IP multicast, la porta, il formato del flusso e altre impostazioni della stazione. Gli annunci vengono creati da Windows Media Administrator quando viene creato un flusso di pubblicazione unicast o multicast. Il client può caricare rapidamente il file dell'annuncio e quindi procedere con l'accesso al file multimediale di streaming.

Per un punto di pubblicazione unicast, viene aperto il flusso multimediale del punto di pubblicazione. Per un punto di pubblicazione multicast, l'URL viene estratto da un file di stazione di trasmissione con estensione nsc e viene eseguito l'accesso ai supporti di streaming. A differenza di un flusso unicast, nessuna informazione di intestazione è contenuta in un flusso multicast. Queste informazioni provengono dal file della stazione di trasmissione con estensione nsc. Windows Media Player apre in genere un file di annuncio, che viene utilizzato per le playlist di metafile, che punta al percorso del file della stazione di trasmissione.

Codice di esempio


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Uso di playlist di metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




