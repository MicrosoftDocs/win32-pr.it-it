---
title: Elemento ConfigBlob (EapHostConfig)
description: Viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato stringa di testo.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Elemento ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739695"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="fd558-104">Elemento ConfigBlob (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="fd558-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="fd558-105">L'elemento **ConfigBlob (EapHostConfig)** viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="fd558-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="fd558-106">L'elemento **ConfigBlob** è definito dall'elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fd558-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd558-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd558-107">Remarks</span></span>

<span data-ttu-id="fd558-108">Gli elementi [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e **ConfigBlob** non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="fd558-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd558-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd558-109">Requirements</span></span>



| <span data-ttu-id="fd558-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd558-110">Requirement</span></span> | <span data-ttu-id="fd558-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fd558-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd558-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd558-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd558-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd558-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd558-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd558-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd558-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd558-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd558-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd558-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd558-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fd558-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fd558-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="fd558-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="fd558-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fd558-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fd558-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="fd558-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="fd558-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="fd558-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fd558-122">Schema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="fd558-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





