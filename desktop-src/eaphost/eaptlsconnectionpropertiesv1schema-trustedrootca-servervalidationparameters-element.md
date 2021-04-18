---
title: Elemento TrustedRootCA (ServerValidationParameters)-Connection
description: Acquisisce la stampa Thumb delle autorità di certificazione radice considerate attendibili dal client. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323787"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="b91cf-105">Elemento TrustedRootCA (ServerValidationParameters) per le proprietà di connessione</span><span class="sxs-lookup"><span data-stu-id="b91cf-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="b91cf-106">L'elemento **TrustedRootCA (ServerValidationParameters)** acquisisce la stampa Thumb delle autorità di certificazione radice che sono considerate attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="b91cf-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="b91cf-107">L'elemento **TrustedRootCA** è definito dal tipo complesso [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b91cf-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b91cf-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b91cf-108">Remarks</span></span>

<span data-ttu-id="b91cf-109">La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="b91cf-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="b91cf-110">L'elemento **TrustedRootCA** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b91cf-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91cf-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b91cf-111">Requirements</span></span>



| <span data-ttu-id="b91cf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91cf-112">Requirement</span></span> | <span data-ttu-id="b91cf-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b91cf-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b91cf-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b91cf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b91cf-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b91cf-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b91cf-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b91cf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b91cf-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b91cf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b91cf-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b91cf-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b91cf-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b91cf-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b91cf-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="b91cf-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="b91cf-121">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b91cf-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b91cf-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="b91cf-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="b91cf-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b91cf-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b91cf-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b91cf-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b91cf-125">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b91cf-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b91cf-126">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b91cf-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





