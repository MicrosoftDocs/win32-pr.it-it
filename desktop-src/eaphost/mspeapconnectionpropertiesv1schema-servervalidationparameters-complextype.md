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
# <a name="servervalidationparameters-complex-type-peap"></a>Tipo complesso ServerValidationParameters (PEAP)

Il tipo complesso **ServerValidationParameters** contiene informazioni su come eseguire la convalida del server.

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

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                                                    | Tipo        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean     | Indica se all'utente deve essere richiesta la convalida del server. <br/> Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è true, PEAP esegue la convalida del server senza l'input dell'utente; Se la convalida ha esito negativo, PEAP non riesce.<br/> Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è false, all'utente viene richiesto un certificato o un nome del server convalidato o un'autorità di certificazione radice (CA).<br/> L'elemento [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) è facoltativo.<br/> |
| [**Nomi**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | complexType | Rappresenta un elenco di server considerati attendibili dal client. Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari. <br/> L'elemento [**serverNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary   | Acquisisce la stampa Thumb delle autorità di certificazione radice ritenute attendibili dal client. <br/> La stampa Thumb è una stringa esadecimale che contiene l'hash SHA-1 del certificato.<br/> L'elemento [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a>Attributi



| Nome                    | Tipo    | Descrizione                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PerformServerValidation | boolean | Windows 7 o versioni successive: indica se viene eseguita la convalida del server. L'elemento [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) è facoltativo.<br/> |



## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi complessi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





