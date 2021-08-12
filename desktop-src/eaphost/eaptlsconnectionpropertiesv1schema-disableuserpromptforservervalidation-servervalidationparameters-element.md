---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: Informazioni sull'elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se all'utente deve essere richiesta la convalida del server. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
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
ms.openlocfilehash: 37f412f9c6200e7d2a54d624d0a77b4df5316ea7edd0ab75b69f92c753abbcff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273719"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (TLS)

**L'elemento DisableUserPromptForServerValidation (ServerValidationParameters)** indica se all'utente deve essere richiesta la convalida del server.

Se **DisableUserPromptForServerValidation** è TRUE, EAP-TLS esegue la convalida del server senza l'input dell'utente. Se la convalida non riesce, EAP-TLS non riesce l'autenticazione. Se **DisableUserPromptForServerValidation** è FALSE, all'utente viene richiesto di specificare un nome o un certificato del server convalidato o un'autorità di certificazione radice (CA).

**L'elemento DisableUserPromptForServerValidation** è facoltativo.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

**L'elemento DisableUserPromptForServerValidation** è definito dal tipo complesso [**ServerValidationParameters.**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Proprietà ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





