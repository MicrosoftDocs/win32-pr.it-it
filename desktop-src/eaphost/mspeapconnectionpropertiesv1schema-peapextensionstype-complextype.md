---
title: Tipo complesso PeapExtensionsType
description: Contiene miglioramenti allo schema apportati in Windows 7. I miglioramenti futuri dello schema verranno gestiti da PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742842"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="f930c-105">Tipo complesso PeapExtensionsType</span><span class="sxs-lookup"><span data-stu-id="f930c-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="f930c-106">Il tipo complesso **PeapExtensionsType** contiene miglioramenti dello schema apportati in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f930c-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="f930c-107">I miglioramenti futuri dello schema verranno gestiti da [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="f930c-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f930c-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f930c-108">Child elements</span></span>



| <span data-ttu-id="f930c-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f930c-109">Element</span></span>                                                                                                                               | <span data-ttu-id="f930c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f930c-110">Type</span></span> | <span data-ttu-id="f930c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f930c-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f930c-112">**extendedPeap:PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="f930c-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="f930c-113">Windows 7 e versioni successive: indica se viene eseguita la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="f930c-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="f930c-114">**extendedPeap:AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="f930c-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="f930c-115">Windows 7 e versioni successive: indica se viene letto il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="f930c-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="f930c-116">**extendedPeap:IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="f930c-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="f930c-117">Windows 7 e versioni successive: indica se viene inviata un'identità vera o anonima dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f930c-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="f930c-118">**extendedPeap:PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="f930c-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="f930c-119">Windows 7 e versioni successive: consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="f930c-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="f930c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f930c-120">Remarks</span></span>

<span data-ttu-id="f930c-121">L'elemento **PeapExtensionsType** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f930c-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f930c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f930c-122">Requirements</span></span>



| <span data-ttu-id="f930c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f930c-123">Requirement</span></span> | <span data-ttu-id="f930c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f930c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f930c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f930c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f930c-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f930c-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f930c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f930c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f930c-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f930c-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f930c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f930c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f930c-130">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="f930c-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f930c-131">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f930c-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f930c-132">Tipi complessi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f930c-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





