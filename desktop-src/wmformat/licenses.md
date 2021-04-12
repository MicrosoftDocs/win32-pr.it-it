---
title: Licenze
description: Licenze
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), licenze file protette
- DRM (Digital Rights Management), licenze file protette
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332308"
---
# <a name="licenses"></a>Licenze

Una licenza è un set di dati che descrive le condizioni in base alle quali è possibile leggere i dati nei file protetti. Ogni licenza viene applicata a un identificatore di chiave, che in genere viene assegnato a un singolo file multimediale. Questo identificatore viene usato per identificare il contenuto protetto nella licenza.

Ogni licenza specifica una o più azioni che possono essere eseguite con il contenuto protetto. Queste azioni, denominate anche diritti, possono essere limitate in diversi modi. Combinando le date di inizio, le date di fine, i conteggi e i limiti di tempo, l'emittente della licenza può creare qualsiasi limitazione immaginabile su un diritto.

Le licenze vengono rilasciate da un servizio Web. Quando viene acquisita una licenza, questa viene archiviata nel computer client nell'archivio licenze locale, ovvero un file protetto che contiene licenze e altri dati DRM. Quando un'applicazione accede al contenuto protetto, il sottosistema DRM Cerca nell'archivio licenze locale una licenza che conceda il diritto appropriato. Se non viene trovata alcuna licenza, l'applicazione può acquisirne una in base alle informazioni archiviate nell'intestazione DRM del file.

È possibile emettere più licenze per lo stesso file protetto. Quando il sottosistema DRM determina se un'azione è consentita, aggrega i diritti da tutte le licenze che si applicano. A ogni licenza può essere assegnata una priorità. Se a un'azione viene applicata più di una licenza, viene verificata la licenza con priorità più elevata per determinare se è necessario decrementare i conteggi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




