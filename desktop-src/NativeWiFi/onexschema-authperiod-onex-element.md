---
description: Specifica il periodo di tempo massimo, in secondi, durante il quale un client attende una risposta dall'autenticatore.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Elemento authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049986"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="87f71-103">Elemento authPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="87f71-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="87f71-104">L'elemento authPeriod (OneX) specifica la quantità massima di tempo, in secondi, in cui un client attende una risposta dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="87f71-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="87f71-105">Se non viene ricevuta una risposta entro il periodo specificato, il client presuppone che non sia presente alcun autenticatore nella rete.</span><span class="sxs-lookup"><span data-stu-id="87f71-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="87f71-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87f71-106">This element is optional.</span></span> <span data-ttu-id="87f71-107">Quando authPeriod non viene specificato in un profilo, viene utilizzato un valore di 18 secondi.</span><span class="sxs-lookup"><span data-stu-id="87f71-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="87f71-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="87f71-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
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

<span data-ttu-id="87f71-109">L'elemento **authPeriod** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="87f71-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f71-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87f71-110">Requirements</span></span>



| <span data-ttu-id="87f71-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f71-111">Requirement</span></span> | <span data-ttu-id="87f71-112">Valore</span><span class="sxs-lookup"><span data-stu-id="87f71-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87f71-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f71-113">Minimum supported client</span></span><br/> | <span data-ttu-id="87f71-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87f71-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87f71-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f71-115">Minimum supported server</span></span><br/> | <span data-ttu-id="87f71-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87f71-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87f71-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87f71-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="87f71-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="87f71-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="87f71-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="87f71-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="87f71-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="87f71-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="87f71-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="87f71-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




