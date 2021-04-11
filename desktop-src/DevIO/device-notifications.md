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
# <a name="device-notifications"></a><span data-ttu-id="4d9b1-103">Notifiche del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d9b1-103">Device Notifications</span></span>

<span data-ttu-id="4d9b1-104">Il sistema trasmette un set di eventi di modifica del dispositivo predefiniti a tutte le applicazioni e i servizi.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="4d9b1-105">Non è necessario eseguire la registrazione per ricevere questi eventi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="4d9b1-106">Per informazioni dettagliate, vedere la sezione Osservazioni in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="4d9b1-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="4d9b1-107">Per specificare altri eventi che devono essere ricevuti dall'applicazione o dal servizio, usare la funzione **RegisterDeviceNotification** .</span><span class="sxs-lookup"><span data-stu-id="4d9b1-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="4d9b1-108">Quando un'applicazione o un servizio chiama [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), specifica anche la finestra che riceverà gli eventi di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="4d9b1-109">I servizi possono specificare un handle dello stato del servizio anziché un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="4d9b1-110">Se un servizio specifica il relativo handle di stato del servizio, il gestore di controllo del servizio riceverà gli eventi di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="4d9b1-111">Per ulteriori informazioni, vedere [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="4d9b1-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="4d9b1-112">Assicurarsi di gestire Plug and Play eventi del dispositivo il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="4d9b1-113">In caso contrario, il sistema potrebbe smettere di rispondere.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="4d9b1-114">Se il gestore eventi deve eseguire un'operazione che può bloccare l'esecuzione, ad esempio I/O, è consigliabile avviare un altro thread per eseguire l'operazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="4d9b1-115">Gli handle di notifica del dispositivo restituiti da [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devono essere chiusi chiamando la funzione [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="4d9b1-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d9b1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d9b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d9b1-117">Registrazione per la notifica del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d9b1-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
