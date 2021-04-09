---
description: La maggior parte delle funzioni GetXbyY vengono convertite da WS2 \_32.dll a una sequenza WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd che usa uno di un set di GUID speciali come classe del servizio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Approccio di base per GetXbyY in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879230"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="171c0-103">Approccio di base per GetXbyY in SPI</span><span class="sxs-lookup"><span data-stu-id="171c0-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="171c0-104">La maggior parte delle funzioni **GetXbyY** vengono convertite da WS2 \_32.dll a una sequenza [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) che usa uno di un set di GUID speciali come classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="171c0-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="171c0-105">Questi GUID identificano il tipo di operazione **GetXbyY** da emulare.</span><span class="sxs-lookup"><span data-stu-id="171c0-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="171c0-106">La query è vincolata a tali rete che supportano AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="171c0-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="171c0-107">Ogni volta che una funzione **GetXbyY** restituisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , l' \_32.dll WS2 specificherà il \_ flag del BLOB restituito LUP \_ in **WSALookupServiceBegin** in modo che le informazioni desiderate vengano restituite da NSP.</span><span class="sxs-lookup"><span data-stu-id="171c0-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="171c0-108">Queste strutture devono essere modificate leggermente in quanto i puntatori contenuti in devono essere sostituiti da offset relativi all'inizio dei dati del BLOB.</span><span class="sxs-lookup"><span data-stu-id="171c0-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="171c0-109">Tutti i valori a cui fanno riferimento questi membri del puntatore devono, ovviamente, essere completamente contenuti all'interno del BLOB e tutte le stringhe sono ASCII.</span><span class="sxs-lookup"><span data-stu-id="171c0-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



