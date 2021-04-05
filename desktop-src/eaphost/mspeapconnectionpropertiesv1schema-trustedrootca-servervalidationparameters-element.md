---
title: Elemento TrustedRootCA (ServerValidationParameters)
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
ms.openlocfilehash: e62b691c5075f1a42f87e558a9a1f0795b90e8bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886070"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="1f8ce-105">Elemento TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="1f8ce-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="1f8ce-106">L'elemento **TrustedRootCA (ServerValidationParameters)** elemento acquisisce la stampa Thumb delle autorità di certificazione radice che sono considerate attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="1f8ce-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="1f8ce-107">L'elemento **TrustedRootCA** è definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8ce-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f8ce-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f8ce-108">Remarks</span></span>

<span data-ttu-id="1f8ce-109">La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="1f8ce-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="1f8ce-110">L'elemento **TrustedRootCA** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f8ce-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8ce-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f8ce-111">Requirements</span></span>



| <span data-ttu-id="1f8ce-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f8ce-112">Requirement</span></span> | <span data-ttu-id="1f8ce-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8ce-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f8ce-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f8ce-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8ce-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f8ce-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f8ce-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f8ce-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8ce-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f8ce-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f8ce-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f8ce-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f8ce-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1f8ce-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1f8ce-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="1f8ce-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="1f8ce-121">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="1f8ce-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1f8ce-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="1f8ce-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="1f8ce-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1f8ce-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1f8ce-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="1f8ce-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1f8ce-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f8ce-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1f8ce-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f8ce-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





