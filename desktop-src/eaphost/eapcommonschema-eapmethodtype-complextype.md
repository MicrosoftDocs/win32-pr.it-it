---
title: Tipo complesso EapMethodType
description: Definisce gli elementi che identificano in modo univoco un solo tipo di metodo EAP, VendorId, VendorType e autorizzazione.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741842"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="14208-104">Tipo complesso EapMethodType</span><span class="sxs-lookup"><span data-stu-id="14208-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="14208-105">Il tipo complesso **EapMethodType** definisce gli elementi che identificano in modo univoco un singolo metodo EAP, ovvero [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)e [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="14208-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="14208-106">Il [**tipo**](eapcommonschema-type-eapmethodtype-element.md) e l' [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md) sono elementi obbligatori, mentre [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) sono obbligatori solo quando l'elemento **Type** è 254 (un metodo EAP espanso).</span><span class="sxs-lookup"><span data-stu-id="14208-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="14208-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="14208-107">Child elements</span></span>



| <span data-ttu-id="14208-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="14208-108">Element</span></span>                                                                | <span data-ttu-id="14208-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="14208-109">Type</span></span>         | <span data-ttu-id="14208-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14208-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14208-111">**AuthorId**</span><span class="sxs-lookup"><span data-stu-id="14208-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="14208-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="14208-112">unsignedInt</span></span>  | <span data-ttu-id="14208-113">Si riferisce all'autore del metodo.</span><span class="sxs-lookup"><span data-stu-id="14208-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="14208-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="14208-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="14208-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="14208-115">unsignedByte</span></span> | <span data-ttu-id="14208-116">Si riferisce al tipo di metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="14208-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="14208-117">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="14208-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="14208-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="14208-118">unsignedInt</span></span>  | <span data-ttu-id="14208-119">Fa riferimento al fornitore che ha definito il metodo, se l'elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso).</span><span class="sxs-lookup"><span data-stu-id="14208-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="14208-120">[**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="14208-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="14208-121">**VendorType**</span><span class="sxs-lookup"><span data-stu-id="14208-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="14208-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="14208-122">unsignedInt</span></span>  | <span data-ttu-id="14208-123">È il tipo definito dal fornitore per il metodo.</span><span class="sxs-lookup"><span data-stu-id="14208-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="14208-124">[**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="14208-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="14208-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="14208-125">Remarks</span></span>

<span data-ttu-id="14208-126">Gli elementi [**autorizzazioned**](eapcommonschema-authorid-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.</span><span class="sxs-lookup"><span data-stu-id="14208-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="14208-127">Gli elementi [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md), [**tipo**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) e [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) sono ciascuno un numero univoco emesso da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="14208-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="14208-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14208-128">Requirements</span></span>



| <span data-ttu-id="14208-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="14208-129">Requirement</span></span> | <span data-ttu-id="14208-130">Valore</span><span class="sxs-lookup"><span data-stu-id="14208-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14208-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14208-131">Minimum supported client</span></span><br/> | <span data-ttu-id="14208-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14208-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14208-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14208-133">Minimum supported server</span></span><br/> | <span data-ttu-id="14208-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14208-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14208-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14208-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14208-136">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="14208-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="14208-137">Schema eapcommon</span><span class="sxs-lookup"><span data-stu-id="14208-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





