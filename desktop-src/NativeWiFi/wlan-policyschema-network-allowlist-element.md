---
description: Definisce una rete consentita.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Elemento Network (Consenti)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318257"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="1c2af-103">Elemento Network (Consenti)</span><span class="sxs-lookup"><span data-stu-id="1c2af-103">network (allowList) Element</span></span>

<span data-ttu-id="1c2af-104">L'elemento Network (allowname) definisce una rete consentita.</span><span class="sxs-lookup"><span data-stu-id="1c2af-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="1c2af-105">Un computer deve essere autorizzato a connettersi a una rete consentita.</span><span class="sxs-lookup"><span data-stu-id="1c2af-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="1c2af-106">L'elemento **Network** è definito dall'elemento [**Allow**](wlan-policyschema-allowlist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1c2af-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2af-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c2af-107">Requirements</span></span>



| <span data-ttu-id="1c2af-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2af-108">Requirement</span></span> | <span data-ttu-id="1c2af-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1c2af-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c2af-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c2af-110">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2af-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c2af-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c2af-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c2af-112">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2af-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c2af-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c2af-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c2af-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c2af-115">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1c2af-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1c2af-116">**Elenco serializzazione**</span><span class="sxs-lookup"><span data-stu-id="1c2af-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="1c2af-117">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="1c2af-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1c2af-118">**Allow (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="1c2af-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




