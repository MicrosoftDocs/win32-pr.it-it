---
description: Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Timer stato chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221b0cd1182e59304b13d6d276bece9f755c5dacc0215218ff5ee23aea09e532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869995"
---
# <a name="call-state-timer"></a>Timer stato chiamata

Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni. Questa situazione può essere gravosa se l'applicazione monitora un numero elevato di chiamate e se sono presenti più applicazioni, possibilmente su più server, può essere necessario che gestisca tutti i timer nelle stesse chiamate. È quindi più opportuno che il tempo di stato delle chiamate sia gestito dal server.

Il **membro tStateEntryTime** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) consente di sincronizzazione delle chiamate negli stati da notificare. Il membro (di tipo **SYSTIME**) indica l'ora in cui è stato immesso lo stato corrente.

 

 



