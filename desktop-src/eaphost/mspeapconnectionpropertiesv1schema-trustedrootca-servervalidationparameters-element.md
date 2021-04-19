---
title: Elemento TrustedRootCA (ServerValidationParameters) (V1)
description: Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389078"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="8137b-105">Elemento TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="8137b-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="8137b-106">L'elemento **TrustedRootCA (ServerValidationParameters)** elemento acquisisce la stampa Thumb delle autorità di certificazione radice che sono considerate attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="8137b-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="8137b-107">L'elemento **TrustedRootCA** è definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8137b-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8137b-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8137b-108">Remarks</span></span>

<span data-ttu-id="8137b-109">La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="8137b-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="8137b-110">L'elemento **TrustedRootCA** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8137b-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8137b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8137b-111">Requirements</span></span>



| <span data-ttu-id="8137b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8137b-112">Requirement</span></span> | <span data-ttu-id="8137b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8137b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8137b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8137b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8137b-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8137b-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8137b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8137b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8137b-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8137b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8137b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8137b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="8137b-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="8137b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8137b-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="8137b-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="8137b-121">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="8137b-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8137b-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="8137b-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="8137b-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8137b-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="8137b-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="8137b-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8137b-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8137b-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="8137b-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8137b-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





