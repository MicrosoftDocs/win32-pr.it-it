---
title: Elemento config (EapHostConfig)
description: Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento config EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477170"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="2b92b-104">Elemento config (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="2b92b-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="2b92b-105">L'elemento **config (EapHostConfig)** viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="2b92b-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="2b92b-106">L'elemento **config** è definito dall'elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2b92b-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b92b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b92b-107">Remarks</span></span>

<span data-ttu-id="2b92b-108">Gli elementi **config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="2b92b-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b92b-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b92b-109">Requirements</span></span>



| <span data-ttu-id="2b92b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b92b-110">Requirement</span></span> | <span data-ttu-id="2b92b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2b92b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b92b-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b92b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2b92b-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b92b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b92b-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b92b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2b92b-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b92b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b92b-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b92b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b92b-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="2b92b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2b92b-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="2b92b-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="2b92b-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="2b92b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2b92b-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="2b92b-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="2b92b-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="2b92b-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2b92b-122">Schema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="2b92b-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





