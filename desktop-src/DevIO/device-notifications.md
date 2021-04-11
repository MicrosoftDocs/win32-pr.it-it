---
description: Il sistema trasmette un set di eventi di modifica del dispositivo predefiniti a tutte le applicazioni e i servizi.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notifiche del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127294"
---
# <a name="device-notifications"></a>Notifiche del dispositivo

Il sistema trasmette un set di eventi di modifica del dispositivo predefiniti a tutte le applicazioni e i servizi. Non è necessario eseguire la registrazione per ricevere questi eventi predefiniti. Per informazioni dettagliate, vedere la sezione Osservazioni in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) . Per specificare altri eventi che devono essere ricevuti dall'applicazione o dal servizio, usare la funzione **RegisterDeviceNotification** .

Quando un'applicazione o un servizio chiama [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), specifica anche la finestra che riceverà gli eventi di notifica. I servizi possono specificare un handle dello stato del servizio anziché un handle di finestra. Se un servizio specifica il relativo handle di stato del servizio, il gestore di controllo del servizio riceverà gli eventi di notifica. Per ulteriori informazioni, vedere [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Assicurarsi di gestire Plug and Play eventi del dispositivo il più rapidamente possibile. In caso contrario, il sistema potrebbe smettere di rispondere. Se il gestore eventi deve eseguire un'operazione che può bloccare l'esecuzione, ad esempio I/O, è consigliabile avviare un altro thread per eseguire l'operazione in modo asincrono.

Gli handle di notifica del dispositivo restituiti da [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devono essere chiusi chiamando la funzione [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando non sono più necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione per la notifica del dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
