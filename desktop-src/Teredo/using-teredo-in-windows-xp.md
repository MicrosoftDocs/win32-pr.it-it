---
title: Utilizzo di Teredo in Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'Altre informazioni su: uso di Teredo in Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058268"
---
# <a name="using-teredo-in-windows-xp"></a>Utilizzo di Teredo in Windows XP

Per utilizzare il client Teredo o l'inoltro specifico dell'host nei computer che eseguono Windows XP con Service Pack 1 (SP1) con Advanced Networking Pack, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) o Windows Server 2003 con Service Pack 2 (SP2), uno sviluppatore di applicazioni deve eseguire le operazioni seguenti:

-   Assicurarsi che l'applicazione sia compatibile con IPv6 usando nuovi elementi di programmazione Windows Sockets 2 (funzioni e strutture) che supportano sia IPv4 che IPv6. Per ulteriori informazioni, vedere la [Guida a IPv6 per le applicazioni Windows Sockets](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   Abilitare l'uso di Teredo nell'applicazione impostando l'opzione del socket del livello di \_ protezione IPv6 \_ Windows Sockets sul livello di protezione \_ \_ senza restrizioni. Per ulteriori informazioni, vedere [using IPv6 \_ Protection \_ Level](/previous-versions/aa916826(v=msdn.10)). È anche possibile impostare questa opzione tramite la classe [System .NET. sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework.
-   Creare un'eccezione affinché il Windows Firewall consenta il traffico Teredo in entrata non richiesto. Utilizzare le API [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page) per creare un'eccezione di porta per la porta UDP assegnata per il traffico Teredo. Per ulteriori informazioni ed esempi che illustrano in dettaglio le considerazioni di sicurezza e traffico necessarie per Teredo, vedere [utilizzo di Teredo](using-teredo.md).

Per assicurarsi che Teredo sia disponibile per l'utilizzo durante l'esecuzione dell'applicazione, gli sviluppatori di applicazioni devono eseguire le operazioni seguenti durante il processo di installazione dell'applicazione:

-   Installare IPv6 con il comando **netsh interface ipv6 install** . Windows Firewall protegge il computer dell'utente dal traffico IPv6 in ingresso non richiesto nello stesso modo del traffico IPv4.
-   Abilitare Teredo con il comando **netsh interface ipv6 set Teredo client** .

Facoltativamente, è possibile verificare se IPv6 è installato ogni volta che viene eseguita l'applicazione e installare IPv6 e abilitare Teredo in base alle esigenze. È inoltre necessario informare l'utente che è in corso l'installazione di IPv6 e che Teredo è abilitato.

 

 
