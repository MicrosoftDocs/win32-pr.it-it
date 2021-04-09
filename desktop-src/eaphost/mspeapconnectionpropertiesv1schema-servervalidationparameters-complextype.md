---
title: Tipo complesso ServerValidationParameters (PEAP)
description: Informazioni sul tipo complesso ServerValidationParameters. Questo tipo contiene informazioni su come eseguire la convalida del server. | Tipo complesso ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- ServerValidationParameters di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969044"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="81dad-106">Tipo complesso ServerValidationParameters (PEAP)</span><span class="sxs-lookup"><span data-stu-id="81dad-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="81dad-107">Il tipo complesso **ServerValidationParameters** contiene informazioni su come eseguire la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="81dad-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="81dad-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="81dad-108">Child elements</span></span>



| <span data-ttu-id="81dad-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="81dad-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="81dad-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="81dad-110">Type</span></span>        | <span data-ttu-id="81dad-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81dad-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81dad-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="81dad-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="81dad-113">boolean</span><span class="sxs-lookup"><span data-stu-id="81dad-113">boolean</span></span>     | <span data-ttu-id="81dad-114">Indica se all'utente deve essere richiesta la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="81dad-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="81dad-115">Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è true, PEAP esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, PEAP non riesce.</span><span class="sxs-lookup"><span data-stu-id="81dad-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="81dad-116">Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è false, all'utente viene richiesto un certificato o un nome del server convalidato o un'autorità di certificazione radice (CA).</span><span class="sxs-lookup"><span data-stu-id="81dad-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="81dad-117">L'elemento [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="81dad-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="81dad-118">**Nomi**</span><span class="sxs-lookup"><span data-stu-id="81dad-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="81dad-119">complexType</span><span class="sxs-lookup"><span data-stu-id="81dad-119">complextype</span></span> | <span data-ttu-id="81dad-120">Rappresenta un elenco di server considerati attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="81dad-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="81dad-121">Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="81dad-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="81dad-122">L'elemento [**serverNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="81dad-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="81dad-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="81dad-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="81dad-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="81dad-124">hexBinary</span></span>   | <span data-ttu-id="81dad-125">Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="81dad-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="81dad-126">La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="81dad-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="81dad-127">L'elemento [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="81dad-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="81dad-128">Attributi</span><span class="sxs-lookup"><span data-stu-id="81dad-128">Attributes</span></span>



| <span data-ttu-id="81dad-129">Nome</span><span class="sxs-lookup"><span data-stu-id="81dad-129">Name</span></span>                    | <span data-ttu-id="81dad-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="81dad-130">Type</span></span>    | <span data-ttu-id="81dad-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81dad-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dad-132">PerformServerValidation</span><span class="sxs-lookup"><span data-stu-id="81dad-132">PerformServerValidation</span></span> | <span data-ttu-id="81dad-133">boolean</span><span class="sxs-lookup"><span data-stu-id="81dad-133">boolean</span></span> | <span data-ttu-id="81dad-134">Windows 7 o versioni successive: indica se viene eseguita la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="81dad-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="81dad-135">L'elemento [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="81dad-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="81dad-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81dad-136">Requirements</span></span>



| <span data-ttu-id="81dad-137">Ruolo</span><span class="sxs-lookup"><span data-stu-id="81dad-137">Role</span></span> | <span data-ttu-id="81dad-138">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="81dad-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="81dad-139">Client</span><span class="sxs-lookup"><span data-stu-id="81dad-139">Client</span></span><br/> | <span data-ttu-id="81dad-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81dad-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81dad-141">Server</span><span class="sxs-lookup"><span data-stu-id="81dad-141">Server</span></span><br/> | <span data-ttu-id="81dad-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81dad-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81dad-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81dad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dad-144">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="81dad-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="81dad-145">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="81dad-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="81dad-146">Tipi complessi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="81dad-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="81dad-147">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="81dad-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





