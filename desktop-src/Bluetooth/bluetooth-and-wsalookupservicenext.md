---
title: Bluetooth e WSALookupServiceNext
description: Bluetooth usa la funzione WSALookupServiceNext per trovare la corrispondenza con le query specificate in una precedente chiamata a WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872578"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="7b7cf-106">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="7b7cf-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="7b7cf-107">Bluetooth usa la funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per trovare la corrispondenza con le query specificate in una precedente chiamata a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span><span class="sxs-lookup"><span data-stu-id="7b7cf-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="7b7cf-108">I risultati della funzione **WSALookupServiceNext** sono determinati dalle impostazioni definite nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata nella chiamata di funzione **WSALookupServiceBegin** iniziale.</span><span class="sxs-lookup"><span data-stu-id="7b7cf-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="7b7cf-109">I passaggi per la richiesta del dispositivo e l'individuazione dei servizi in Bluetooth sono sufficientemente diversi per meritare un trattamento distinto.</span><span class="sxs-lookup"><span data-stu-id="7b7cf-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="7b7cf-110">Per altre informazioni su Bluetooth e sulla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per le richieste dei dispositivi, vedere [Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="7b7cf-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="7b7cf-111">Per ulteriori informazioni su Bluetooth e sulla funzione **WSALookupServiceBegin** per l'individuazione del servizio, vedere [Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="7b7cf-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b7cf-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b7cf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7cf-113">Individuazione di dispositivi e servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7b7cf-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="7b7cf-114">Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7b7cf-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="7b7cf-115">Bluetooth e WSALookupServiceBegin per l'individuazione del servizio</span><span class="sxs-lookup"><span data-stu-id="7b7cf-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="7b7cf-116">Bluetooth e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="7b7cf-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="7b7cf-117">**\_servizio query \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="7b7cf-118">**connessione**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="7b7cf-119">**\_BTH sockaddr**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="7b7cf-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="7b7cf-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="7b7cf-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="7b7cf-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="7b7cf-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 