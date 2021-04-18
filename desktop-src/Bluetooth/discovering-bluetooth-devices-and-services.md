---
title: Individuazione di dispositivi e servizi Bluetooth
description: Per semplificare l'individuazione di dispositivi e servizi Bluetooth, Windows mappa il protocollo SDP (Bluetooth Service Discovery Protocol) sulle interfacce dello spazio dei nomi Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, attività, individuazione di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/07/2020
ms.locfileid: "106299493"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="14086-104">Individuazione di dispositivi e servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="14086-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="14086-105">Per semplificare l'individuazione di dispositivi e servizi Bluetooth, Windows mappa il protocollo SDP (Bluetooth Service Discovery Protocol) sulle interfacce dello spazio dei nomi Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="14086-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="14086-106">Le funzioni primarie usate per questo mapping sono le funzioni [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="14086-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="14086-107">La struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) viene inoltre utilizzata insieme a queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="14086-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="14086-108">Poiché alcuni concetti e parametri del sistema SDP Bluetooth non eseguono necessariamente il mapping direttamente alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , è necessario prestare attenzione alla modalità di creazione e di utilizzo dei membri.</span><span class="sxs-lookup"><span data-stu-id="14086-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="14086-109">Per molte operazioni Bluetooth complesse, ad esempio la creazione di record SDP, viene usato il membro **lpBlob** di **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="14086-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="14086-110">Quando è necessario prestare particolare attenzione, viene descritta in modo specifico, ad esempio nelle pagine di riferimento come [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e altre.</span><span class="sxs-lookup"><span data-stu-id="14086-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="14086-111">È importante comprendere che la registrazione SDP è separata dal controllo socket.</span><span class="sxs-lookup"><span data-stu-id="14086-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="14086-112">Quando un'applicazione server è preparata ad accettare la connessione client, deve chiamare la funzione [**WSASetService**](bluetooth-and-wsasetservice.md) per registrare un record SDP Bluetooth corrispondente a tale servizio.</span><span class="sxs-lookup"><span data-stu-id="14086-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="14086-113">L'applicazione Bluetooth deve chiamare nuovamente la funzione **WSASetService** prima di chiudere, per annullare la registrazione del record SDP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="14086-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="14086-114">Quando si usano le funzioni di mapping descritte in questa pagina, \_ viene assegnato lo spazio dei nomi NS BTH.</span><span class="sxs-lookup"><span data-stu-id="14086-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="14086-115">Per ulteriori informazioni sull'individuazione di dispositivi e servizi, consultare le pagine di riferimento seguenti:</span><span class="sxs-lookup"><span data-stu-id="14086-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="14086-116">**Bluetooth e WSASetService**</span><span class="sxs-lookup"><span data-stu-id="14086-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="14086-117">**Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="14086-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="14086-118">**Bluetooth e WSALookupServiceBegin per l'individuazione del servizio**</span><span class="sxs-lookup"><span data-stu-id="14086-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="14086-119">**Bluetooth e WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="14086-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="14086-120">**Bluetooth e WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="14086-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="14086-121">**Bluetooth e BLOB**</span><span class="sxs-lookup"><span data-stu-id="14086-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="14086-122">**Bluetooth e WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="14086-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="14086-123">Per un esempio completo, è anche possibile scaricare l' [esempio di connessione Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) .</span><span class="sxs-lookup"><span data-stu-id="14086-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14086-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14086-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14086-125">Programmazione Bluetooth con Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="14086-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="14086-126">Esempio di connessione Bluetooth</span><span class="sxs-lookup"><span data-stu-id="14086-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




