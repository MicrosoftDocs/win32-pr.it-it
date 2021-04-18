---
title: Bluetooth e BLOB
description: Bluetooth usa la struttura BLOB per passare o ricevere dati specifici del trasporto alla struttura WSAQUERYSET durante le chiamate a WSASetService o WSALookupService \ functions.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300342"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="e179c-107">Bluetooth e BLOB</span><span class="sxs-lookup"><span data-stu-id="e179c-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="e179c-108">Bluetooth usa la struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) per passare o ricevere dati specifici del trasporto alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante le chiamate alle funzioni [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* .</span><span class="sxs-lookup"><span data-stu-id="e179c-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="e179c-109">Per l'uso con Bluetooth e la funzione [**WSASetService**](bluetooth-and-wsasetservice.md) , è necessario che i membri della struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) dispongano delle impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e179c-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="e179c-110">Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ servizio del set di BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) utilizzata nel membro **pBlobData** , in byte.</span><span class="sxs-lookup"><span data-stu-id="e179c-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="e179c-111">Il membro **pBlobData** deve essere un puntatore a una struttura del [**\_ \_ servizio set BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="e179c-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="e179c-112">Per l'uso con Bluetooth e [WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), usare le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e179c-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="e179c-113">Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ dispositivo di query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilizzata nel membro **pBlobData** , in byte.</span><span class="sxs-lookup"><span data-stu-id="e179c-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="e179c-114">Il membro **pBlobData** deve essere un puntatore a una struttura di [**\_ \_ dispositivi di query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .</span><span class="sxs-lookup"><span data-stu-id="e179c-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="e179c-115">Per l'uso con Bluetooth e [WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), usare le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e179c-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="e179c-116">Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilizzata nel membro **pBlobData** , in byte.</span><span class="sxs-lookup"><span data-stu-id="e179c-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="e179c-117">Il membro **pBlobData** deve essere un puntatore a una struttura del [**\_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .</span><span class="sxs-lookup"><span data-stu-id="e179c-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="e179c-118">Per ulteriori informazioni, vedere la sezione Osservazioni nella pagina di riferimento relativa alla struttura del [**\_ set di \_ Servizi BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="e179c-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e179c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e179c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e179c-120">Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e179c-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="e179c-121">Bluetooth e WSALookupServiceBegin per l'individuazione del servizio</span><span class="sxs-lookup"><span data-stu-id="e179c-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="e179c-122">Bluetooth e WSASetService</span><span class="sxs-lookup"><span data-stu-id="e179c-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="e179c-123">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="e179c-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="e179c-124">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="e179c-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="e179c-125">**\_dispositivo di query BTH \_**</span><span class="sxs-lookup"><span data-stu-id="e179c-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="e179c-126">**\_servizio query \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="e179c-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="e179c-127">**\_servizio set \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="e179c-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="e179c-128">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="e179c-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="e179c-129">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="e179c-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="e179c-130">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="e179c-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 