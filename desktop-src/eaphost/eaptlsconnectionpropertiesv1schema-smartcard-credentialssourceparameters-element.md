---
title: Elemento SmartCard (CredentialsSourceParameters)
description: Indica che EAP-TLS deve leggere il certificato dalla smart card.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Elemento SmartCard EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301954"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="6acf7-104">Elemento SmartCard (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="6acf7-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="6acf7-105">L'elemento **smartcard (CredentialsSourceParameters)** indica che EAP-TLS deve leggere il certificato dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="6acf7-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="6acf7-106">L'elemento **smartcard** è definito dal tipo complesso [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6acf7-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acf7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6acf7-107">Remarks</span></span>

<span data-ttu-id="6acf7-108">Gli elementi [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e **smartcard** non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="6acf7-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6acf7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6acf7-109">Requirements</span></span>



| <span data-ttu-id="6acf7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6acf7-110">Requirement</span></span> | <span data-ttu-id="6acf7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6acf7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6acf7-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6acf7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6acf7-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6acf7-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6acf7-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6acf7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6acf7-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6acf7-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6acf7-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6acf7-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="6acf7-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="6acf7-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6acf7-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="6acf7-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="6acf7-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="6acf7-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6acf7-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="6acf7-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="6acf7-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6acf7-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6acf7-122">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="6acf7-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6acf7-123">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6acf7-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6acf7-124">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6acf7-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





