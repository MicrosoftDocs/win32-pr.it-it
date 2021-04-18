---
title: Elemento DisableUserPromptForServerValidation (PEAP)
description: Informazioni sull'elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se all'utente deve essere richiesta la convalida del server. | Elemento DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- Elemento DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321439"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="46e9f-106">Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="46e9f-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="46e9f-107">L'elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se all'utente deve essere richiesta la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="46e9f-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="46e9f-108">Se **DisableUserPromptForServerValidation** è true, EAP-TLS esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, EAP-TLS ha esito negativo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="46e9f-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="46e9f-109">Se **DisableUserPromptForServerValidation** è false, all'utente viene richiesto di specificare un certificato o un nome del server convalidato oppure un'autorità di certificazione radice (CA).</span><span class="sxs-lookup"><span data-stu-id="46e9f-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="46e9f-110">L'elemento **DisableUserPromptForServerValidation** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="46e9f-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="46e9f-111">L'elemento **DisableUserPromptForServerValidation** è definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="46e9f-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e9f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46e9f-112">Requirements</span></span>



| <span data-ttu-id="46e9f-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="46e9f-113">Role</span></span> | <span data-ttu-id="46e9f-114">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="46e9f-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="46e9f-115">Client</span><span class="sxs-lookup"><span data-stu-id="46e9f-115">Client</span></span><br/> | <span data-ttu-id="46e9f-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46e9f-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46e9f-117">Server</span><span class="sxs-lookup"><span data-stu-id="46e9f-117">Server</span></span><br/> | <span data-ttu-id="46e9f-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46e9f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46e9f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46e9f-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="46e9f-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="46e9f-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="46e9f-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="46e9f-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="46e9f-122">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="46e9f-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="46e9f-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="46e9f-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="46e9f-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="46e9f-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="46e9f-125">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="46e9f-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="46e9f-126">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="46e9f-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="46e9f-127">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="46e9f-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





