---
title: Uso degli annunci
description: Uso degli annunci
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Playlist Windows Media Metafile, annunci
- playlist, annunci
- playlist di metafile, annunci
- Windows Media Player, annunci
- annunci
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298085"
---
# <a name="using-announcements"></a>Uso degli annunci

Un annuncio è un file che contiene informazioni sull'URL per un flusso multimediale, tra cui l'indirizzo IP multicast, la porta, il formato del flusso e altre impostazioni della stazione. Gli annunci vengono creati da amministratore di Windows Media quando viene creato un flusso di pubblicazione unicast o multicast. Il client può caricare rapidamente il file di annuncio, quindi procedere con l'accesso al file multimediale di streaming.

Per un punto di pubblicazione unicast, viene aperto il flusso multimediale del punto di pubblicazione. Per un punto di pubblicazione multicast, l'URL viene Estratto da un file della stazione di trasmissione con estensione NSC e viene eseguito l'accesso al supporto di streaming. A differenza di un flusso unicast, nessuna informazione di intestazione è contenuta in un flusso multicast. Tali informazioni provengono dal file della stazione di trasmissione con estensione NSC. Windows Media Player in genere apre prima di tutto un file di annuncio, ovvero un uso per le playlist di metafile, che punta al percorso del file della stazione di trasmissione.

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

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




