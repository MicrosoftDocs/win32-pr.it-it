---
title: Bluetooth e WSALookupServiceEnd
description: Bluetooth usa la funzione WSALookupServiceEnd per terminare una query avviata in una precedente chiamata a WSALookupServiceBegin ed eventualmente estesa nelle chiamate successive a WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963169"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="6e574-106">Bluetooth e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="6e574-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="6e574-107">Bluetooth usa la funzione [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) per terminare una query avviata in una precedente chiamata a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)ed eventualmente estesa nelle chiamate successive a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="6e574-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="6e574-108">La chiamata a **WSALookupServiceEnd** termina la query e pulisce il contesto.</span><span class="sxs-lookup"><span data-stu-id="6e574-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="6e574-109">I passaggi per la richiesta del dispositivo e l'individuazione dei servizi in Bluetooth sono sufficientemente diversi per meritare un trattamento distinto.</span><span class="sxs-lookup"><span data-stu-id="6e574-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="6e574-110">Per altre informazioni su Bluetooth e sulla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per le richieste dei dispositivi, vedere [Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="6e574-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="6e574-111">Per ulteriori informazioni su Bluetooth e sulla funzione **WSALookupServiceBegin** per l'individuazione del servizio, vedere [Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="6e574-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e574-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e574-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e574-113">Individuazione di dispositivi e servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="6e574-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="6e574-114">Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="6e574-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="6e574-115">Bluetooth e WSALookupServiceBegin per l'individuazione del servizio</span><span class="sxs-lookup"><span data-stu-id="6e574-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="6e574-116">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="6e574-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="6e574-117">**\_servizio query \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="6e574-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="6e574-118">**connessione**</span><span class="sxs-lookup"><span data-stu-id="6e574-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="6e574-119">**\_BTH sockaddr**</span><span class="sxs-lookup"><span data-stu-id="6e574-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="6e574-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="6e574-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="6e574-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="6e574-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="6e574-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="6e574-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="6e574-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="6e574-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="6e574-124">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6e574-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 