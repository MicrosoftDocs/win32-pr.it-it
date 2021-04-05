---
title: Elemento EapHostUserCredentials
description: Contiene l'elemento EapMethod e le credenziali o l'elemento CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Elemento EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120566"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="e5b3f-104">Elemento EapHostUserCredentials</span><span class="sxs-lookup"><span data-stu-id="e5b3f-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="e5b3f-105">L'elemento **EapHostUserCredentials** contiene l'elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) e le [**credenziali**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) o l'elemento [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b3f-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="e5b3f-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e5b3f-106">Child elements</span></span>



| <span data-ttu-id="e5b3f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e5b3f-107">Element</span></span>                                                                                                | <span data-ttu-id="e5b3f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5b3f-108">Type</span></span>                                                                                                                | <span data-ttu-id="e5b3f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5b3f-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5b3f-110">**Credenziali**</span><span class="sxs-lookup"><span data-stu-id="e5b3f-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="e5b3f-111">**BaseEapMethodUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="e5b3f-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="e5b3f-112">Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="e5b3f-113">**CredentialsBlob**</span><span class="sxs-lookup"><span data-stu-id="e5b3f-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="e5b3f-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e5b3f-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="e5b3f-115">Viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="e5b3f-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="e5b3f-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="e5b3f-117">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="e5b3f-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="e5b3f-118">Identifica il metodo a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="e5b3f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5b3f-119">Remarks</span></span>

<span data-ttu-id="e5b3f-120">Gli elementi [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="e5b3f-121">Esiste un punto di estensione per altri spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="e5b3f-122">L'elemento **processContents** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="e5b3f-123">L'elemento **processContents** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b3f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5b3f-124">Requirements</span></span>



| <span data-ttu-id="e5b3f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b3f-125">Requirement</span></span> | <span data-ttu-id="e5b3f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b3f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5b3f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b3f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b3f-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5b3f-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5b3f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b3f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b3f-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5b3f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5b3f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5b3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b3f-132">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="e5b3f-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e5b3f-133">Schema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="e5b3f-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





