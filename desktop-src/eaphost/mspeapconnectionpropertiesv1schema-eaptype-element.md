---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema BaseEapConnectionProperties. Per mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334325"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="61535-105">Elemento EapType (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="61535-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="61535-106">L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) dello schema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="61535-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="61535-107">Questo elemento **EapType** derivato contiene gli elementi seguenti: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) e [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="61535-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="61535-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="61535-108">Child elements</span></span>



| <span data-ttu-id="61535-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="61535-109">Element</span></span>                                                                                                     | <span data-ttu-id="61535-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="61535-110">Type</span></span>                                                                                                            | <span data-ttu-id="61535-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61535-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61535-112">**EAP**</span><span class="sxs-lookup"><span data-stu-id="61535-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="61535-113">Descrive il metodo interno e la configurazione del metodo.</span><span class="sxs-lookup"><span data-stu-id="61535-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="61535-114">Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è true, è necessario che l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) sia presente.</span><span class="sxs-lookup"><span data-stu-id="61535-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="61535-115">Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è false, l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deve essere assente.</span><span class="sxs-lookup"><span data-stu-id="61535-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="61535-116">**EnableQuarantineChecks**</span><span class="sxs-lookup"><span data-stu-id="61535-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="61535-117">boolean</span><span class="sxs-lookup"><span data-stu-id="61535-117">boolean</span></span>                                                                                                         | <span data-ttu-id="61535-118">Indica se eseguire i controlli di protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="61535-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="61535-119">Se l'elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è true, PEAP eseguirà i controlli NAP; Se FALSE PEAP non eseguirà controlli NAP.</span><span class="sxs-lookup"><span data-stu-id="61535-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="61535-120">L'elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="61535-121">**Per riconnessione rapida**</span><span class="sxs-lookup"><span data-stu-id="61535-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="61535-122">boolean</span><span class="sxs-lookup"><span data-stu-id="61535-122">boolean</span></span>                                                                                                         | <span data-ttu-id="61535-123">Indica se eseguire una riconnessione rapida.</span><span class="sxs-lookup"><span data-stu-id="61535-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="61535-124">Se l'elemento [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è true, PEAP tenta di eseguire una riconnessione rapida. Se FALSE, PEAP esegue l'autenticazione completa.</span><span class="sxs-lookup"><span data-stu-id="61535-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="61535-125">L'elemento [**per riconnessione rapida**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="61535-126">**IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="61535-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="61535-127">**IdentityPrivacyParameters**</span><span class="sxs-lookup"><span data-stu-id="61535-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="61535-128">Windows 7 o versioni successive: indica se viene inviata un'identità vera o anonima dell'utente.</span><span class="sxs-lookup"><span data-stu-id="61535-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="61535-129">L'elemento [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="61535-130">**InnerEapOptional**</span><span class="sxs-lookup"><span data-stu-id="61535-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="61535-131">boolean</span><span class="sxs-lookup"><span data-stu-id="61535-131">boolean</span></span>                                                                                                         | <span data-ttu-id="61535-132">Indica se eseguire l'accesso GUEST.</span><span class="sxs-lookup"><span data-stu-id="61535-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="61535-133">Se l'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è true, è necessario che l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) sia presente e descriva il metodo interno e la relativa configurazione. Se FALSE, PEAP eseguirà l'accesso GUEST.</span><span class="sxs-lookup"><span data-stu-id="61535-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="61535-134">L'elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="61535-135">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="61535-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="61535-136">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="61535-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="61535-137">L'elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="61535-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="61535-138">L'elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="61535-139">**RequireCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="61535-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="61535-140">boolean</span><span class="sxs-lookup"><span data-stu-id="61535-140">boolean</span></span>                                                                                                         | <span data-ttu-id="61535-141">Indica se eseguire l'autenticazione con i server che supportano la crittografia.</span><span class="sxs-lookup"><span data-stu-id="61535-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="61535-142">Se l'elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è true, PEAP eseguirà l'autenticazione con i server che non supportano Crypto; Se FALSE, PEAP eseguirà l'autenticazione solo con i server che supportano la crittografia.</span><span class="sxs-lookup"><span data-stu-id="61535-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="61535-143">L'elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="61535-144">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="61535-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="61535-145">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="61535-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="61535-146">Contiene informazioni su come eseguire la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="61535-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="61535-147">L'elemento [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61535-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="61535-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61535-148">Requirements</span></span>



| <span data-ttu-id="61535-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="61535-149">Requirement</span></span> | <span data-ttu-id="61535-150">Valore</span><span class="sxs-lookup"><span data-stu-id="61535-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61535-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61535-151">Minimum supported client</span></span><br/> | <span data-ttu-id="61535-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61535-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61535-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61535-153">Minimum supported server</span></span><br/> | <span data-ttu-id="61535-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61535-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61535-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61535-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61535-156">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="61535-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="61535-157">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="61535-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="61535-158">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="61535-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





