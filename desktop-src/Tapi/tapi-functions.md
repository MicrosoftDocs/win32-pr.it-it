---
description: Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area. Le informazioni per ogni funzione includono un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funzioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529214"
---
# <a name="tapi-functions"></a><span data-ttu-id="f324f-104">Funzioni TAPI</span><span class="sxs-lookup"><span data-stu-id="f324f-104">TAPI Functions</span></span>

<span data-ttu-id="f324f-105">Le sezioni seguenti contengono un elenco alfabetico di funzioni raggruppate per area.</span><span class="sxs-lookup"><span data-stu-id="f324f-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="f324f-106">Le informazioni per ogni funzione includono un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f324f-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="f324f-107">Funzioni di telefonia assistita</span><span class="sxs-lookup"><span data-stu-id="f324f-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="f324f-108">Funzioni Call Center</span><span class="sxs-lookup"><span data-stu-id="f324f-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="f324f-109">Funzioni del dispositivo linea</span><span class="sxs-lookup"><span data-stu-id="f324f-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="f324f-110">Funzioni del dispositivo telefonico</span><span class="sxs-lookup"><span data-stu-id="f324f-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="f324f-111">Per le funzioni TAPI categorizzate in base al livello di servizio e all'attività, vedere informazioni di [riferimento sulle funzioni TAPI Quick](tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f324f-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="f324f-112">Si noti che possono esistere limitazioni del provider di servizi riguardanti gli Stati effettivi in cui è possibile eseguire una funzione.</span><span class="sxs-lookup"><span data-stu-id="f324f-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="f324f-113">Le applicazioni devono verificare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) per determinare se una funzione è consentita o meno nello stato di chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="f324f-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



