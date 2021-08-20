---
title: Considerazioni sulla sicurezza dei punti di controllo
description: Quando si crea un punto di controllo, è necessario prendere in considerazione i problemi di sicurezza seguenti.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126008"
---
# <a name="control-point-security-considerations"></a>Considerazioni sulla sicurezza dei punti di controllo

Quando si crea un punto di controllo, è necessario prendere in considerazione i problemi di sicurezza seguenti.

-   Per impostazione predefinita, tutte le ricerche nei punti di controllo vengono inviate con una durata (TTL) di 1. Ciò significa che vengono individuati solo i dispositivi all'interno della stessa subnet. È possibile configurare una durata (TTL) superiore nel Registro di sistema.
-   La descrizione del dispositivo e del servizio di un dispositivo viene scaricata solo se è presente nello stesso dispositivo che ha inviato l'annuncio del dispositivo.
-   A un dispositivo vengono inviati il controllo e le richieste di sottoscrizione solo se gli URL di controllo e sottoscrizione sono nello stesso dispositivo che ha inviato gli annunci del dispositivo.

 

 




