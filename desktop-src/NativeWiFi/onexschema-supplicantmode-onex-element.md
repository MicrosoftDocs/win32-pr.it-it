---
description: Specifica il metodo di trasmissione utilizzato per EAPOL-Start messaggi.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311665"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="b3e8a-103">Elemento supplicantMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="b3e8a-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="b3e8a-104">L'elemento supplicantMode (OneX) specifica il metodo di trasmissione utilizzato per EAPOL-Start messaggi.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="b3e8a-105">Nella tabella seguente sono descritti i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="b3e8a-106">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e8a-106">Value</span></span>               | <span data-ttu-id="b3e8a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e8a-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e8a-108">inhibitTransmission</span><span class="sxs-lookup"><span data-stu-id="b3e8a-108">inhibitTransmission</span></span> | <span data-ttu-id="b3e8a-109">EAPOL-Start messaggi non vengono trasmessi.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="b3e8a-110">Valido solo per i profili LAN cablati.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="b3e8a-111">includeLearning</span><span class="sxs-lookup"><span data-stu-id="b3e8a-111">includeLearning</span></span>     | <span data-ttu-id="b3e8a-112">Il client determina quando inviare pacchetti di EAPOL-Start in base alla funzionalità di rete.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="b3e8a-113">EAPOL-Start messaggi vengono inviati solo quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="b3e8a-114">Valido solo per i profili LAN cablati.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="b3e8a-115">compliant</span><span class="sxs-lookup"><span data-stu-id="b3e8a-115">compliant</span></span>           | <span data-ttu-id="b3e8a-116">EAPOL-Start messaggi vengono trasmessi come specificato da 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="b3e8a-117">Valido per i profili LAN cablati e wireless.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="b3e8a-118">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-118">This element is optional.</span></span> <span data-ttu-id="b3e8a-119">Quando supplicantMode non viene specificato in un profilo, viene utilizzato un valore di `compliant` per i profili LAN cablati e wireless.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="b3e8a-120">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b3e8a-121">L'elemento **supplicantMode** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e8a-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e8a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3e8a-122">Requirements</span></span>



| <span data-ttu-id="b3e8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e8a-123">Requirement</span></span> | <span data-ttu-id="b3e8a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e8a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3e8a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e8a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e8a-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3e8a-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3e8a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e8a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e8a-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3e8a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3e8a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3e8a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3e8a-130">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3e8a-131">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b3e8a-132">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3e8a-133">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




