---
description: Il sistema trasmette un set di eventi di modifica del dispositivo predefiniti a tutte le applicazioni e i servizi.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notifiche del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12186ab6349057258d723f7e690e889b7e79af4abe47f714055599cb6f648333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636621"
---
# <a name="device-notifications"></a>Notifiche del dispositivo

Il sistema trasmette un set di eventi di modifica del dispositivo predefiniti a tutte le applicazioni e i servizi. Non è necessario registrarsi per ricevere questi eventi predefiniti. Per informazioni dettagliate, vedere la sezione Osservazioni in [**RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Per specificare altri eventi che l'applicazione o il servizio deve ricevere, usare la **funzione RegisterDeviceNotification.**

Quando un'applicazione o un servizio chiama [**RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)specifica anche la finestra che riceverà gli eventi di notifica. I servizi possono specificare un handle di stato del servizio anziché un handle di finestra. Se un servizio specifica l'handle di stato del servizio, il gestore di controllo del servizio riceverà gli eventi di notifica. Per altre informazioni, vedere [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Assicurarsi di gestire gli Plug and Play del dispositivo il più rapidamente possibile. In caso contrario, il sistema potrebbe non rispondere. Se il gestore eventi deve eseguire un'operazione che può bloccare l'esecuzione (ad esempio I/O), è meglio avviare un altro thread per eseguire l'operazione in modo asincrono.

Gli handle di notifica del dispositivo restituiti da [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devono essere chiusi chiamando la [**funzione UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando non sono più necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione per la notifica del dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
