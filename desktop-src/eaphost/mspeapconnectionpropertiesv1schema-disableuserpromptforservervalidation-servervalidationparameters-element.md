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
ms.openlocfilehash: c032c4c0dcb67f60f64fe2b447fd1af7061df51ed19586f4ee15b43d6a6f870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561761"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)

**L'elemento DisableUserPromptForServerValidation (ServerValidationParameters)** indica se all'utente deve essere richiesta la convalida del server.

Se **DisableUserPromptForServerValidation** è TRUE, EAP-TLS esegue la convalida del server senza input dell'utente. se la convalida non riesce, EAP-TLS non riesce l'autenticazione. Se **DisableUserPromptForServerValidation** è FALSE, all'utente viene richiesto di specificare un nome o un certificato del server convalidato o un'autorità di certificazione radice.

**L'elemento DisableUserPromptForServerValidation** è facoltativo.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

**L'elemento DisableUserPromptForServerValidation** è definito dal tipo complesso [**ServerValidationParameters.**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



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

 

 





