---
title: Considerazioni sulla sicurezza del punto di controllo
description: Quando si crea un punto di controllo, è necessario prendere in considerazione i seguenti problemi di sicurezza.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955684"
---
# <a name="control-point-security-considerations"></a>Considerazioni sulla sicurezza del punto di controllo

Quando si crea un punto di controllo, è necessario prendere in considerazione i seguenti problemi di sicurezza.

-   Per impostazione predefinita, tutte le ricerche di punti di controllo sono inviate con un valore TTL pari a 1. Ciò significa che vengono individuati solo i dispositivi all'interno della stessa subnet. È possibile configurare una durata (TTL) superiore nel registro di sistema.
-   La descrizione del dispositivo e del servizio di un dispositivo viene scaricata solo se è presente nello stesso dispositivo che ha inviato l'annuncio del dispositivo.
-   Un dispositivo viene inviato solo per le richieste di controllo e sottoscrizione se gli URL di controllo e sottoscrizione si trovano nello stesso dispositivo che ha inviato gli annunci del dispositivo.

 

 




