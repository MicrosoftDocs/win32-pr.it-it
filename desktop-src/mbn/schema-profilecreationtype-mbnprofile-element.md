---
description: Contiene informazioni sull'autore del profilo.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129570"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="69008-103">Elemento ProfileCreationType (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="69008-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="69008-104">L'elemento **ProfileCreationType (MBNProfile)** contiene informazioni sull'autore del profilo.</span><span class="sxs-lookup"><span data-stu-id="69008-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="69008-105">Questo elemento può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69008-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="69008-106">Valore</span><span class="sxs-lookup"><span data-stu-id="69008-106">Value</span></span>                 | <span data-ttu-id="69008-107">Significato</span><span class="sxs-lookup"><span data-stu-id="69008-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69008-108">"UserProvisioned"</span><span class="sxs-lookup"><span data-stu-id="69008-108">"UserProvisioned"</span></span>     | <span data-ttu-id="69008-109">Questo profilo viene creato dalle informazioni fornite dall'utente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69008-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="69008-110">"AdminProvisioned"</span><span class="sxs-lookup"><span data-stu-id="69008-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="69008-111">Questo profilo viene creato dagli amministratori IT e distribuito agli utenti.</span><span class="sxs-lookup"><span data-stu-id="69008-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="69008-112">"OperatorProvisioned"</span><span class="sxs-lookup"><span data-stu-id="69008-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="69008-113">Questo profilo viene creato da un operatore di rete e distribuito agli utenti.</span><span class="sxs-lookup"><span data-stu-id="69008-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="69008-114">"DeviceProvisioned"</span><span class="sxs-lookup"><span data-stu-id="69008-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="69008-115">Questo profilo viene creato dal servizio Mobile Broadband usando le informazioni archiviate nel contesto con provisioning del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69008-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="69008-116">Si tratta di un elemento facoltativo.</span><span class="sxs-lookup"><span data-stu-id="69008-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="69008-117">L'elemento **ProfileCreationType** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="69008-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="69008-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69008-118">Requirements</span></span>



| <span data-ttu-id="69008-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="69008-119">Requirement</span></span> | <span data-ttu-id="69008-120">Valore</span><span class="sxs-lookup"><span data-stu-id="69008-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="69008-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69008-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69008-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69008-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="69008-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69008-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69008-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69008-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="69008-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69008-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="69008-126">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="69008-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="69008-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="69008-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="69008-128">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="69008-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="69008-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="69008-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




