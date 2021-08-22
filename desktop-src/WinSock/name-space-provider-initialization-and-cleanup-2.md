---
description: Uso di NSPStartup e NSPCleanup per l'inizializzazione e la pulizia del provider dello spazio dei nomi in Windows Sockets (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Inizializzazione e pulizia del provider dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4007533bb1456268ee3a1110da4681a7041a56ed80c0d9a522790c8a0c9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612981"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Inizializzazione e pulizia del provider dello spazio dei nomi

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Come nel caso del trasporto SPI, un provider dello spazio dei nomi viene inizializzato con una chiamata a [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) e viene terminato con una chiamata finale a [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Le chiamate alla funzione di avvio possono essere annidate, ma verranno abbinate dalle chiamate corrispondenti alla funzione cleanup. Un provider deve usare il conteggio dei riferimenti per determinare quando si è verificata la chiamata finale a **NSPCleanup.**

 

 



