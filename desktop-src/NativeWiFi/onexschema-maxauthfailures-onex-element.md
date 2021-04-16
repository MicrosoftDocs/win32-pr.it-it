---
description: Specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Elemento maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529029"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="d841d-103">Elemento maxAuthFailures (OneX)</span><span class="sxs-lookup"><span data-stu-id="d841d-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="d841d-104">L'elemento maxAuthFailures (OneX) specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.</span><span class="sxs-lookup"><span data-stu-id="d841d-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="d841d-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d841d-105">This element is optional.</span></span> <span data-ttu-id="d841d-106">Quando maxAuthFailures non viene specificato in un profilo, viene utilizzato un valore di uno.</span><span class="sxs-lookup"><span data-stu-id="d841d-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="d841d-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="d841d-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d841d-108">L'elemento **maxAuthFailures** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d841d-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d841d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d841d-109">Requirements</span></span>



| <span data-ttu-id="d841d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d841d-110">Requirement</span></span> | <span data-ttu-id="d841d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d841d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d841d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d841d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d841d-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d841d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d841d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d841d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d841d-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d841d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d841d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d841d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d841d-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d841d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d841d-118">**OneX**</span><span class="sxs-lookup"><span data-stu-id="d841d-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="d841d-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d841d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d841d-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="d841d-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




