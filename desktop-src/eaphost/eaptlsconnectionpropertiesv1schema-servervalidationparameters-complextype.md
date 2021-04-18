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
# <a name="servervalidationparameters-complex-type-tls"></a>Tipo complesso ServerValidationParameters (TLS)

Il tipo complesso **ServerValidationParameters** contiene informazioni su come eseguire la convalida del server.

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

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                                                    | Tipo      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean   | Indica se all'utente deve essere richiesta la convalida del server. <br/> Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è true, EAP-TLS esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, EAP-TLS ha esito negativo per l'autenticazione. <br/> Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è false, all'utente viene richiesto di specificare un certificato o un nome del server convalidato oppure un'autorità di certificazione radice (CA).<br/> L'elemento [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è facoltativo.<br/> |
| [**Nomi**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | string    | Rappresenta un elenco di server considerati attendibili dal client. Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari.<br/> L'elemento [**serverNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary | Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client. <br/> La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.<br/> L'elemento [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi complessi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





