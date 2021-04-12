---
description: Specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226193"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="57cbe-103">Elemento AutoConnectOnInternet (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="57cbe-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="57cbe-104">L'elemento **AutoConnectOnInternet (MBNProfile)** specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.</span><span class="sxs-lookup"><span data-stu-id="57cbe-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="57cbe-105">Se è impostato su **false**, la logica di connessione automatica del servizio Mobile Broadband non verrà usata se per il sistema sono disponibili altre connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="57cbe-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="57cbe-106">Se è impostato su **true**, il servizio Mobile Broadband tenterà di connettere automaticamente il dispositivo alla rete in base all'impostazione di connessione automatica definita nell'elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="57cbe-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="57cbe-107">**Windows 8 e versioni successive:** Questo elemento è deprecato.</span><span class="sxs-lookup"><span data-stu-id="57cbe-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="57cbe-108">Usare invece il metodo [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) con il parametro *Property* impostato su **file WCM \_ Global \_ Property \_ minimizzi \_ policy** .</span><span class="sxs-lookup"><span data-stu-id="57cbe-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="57cbe-109">L'elemento **AutoConnectOnInternet** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="57cbe-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cbe-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cbe-110">Requirements</span></span>



| <span data-ttu-id="57cbe-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cbe-111">Requirement</span></span> | <span data-ttu-id="57cbe-112">Valore</span><span class="sxs-lookup"><span data-stu-id="57cbe-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="57cbe-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cbe-113">Minimum supported client</span></span><br/> | <span data-ttu-id="57cbe-114">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="57cbe-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="57cbe-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cbe-115">Minimum supported server</span></span><br/> | <span data-ttu-id="57cbe-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="57cbe-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="57cbe-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cbe-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="57cbe-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="57cbe-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="57cbe-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="57cbe-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="57cbe-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="57cbe-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="57cbe-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="57cbe-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

