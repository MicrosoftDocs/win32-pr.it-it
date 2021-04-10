---
description: Specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966661"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="570a4-103">Elemento ConnectionMode (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="570a4-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="570a4-104">L'elemento **ConnectionMode (MBNProfile)** specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.</span><span class="sxs-lookup"><span data-stu-id="570a4-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="570a4-105">Questo elemento può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="570a4-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="570a4-106">Valore</span><span class="sxs-lookup"><span data-stu-id="570a4-106">Value</span></span>       | <span data-ttu-id="570a4-107">Significato</span><span class="sxs-lookup"><span data-stu-id="570a4-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="570a4-108">manuale</span><span class="sxs-lookup"><span data-stu-id="570a4-108">"manual"</span></span>    | <span data-ttu-id="570a4-109">Non connettersi mai automaticamente alla rete.</span><span class="sxs-lookup"><span data-stu-id="570a4-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="570a4-110">auto</span><span class="sxs-lookup"><span data-stu-id="570a4-110">"auto"</span></span>      | <span data-ttu-id="570a4-111">Connettersi sempre automaticamente alla rete.</span><span class="sxs-lookup"><span data-stu-id="570a4-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="570a4-112">"auto-Home"</span><span class="sxs-lookup"><span data-stu-id="570a4-112">"auto-home"</span></span> | <span data-ttu-id="570a4-113">Connettersi automaticamente alla rete tranne che in una rete in roaming.</span><span class="sxs-lookup"><span data-stu-id="570a4-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="570a4-114">Questo elemento può avere un massimo di un'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="570a4-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="570a4-115">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="570a4-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="570a4-116">L'elemento **ConnectionMode** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="570a4-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="570a4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="570a4-117">Requirements</span></span>



| <span data-ttu-id="570a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="570a4-118">Requirement</span></span> | <span data-ttu-id="570a4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="570a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="570a4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="570a4-121">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="570a4-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="570a4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="570a4-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="570a4-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="570a4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="570a4-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="570a4-125">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="570a4-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="570a4-126">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="570a4-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="570a4-127">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="570a4-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="570a4-128">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="570a4-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




