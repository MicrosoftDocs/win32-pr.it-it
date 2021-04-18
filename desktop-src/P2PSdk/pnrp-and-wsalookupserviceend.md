---
description: PNRP utilizza la funzione WSALookupServiceEnd per eseguire le operazioni seguenti.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314741"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="c2217-103">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="c2217-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="c2217-104">PNRP utilizza la funzione [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2217-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="c2217-105">Termina una query avviata in una chiamata precedente a [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="c2217-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="c2217-106">Sbloccare una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per arrestare la ricerca</span><span class="sxs-lookup"><span data-stu-id="c2217-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="c2217-107">Una chiamata a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) termina una query e pulisce il contesto.</span><span class="sxs-lookup"><span data-stu-id="c2217-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="c2217-108">L'handle ottenuto da una chiamata a **WSALookupServiceBegin** deve essere passato come parametro a **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="c2217-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="c2217-109">Per ulteriori informazioni su PNRP e la funzione [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , vedere [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="c2217-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2217-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2217-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2217-111">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="c2217-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="c2217-112">Codici di errore PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="c2217-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="c2217-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="c2217-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



