---
description: Un servizio che è un'applicazione console può registrare un gestore di controllo della console per ricevere una notifica quando un utente si disconnette.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Ricezione di eventi in un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe2312989208d5b6587067e64f10401c32229c2b19a7b4846163444576e63ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003709"
---
# <a name="receiving-events-in-a-service"></a>Ricezione di eventi in un servizio

Un servizio che è un'applicazione console può registrare un gestore di [controllo della console](/windows/console/console-control-handlers) per ricevere una notifica quando un utente si disconnette. Tuttavia, non viene inviato alcun evento della console quando un utente interattivo esegue l'accesso. Per informazioni sulla ricezione di notifiche quando un utente accede, vedere [Creazione di un pacchetto di notifica Winlogon.](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package)

Il sistema trasmette gli eventi di modifica del dispositivo a tutti i servizi. Questi eventi possono essere ricevuti da un servizio in una routine della finestra o nel relativo gestore di controllo del servizio. Per specificare gli eventi che il servizio deve ricevere, usare la [**funzione RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

Assicurarsi di gestire gli Plug and Play del dispositivo nel più breve tempo possibile. In caso contrario, il sistema potrebbe non rispondere. Se il gestore eventi deve eseguire un'operazione che potrebbe bloccare l'esecuzione (ad esempio I/O), è meglio avviare un altro thread per eseguire l'operazione in modo asincrono.

Quando un servizio chiama [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa), il servizio specifica anche un handle di finestra o un handle di stato del servizio. Se un servizio specifica un handle di finestra, la routine della finestra riceve gli eventi di notifica. Se un servizio specifica l'handle di stato del servizio, il gestore di controllo del servizio riceve gli eventi di notifica. Per altre informazioni, vedere [**HandlerEx.**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)

Gli handle di notifica del dispositivo restituiti da [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) devono essere chiusi chiamando [**la funzione UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) quando non sono più necessari.

 

 
