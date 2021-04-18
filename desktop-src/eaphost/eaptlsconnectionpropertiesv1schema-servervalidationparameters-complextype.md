---
title: Tipo complesso ServerValidationParameters (TLS)
description: Informazioni sul tipo complesso ServerValidationParameters. Questo tipo contiene informazioni su come eseguire la convalida del server. | Tipo complesso ServerValidationParameters (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
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
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321619"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="80190-106">Tipo complesso ServerValidationParameters (TLS)</span><span class="sxs-lookup"><span data-stu-id="80190-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="80190-107">Il tipo complesso **ServerValidationParameters** contiene informazioni su come eseguire la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="80190-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="80190-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="80190-108">Child elements</span></span>



| <span data-ttu-id="80190-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="80190-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="80190-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="80190-110">Type</span></span>      | <span data-ttu-id="80190-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80190-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80190-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="80190-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="80190-113">boolean</span><span class="sxs-lookup"><span data-stu-id="80190-113">boolean</span></span>   | <span data-ttu-id="80190-114">Indica se all'utente deve essere richiesta la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="80190-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="80190-115">Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è true, EAP-TLS esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, EAP-TLS ha esito negativo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="80190-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="80190-116">Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è false, all'utente viene richiesto di specificare un certificato o un nome del server convalidato oppure un'autorità di certificazione radice (CA).</span><span class="sxs-lookup"><span data-stu-id="80190-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="80190-117">L'elemento [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80190-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="80190-118">**Nomi**</span><span class="sxs-lookup"><span data-stu-id="80190-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="80190-119">string</span><span class="sxs-lookup"><span data-stu-id="80190-119">string</span></span>    | <span data-ttu-id="80190-120">Rappresenta un elenco di server considerati attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="80190-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="80190-121">Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="80190-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="80190-122">L'elemento [**serverNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80190-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="80190-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="80190-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="80190-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="80190-124">hexBinary</span></span> | <span data-ttu-id="80190-125">Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client.</span><span class="sxs-lookup"><span data-stu-id="80190-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="80190-126">La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="80190-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="80190-127">L'elemento [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80190-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="80190-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80190-128">Requirements</span></span>



| <span data-ttu-id="80190-129">Ruolo</span><span class="sxs-lookup"><span data-stu-id="80190-129">Role</span></span> | <span data-ttu-id="80190-130">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="80190-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="80190-131">Client</span><span class="sxs-lookup"><span data-stu-id="80190-131">Client</span></span><br/> | <span data-ttu-id="80190-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80190-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80190-133">Server</span><span class="sxs-lookup"><span data-stu-id="80190-133">Server</span></span><br/> | <span data-ttu-id="80190-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80190-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80190-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80190-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80190-136">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="80190-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="80190-137">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="80190-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="80190-138">Tipi complessi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="80190-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





