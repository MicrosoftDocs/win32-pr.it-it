---
description: PNRP utilizza la struttura WSAQUERYSET insieme a diverse funzioni per semplificare la risoluzione dei nomi e l'enumerazione di nomi e cloud.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314740"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="0222a-103">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="0222a-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="0222a-104">PNRP utilizza la struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) insieme a diverse funzioni per semplificare la risoluzione dei nomi e l'enumerazione di nomi e cloud.</span><span class="sxs-lookup"><span data-stu-id="0222a-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="0222a-105">Per le definizioni complete delle funzioni [**WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, vedere le rispettive definizioni nella documentazione dell'API di Windows Sockets 2 in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0222a-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="0222a-106">WSAQUERYSET e WSASetService</span><span class="sxs-lookup"><span data-stu-id="0222a-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="0222a-107">La funzione [**WSASetService**](winsock-nsp-reference-links.md) usa la struttura **WSAQUERYSET** per registrare o rimuovere i nomi dei peer.</span><span class="sxs-lookup"><span data-stu-id="0222a-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="0222a-108">La pagina [PNRP e WSASetService](pnrp-and-wsasetservice.md) illustra come usare la struttura **WSAQUERYSET** con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0222a-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="0222a-109">WSAQUERYSET e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="0222a-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="0222a-110">La struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) viene utilizzata ampiamente con le funzioni **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="0222a-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="0222a-111">Le pagine di riferimento seguenti illustrano in dettaglio il modo in cui queste funzioni usano la struttura **WSAQUERYSET** :</span><span class="sxs-lookup"><span data-stu-id="0222a-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="0222a-112">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="0222a-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="0222a-113">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="0222a-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="0222a-114">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="0222a-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="0222a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0222a-115">Requirements</span></span>



| <span data-ttu-id="0222a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0222a-116">Requirement</span></span> | <span data-ttu-id="0222a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0222a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0222a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0222a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0222a-119">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0222a-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0222a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0222a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0222a-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0222a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0222a-122">Versione</span><span class="sxs-lookup"><span data-stu-id="0222a-122">Version</span></span><br/>                  | <span data-ttu-id="0222a-123">Windows XP con SP1 con Advanced Networking Pack per Windows XP</span><span class="sxs-lookup"><span data-stu-id="0222a-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="0222a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0222a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0222a-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="0222a-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0222a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0222a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0222a-127">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="0222a-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="0222a-128">PNRP e WSASetService</span><span class="sxs-lookup"><span data-stu-id="0222a-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




