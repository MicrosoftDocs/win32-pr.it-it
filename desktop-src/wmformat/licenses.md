---
title: Licenses
description: Licenses
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- digital rights management (DRM), licenze file protette
- DRM (Digital Rights Management),gestione delle licenze file protette
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b899e44ffdff5d2a7f3c5fb3237b477ae0143327a331f63bd9717e3ae4320483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700835"
---
# <a name="licenses"></a>Licenses

Una licenza è un set di dati che descrive le condizioni in cui è possibile leggere i dati nei file protetti. Ogni licenza si applica a un identificatore di chiave, che in genere viene assegnato a un singolo file multimediale. Questo identificatore viene usato per identificare il contenuto protetto nella licenza.

Ogni licenza specifica una o più azioni che possono essere eseguite con il contenuto protetto. Queste azioni, denominate anche diritti, possono essere limitate in diversi modi. Combinando le date di inizio, le date di fine, i conteggi e i limiti di tempo, l'emittente della licenza può creare quasi tutte le limitazioni che è possibile immaginare a destra.

Le licenze vengono rilasciate da un servizio Web. Quando viene acquisita, una licenza viene archiviata nel computer client nell'archivio licenze locale, ovvero un file protetto che contiene licenze e altri dati DRM. Quando un'applicazione accede al contenuto protetto, il sottosistema DRM cerca nell'archivio licenze locale una licenza che concede il diritto appropriato. Se non viene trovata alcuna licenza, l'applicazione può acquisirne una in base alle informazioni archiviate nell'intestazione DRM del file.

È possibile emesse più licenze per lo stesso file protetto. Quando il sottosistema DRM determina se un'azione è consentita, aggrega i diritti di tutte le licenze applicabili. A ogni licenza può essere assegnata una priorità. Se a un'azione si applica più di una licenza, viene verificata la licenza con la priorità più alta per determinare se è necessario diminuire i conteggi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




