---
description: Specifica il numero massimo di messaggi di EAPOL-Start inviati.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311668"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="b8fc8-103">Elemento maxStart (OneX)</span><span class="sxs-lookup"><span data-stu-id="b8fc8-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="b8fc8-104">L'elemento maxStart (OneX) specifica il numero massimo di messaggi di EAPOL-Start inviati.</span><span class="sxs-lookup"><span data-stu-id="b8fc8-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="b8fc8-105">Una volta inviato il numero massimo di EAPOL-Start messaggi, il client presuppone che non sia presente alcun autenticatore nella rete.</span><span class="sxs-lookup"><span data-stu-id="b8fc8-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="b8fc8-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b8fc8-106">This element is optional.</span></span> <span data-ttu-id="b8fc8-107">Quando maxStart non viene specificato in un profilo, viene usato un valore di 3 messaggi.</span><span class="sxs-lookup"><span data-stu-id="b8fc8-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="b8fc8-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="b8fc8-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
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

<span data-ttu-id="b8fc8-109">L'elemento **maxStart** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b8fc8-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8fc8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8fc8-110">Requirements</span></span>



| <span data-ttu-id="b8fc8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8fc8-111">Requirement</span></span> | <span data-ttu-id="b8fc8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b8fc8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8fc8-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8fc8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b8fc8-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8fc8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8fc8-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8fc8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b8fc8-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8fc8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8fc8-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8fc8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8fc8-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b8fc8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b8fc8-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b8fc8-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b8fc8-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b8fc8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b8fc8-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b8fc8-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




