---
description: Utilizzo di NSPStartup e NSPCleanup per l'inizializzazione e la pulizia del provider dello spazio dei nomi in Windows Sockets (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Inizializzazione e pulizia del provider dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526137"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Inizializzazione e pulizia del provider dello spazio dei nomi

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Come nel caso del trasporto SPI, un provider dello spazio dei nomi viene inizializzato con una chiamata a [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) e termina con una chiamata finale a [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Le chiamate alla funzione di avvio possono essere annidate, ma verranno confrontate con le chiamate corrispondenti alla funzione Cleanup. Un provider deve utilizzare il conteggio dei riferimenti per determinare quando si è verificata la chiamata finale a **NSPCleanup** .

 

 



