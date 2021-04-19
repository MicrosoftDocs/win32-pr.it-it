---
description: Specifica l'intervallo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Elemento heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311674"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="e5b11-103">Elemento heldPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="e5b11-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="e5b11-104">L'elemento heldPeriod (OneX) specifica il periodo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e5b11-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="e5b11-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e5b11-105">This element is optional.</span></span> <span data-ttu-id="e5b11-106">Quando heldPeriod non viene specificato in un profilo, viene utilizzato un valore di 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="e5b11-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="e5b11-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="e5b11-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e5b11-108">L'elemento **heldPeriod** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b11-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b11-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5b11-109">Requirements</span></span>



| <span data-ttu-id="e5b11-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b11-110">Requirement</span></span> | <span data-ttu-id="e5b11-111">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b11-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5b11-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b11-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b11-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5b11-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5b11-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b11-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b11-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5b11-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5b11-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5b11-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5b11-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e5b11-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e5b11-118">**OneX**</span><span class="sxs-lookup"><span data-stu-id="e5b11-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="e5b11-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e5b11-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e5b11-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="e5b11-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




