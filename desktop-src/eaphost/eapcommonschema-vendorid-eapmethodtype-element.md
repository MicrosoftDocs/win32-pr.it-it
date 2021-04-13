---
title: Elemento VendorId (EapMethodType)
description: Fa riferimento al fornitore che ha definito il metodo se l'elemento Type (EapMethodType) è 254 (un metodo EAP espanso).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517890"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="e9a40-104">Elemento VendorId (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="e9a40-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="e9a40-105">L'elemento **VendorID (EapMethodType)** fa riferimento al fornitore che ha definito il metodo se l'elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso).</span><span class="sxs-lookup"><span data-stu-id="e9a40-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="e9a40-106">**VendorID** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9a40-106">The **VendorId** is optional.</span></span> <span data-ttu-id="e9a40-107">Se usato, **VendorID** è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="e9a40-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="e9a40-108">L'elemento **VendorID** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a40-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9a40-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9a40-109">Remarks</span></span>

<span data-ttu-id="e9a40-110">Gli elementi [**autorizzazioned**](eapcommonschema-authorid-eapmethodtype-element.md) e **VendorID** non devono essere uguali per un metodo specifico.</span><span class="sxs-lookup"><span data-stu-id="e9a40-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a40-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9a40-111">Requirements</span></span>



| <span data-ttu-id="e9a40-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a40-112">Requirement</span></span> | <span data-ttu-id="e9a40-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e9a40-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9a40-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a40-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a40-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9a40-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a40-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a40-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9a40-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9a40-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9a40-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e9a40-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e9a40-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="e9a40-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="e9a40-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="e9a40-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e9a40-122">Schema eapcommon</span><span class="sxs-lookup"><span data-stu-id="e9a40-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





