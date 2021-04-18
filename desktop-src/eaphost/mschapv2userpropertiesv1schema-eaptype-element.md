---
title: Elemento EapType (mschapv2userpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334320"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="b0fcd-105">Elemento EapType (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="b0fcd-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="b0fcd-106">L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dello schema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="b0fcd-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="b0fcd-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b0fcd-107">Child elements</span></span>



| <span data-ttu-id="b0fcd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0fcd-108">Element</span></span>                                                                           | <span data-ttu-id="b0fcd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0fcd-109">Type</span></span>   | <span data-ttu-id="b0fcd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0fcd-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0fcd-111">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="b0fcd-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="b0fcd-112">Identifica l'utente autenticato.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="b0fcd-113">Se questo elemento non è presente, il nome utente viene ottenuto da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="b0fcd-114">L'elemento [**username**](mschapv2userpropertiesv1schema-username-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="b0fcd-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="b0fcd-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="b0fcd-116">string</span><span class="sxs-lookup"><span data-stu-id="b0fcd-116">string</span></span> | <span data-ttu-id="b0fcd-117">Identifica il dominio dell'utente o del computer da autenticare.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="b0fcd-118">Se questo elemento non è presente, viene usato il dominio di Winlogon.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="b0fcd-119">L'elemento [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="b0fcd-120">**Password**</span><span class="sxs-lookup"><span data-stu-id="b0fcd-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="b0fcd-121">string</span><span class="sxs-lookup"><span data-stu-id="b0fcd-121">string</span></span> | <span data-ttu-id="b0fcd-122">Identifica la password dell'utente o del computer da autenticare.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="b0fcd-123">Se questo elemento non è presente, l'hash della password viene ottenuto da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="b0fcd-124">L'elemento [**password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0fcd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0fcd-125">Remarks</span></span>

<span data-ttu-id="b0fcd-126">L'elemento **processContents** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="b0fcd-127">L'elemento **processContents** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fcd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0fcd-128">Requirements</span></span>



| <span data-ttu-id="b0fcd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0fcd-129">Requirement</span></span> | <span data-ttu-id="b0fcd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b0fcd-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0fcd-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0fcd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fcd-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0fcd-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0fcd-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0fcd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fcd-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0fcd-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0fcd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0fcd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fcd-136">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b0fcd-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b0fcd-137">Schema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b0fcd-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





