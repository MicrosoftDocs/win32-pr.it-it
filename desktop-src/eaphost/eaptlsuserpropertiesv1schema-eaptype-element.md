---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334319"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="b2cd8-105">Elemento EapType (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="b2cd8-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="b2cd8-106">L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dello schema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="b2cd8-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="b2cd8-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b2cd8-107">Child elements</span></span>



| <span data-ttu-id="b2cd8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2cd8-108">Element</span></span>                                                                   | <span data-ttu-id="b2cd8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2cd8-109">Type</span></span>      | <span data-ttu-id="b2cd8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2cd8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2cd8-111">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="b2cd8-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="b2cd8-112">Acquisisce il nome utente da inviare nella risposta EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="b2cd8-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="b2cd8-113">Se l'elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento nell'elemento [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b2cd8-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="b2cd8-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="b2cd8-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="b2cd8-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="b2cd8-115">hexBinary</span></span> | <span data-ttu-id="b2cd8-116">Si riferisce all'hash SHA-1 del certificato che deve essere utilizzato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b2cd8-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="b2cd8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2cd8-117">Remarks</span></span>

<span data-ttu-id="b2cd8-118">L'elemento **processContents** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="b2cd8-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="b2cd8-119">L'elemento **processContents** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b2cd8-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2cd8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2cd8-120">Requirements</span></span>



| <span data-ttu-id="b2cd8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2cd8-121">Requirement</span></span> | <span data-ttu-id="b2cd8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b2cd8-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2cd8-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2cd8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b2cd8-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2cd8-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2cd8-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2cd8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b2cd8-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2cd8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2cd8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2cd8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cd8-128">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b2cd8-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b2cd8-129">Schema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b2cd8-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





