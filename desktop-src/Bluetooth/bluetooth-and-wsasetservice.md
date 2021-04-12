---
title: Bluetooth e WSASetService
description: Bluetooth usa la funzione WSASetService per registrare o rimuovere un'istanza del servizio nello spazio dei nomi Bluetooth (NS \_ BTH) dal registro di sistema.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth e WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473246"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="56d30-106">Bluetooth e WSASetService</span><span class="sxs-lookup"><span data-stu-id="56d30-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="56d30-107">Bluetooth usa la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per registrare o rimuovere un'istanza del servizio nello spazio dei nomi Bluetooth (NS \_ BTH) dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="56d30-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="56d30-108">L'handle restituito da questa operazione può essere utilizzato solo per eliminare il servizio.</span><span class="sxs-lookup"><span data-stu-id="56d30-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="56d30-109">Bluetooth offre due metodi per la pubblicità dei servizi tramite la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="56d30-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="56d30-110">L'applicazione può fare in modo che il sistema annunci un semplice record di servizio Bluetooth SDP, costruito da membri standard nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="56d30-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="56d30-111">L'applicazione può fare in modo che il sistema annunci il proprio record SDP Bluetooth passando una struttura del [**\_ \_ servizio set BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) nel membro **lpBlob** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="56d30-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="56d30-112">Si tratta di un approccio più complesso.</span><span class="sxs-lookup"><span data-stu-id="56d30-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="56d30-113">I record SDP annunciati da [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) non vengono mantenuti dopo la chiusura del processo che li ha pubblicati.</span><span class="sxs-lookup"><span data-stu-id="56d30-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="56d30-114">L'uso di [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth prevede i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="56d30-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="56d30-115">Il parametro *lpqsRegInfo* è l'indirizzo della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) da registrare.</span><span class="sxs-lookup"><span data-stu-id="56d30-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="56d30-116">Il parametro *essOperation* è un'enumerazione che contiene una delle operazioni mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="56d30-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="56d30-117">Valore</span><span class="sxs-lookup"><span data-stu-id="56d30-117">Value</span></span>                  | <span data-ttu-id="56d30-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56d30-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d30-119">\_Registro RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="56d30-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="56d30-120">Inizia a annunciare il servizio alle radio remote che eseguono query usando il protocollo Bluetooth SDP.</span><span class="sxs-lookup"><span data-stu-id="56d30-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="56d30-121">RNRSERVICE \_ annullare la registrazione</span><span class="sxs-lookup"><span data-stu-id="56d30-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="56d30-122">Non valido.</span><span class="sxs-lookup"><span data-stu-id="56d30-122">Not valid.</span></span> <span data-ttu-id="56d30-123">Restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="56d30-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="56d30-124">eliminazione di RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="56d30-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="56d30-125">Interrompe la pubblicità del servizio.</span><span class="sxs-lookup"><span data-stu-id="56d30-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="56d30-126">Gli handle del servizio individuati durante una chiamata [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) non sono compatibili con l' \_ operazione di eliminazione RNRSERVICE.</span><span class="sxs-lookup"><span data-stu-id="56d30-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="56d30-127">Il parametro *dwControlFlags* è riservato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="56d30-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="56d30-128">Per altre informazioni e per un elenco delle opzioni dei Socket Bluetooth, vedere [Opzioni per Bluetooth e socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="56d30-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56d30-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56d30-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d30-130">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="56d30-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 