---
title: Elemento EapType (eaptlsconnectionpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema BaseEapConnectionProperties. Per eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334383"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="7ba7b-105">Elemento EapType (eaptlsconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="7ba7b-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="7ba7b-106">L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) dello schema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba7b-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="7ba7b-107">Questo elemento **EapType** derivato contiene gli elementi seguenti: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)e [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="7ba7b-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7ba7b-108">Child elements</span></span>



| <span data-ttu-id="7ba7b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ba7b-109">Element</span></span>                                                                                                                               | <span data-ttu-id="7ba7b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ba7b-110">Type</span></span>                                                                                                              | <span data-ttu-id="7ba7b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ba7b-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ba7b-112">**extendedTLS: PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="7ba7b-113">Windows 7 e versioni successive: indica se viene eseguita la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="7ba7b-114">**extendedTLS: AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="7ba7b-115">Windows 7 e versioni successive: indica se viene letto il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="7ba7b-116">**extendedTLS: TLSExtensions**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="7ba7b-117">Windows 7 e versioni successive: consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7ba7b-118">**CredentialsSource**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="7ba7b-119">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="7ba7b-120">Contiene informazioni sulla posizione del certificato EAP-TLS (EAP Transport Level Security).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="7ba7b-121">L'elemento [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7ba7b-122">**DifferentUsername**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="7ba7b-123">boolean</span><span class="sxs-lookup"><span data-stu-id="7ba7b-123">boolean</span></span>                                                                                                           | <span data-ttu-id="7ba7b-124">Determina il nome utente EAP-TLS da usare.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="7ba7b-125">Se l'elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) è **true**, EAP-TLS deve usare un nome utente diverso dal nome visualizzato nel certificato.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="7ba7b-126">Se l'elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) è **false**, EAP-TLS usa il nome utente visualizzato nel certificato.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="7ba7b-127">L'elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="7ba7b-128">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="7ba7b-129">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="7ba7b-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="7ba7b-130">Contiene informazioni su come eseguire la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="7ba7b-131">L'elemento [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="7ba7b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ba7b-132">Requirements</span></span>



| <span data-ttu-id="7ba7b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba7b-133">Requirement</span></span> | <span data-ttu-id="7ba7b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7ba7b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ba7b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ba7b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba7b-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ba7b-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ba7b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ba7b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba7b-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ba7b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ba7b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ba7b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba7b-140">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="7ba7b-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7ba7b-141">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7ba7b-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7ba7b-142">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7ba7b-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





