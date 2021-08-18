---
description: L'32.dll Ws2 (e i protocolli a più livelli) chiameranno WSPCleanup una volta per ogni \_ chiamata di WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Pulizia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aefac8f58b7d6eed0380b7aa0e7759ff07e5af2a2762cde7d8e9bab445ca1fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741435"
---
# <a name="cleanup"></a>Pulizia

L'32.dll Ws2 (e i protocolli a più livelli) chiameranno \_ [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) una volta per ogni chiamata di [**WSPStartup.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) A ogni chiamata, **WSPCleanup** deve decrementare un contatore dei riferimenti per processo e quando il contatore raggiunge zero, il provider di servizi deve prepararsi per essere scaricato dalla memoria. Il primo ordine di business è quello di terminare la trasmissione di dati non inviati nei socket configurati per una chiusura normalmente. Successivamente, tutte le risorse del provider devono essere liberate. Il provider di servizi deve essere lasciato in uno stato in cui può essere reinizializzato immediatamente da una chiamata a **WSPStartup**.

 

 
