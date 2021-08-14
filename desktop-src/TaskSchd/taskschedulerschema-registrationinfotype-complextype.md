---
title: Tipo complesso registrationInfoType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Tipo complesso registrationInfoType Utilità di pianificazione
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 704fcb3205f032654ef6a666dd119dec34f88992018f16b1715ba4982847149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131661"
---
# <a name="registrationinfotype-complex-type"></a>Tipo complesso registrationInfoType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento RegistrationInfo.**](taskschedulerschema-registrationinfo-tasktype-element.md)

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                           | Tipo     | Descrizione                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Autore**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Specifica l'autore dell'attività.<br/>                                                                       |
| [**Data**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Specifica la data e l'ora di registrazione dell'attività.<br/>                                                |
| [**Descrizione**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Specifica la descrizione dell'attività.<br/>                                                                  |
| [**Documentazione**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Specifica qualsiasi documentazione aggiuntiva per l'attività.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Specifica il descrittore di sicurezza dell'attività.<br/>                                                          |
| [**fonte**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Specifica la posizione di origine dell'attività. Ad esempio, da un componente, un servizio, un'applicazione o un utente.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Specifica l'URI dell'attività.<br/>                                                                          |
| [**Versione**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Specifica il numero di versione dell'attività.<br/>                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





