---
title: Tipo complesso registrationInfoType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Utilità di pianificazione di tipo complesso registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964513"
---
# <a name="registrationinfotype-complex-type"></a>Tipo complesso registrationInfoType

Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .

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
| [**Origine**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Specifica la posizione da cui ha avuto origine l'attività. Ad esempio, da un componente, un servizio, un'applicazione o un utente.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Specifica l'URI dell'attività.<br/>                                                                          |
| [**Versione**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Specifica il numero di versione dell'attività.<br/>                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





