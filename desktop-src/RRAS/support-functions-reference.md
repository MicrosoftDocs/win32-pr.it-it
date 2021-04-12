---
title: Informazioni di riferimento sulle funzioni di supporto
description: Le funzioni seguenti vengono fornite ai protocolli di routing da Gestione router.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Protocollo routing interfaccia RRAS, funzioni di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473814"
---
# <a name="support-functions-reference"></a><span data-ttu-id="b7a7e-104">Informazioni di riferimento sulle funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="b7a7e-104">Support Functions Reference</span></span>

<span data-ttu-id="b7a7e-105">Le funzioni seguenti vengono fornite ai protocolli di routing da Gestione router.</span><span class="sxs-lookup"><span data-stu-id="b7a7e-105">The following functions are provided to routing protocols by the router manager.</span></span> <span data-ttu-id="b7a7e-106">Quando Gestione router chiama la funzione [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementata dal protocollo di routing), gestione router passa il protocollo di routing a una struttura di [**\_ funzioni di supporto**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) che contiene i puntatori alle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7a7e-106">When the router manager calls the [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) function (implemented by the routing protocol), the router manager passes the routing protocol a [**SUPPORT\_FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) structure containing pointers to these functions:</span></span>

<span data-ttu-id="b7a7e-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span></span>

<span data-ttu-id="b7a7e-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7a7e-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span></span>

 

 