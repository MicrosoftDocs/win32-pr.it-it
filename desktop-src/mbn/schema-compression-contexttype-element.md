---
description: Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Elemento Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879406"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="c259d-103">Elemento Compression (contextType)</span><span class="sxs-lookup"><span data-stu-id="c259d-103">Compression (contextType) Element</span></span>

<span data-ttu-id="c259d-104">L'elemento **Compression (ContextType)** specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="c259d-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="c259d-105">Questo elemento può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c259d-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="c259d-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c259d-106">Value</span></span>     | <span data-ttu-id="c259d-107">Significato</span><span class="sxs-lookup"><span data-stu-id="c259d-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="c259d-108">Abilita</span><span class="sxs-lookup"><span data-stu-id="c259d-108">"ENABLE"</span></span>  | <span data-ttu-id="c259d-109">Verrà utilizzata la compressione.</span><span class="sxs-lookup"><span data-stu-id="c259d-109">Compression will be used.</span></span>     |
| <span data-ttu-id="c259d-110">DISABILITARE</span><span class="sxs-lookup"><span data-stu-id="c259d-110">"DISABLE"</span></span> | <span data-ttu-id="c259d-111">Non verrà utilizzata la compressione.</span><span class="sxs-lookup"><span data-stu-id="c259d-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="c259d-112">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c259d-112">This element is optional.</span></span> <span data-ttu-id="c259d-113">Se questo elemento non è specificato, il sistema Mobile Broadband non utilizzerà la compressione.</span><span class="sxs-lookup"><span data-stu-id="c259d-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c259d-114">L'elemento **Compression** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c259d-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c259d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c259d-115">Requirements</span></span>



| <span data-ttu-id="c259d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c259d-116">Requirement</span></span> | <span data-ttu-id="c259d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c259d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c259d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c259d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c259d-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c259d-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c259d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c259d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c259d-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c259d-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c259d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c259d-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c259d-123">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c259d-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c259d-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="c259d-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="c259d-125">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c259d-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c259d-126">**Contesto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="c259d-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




