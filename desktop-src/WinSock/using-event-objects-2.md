---
description: Gli oggetti evento Windows Sockets sono semplici costrutti che è possibile creare e chiudere, impostare e cancellare, attendere e sottoporre a polling.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Utilizzo di oggetti evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306888"
---
# <a name="using-event-objects-windows-sockets-2"></a>Utilizzo di oggetti evento (Windows Sockets 2)

Gli oggetti evento Windows Sockets sono semplici costrutti che è possibile creare e chiudere, impostare e cancellare, attendere e sottoporre a polling. Il modello accettato prevede che i client creino un oggetto evento e forniscano l'handle come parametro (o come componente di una struttura di parametri) in funzioni quali [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Quando si è verificata la condizione candidata, il provider di servizi utilizza l'handle per impostare l'oggetto evento chiamando [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent). Nel frattempo, il client Winsock SPI può bloccarsi e attendere o eseguire il polling finché l'oggetto evento non viene impostato (segnalato). Il client può successivamente cancellare o reimpostare l'oggetto evento e usarlo di nuovo.

 

 
