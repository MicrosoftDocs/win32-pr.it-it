---
title: Cenni preliminari sui file di Windows Media
description: Cenni preliminari sui file di Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Metafile di Windows Media, informazioni
- Windows Media Player, metafile
- Windows Media Player, metafile di Windows Media
- Metafile, informazioni
- Windows Media, metafile
- Playlist Windows Media Metafile, informazioni
- playlist, informazioni
- Metafile di Windows Media, sintassi
- Metafile, sintassi
- playlist di metafile, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298211"
---
# <a name="windows-media-metafiles-overview"></a>Cenni preliminari sui file di Windows Media

La parte più importante della corretta utilizzo di metafile Windows Media consiste nell'utilizzare la sintassi corretta per gli elementi del metafile. Gli errori di sintassi in un metafile di Windows Media possono causare qualsiasi operazione da un singolo attributo che viene trascurato, in modo che il metafile non venga riconosciuto come valido e non riesca a funzionare.

È altrettanto importante l'ordine in cui gli elementi vengono visualizzati in un metafile di Windows Media. Gli attributi di alcuni elementi eseguono temporaneamente l'override degli attributi di elementi simili in sezioni diverse del metafile. Esiste un [ordine di precedenza](order-of-precedence.md)definito.

Le playlist Windows Media metafile sono metafile di Windows Media che forniscono informazioni utilizzate da Windows Media Player per ricevere flussi unicast, flussi multicast e altri supporti supportati da una rete Intranet o Internet. Una playlist di metafile è fondamentalmente un collegamento al contenuto multimediale. Una playlist di metafile può essere inviata come messaggio di posta elettronica, usata come riferimento al collegamento in una pagina Web, creata dinamicamente tramite Active Server Pages (ASP) o esistere come file autonomo in un'unità disco locale. Una playlist di metafile può fare riferimento a un'altra playlist di metafile, a una pagina ASP o a un file di Windows Media Station (con estensione di file NSC). Un file con estensione NSC viene usato per definire un Windows Media Station per Windows Media Player. Il processo di gestione di base è lo stesso per ogni caso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui metafile di Windows Media**](about-windows-media-metafiles.md)
</dt> </dl>

 

 




