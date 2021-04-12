---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contiene un'identità anonima utilizzata al posto dell'identificazione true di un utente. Viene inviato durante la prima fase dell'autenticazione PEAP quando l'identità viene inviata come testo normale.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400767"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="1c292-105">Elemento AnonymousUserName (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="1c292-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="1c292-106">L'elemento **AnonymousUserName (IdentityPrivacyParameters)** contiene un'identità anonima usata al posto dell'identificazione true di un utente.</span><span class="sxs-lookup"><span data-stu-id="1c292-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="1c292-107">Viene inviato durante la prima fase dell'autenticazione PEAP quando l' **identità** viene inviata come testo normale.</span><span class="sxs-lookup"><span data-stu-id="1c292-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="1c292-108">L'utilizzo dell'identità anonima è determinato dall'elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1c292-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="1c292-109">L'elemento **AnonymousUserName** è definito da [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1c292-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="1c292-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c292-110">Remarks</span></span>

<span data-ttu-id="1c292-111">L'elemento **AnonymousUserName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1c292-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c292-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c292-112">Requirements</span></span>



| <span data-ttu-id="1c292-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c292-113">Requirement</span></span> | <span data-ttu-id="1c292-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1c292-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1c292-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c292-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1c292-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1c292-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1c292-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c292-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1c292-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c292-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c292-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c292-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c292-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1c292-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1c292-121">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="1c292-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="1c292-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="1c292-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1c292-123">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="1c292-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="1c292-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="1c292-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1c292-125">Schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1c292-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1c292-126">Elementi dello schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1c292-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





