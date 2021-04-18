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
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)

L'elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se all'utente deve essere richiesta la convalida del server.

Se **DisableUserPromptForServerValidation** è true, EAP-TLS esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, EAP-TLS ha esito negativo per l'autenticazione. Se **DisableUserPromptForServerValidation** è false, all'utente viene richiesto di specificare un certificato o un nome del server convalidato oppure un'autorità di certificazione radice (CA).

L'elemento **DisableUserPromptForServerValidation** è facoltativo.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

L'elemento **DisableUserPromptForServerValidation** è definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





