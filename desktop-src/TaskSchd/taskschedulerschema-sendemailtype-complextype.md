---
title: Tipo complesso sendEmailType
description: Definisce il tipo di azione usato per specificare che verrà inviato un messaggio di posta elettronica quando viene eseguita un'attività. Questo tipo definisce tutti gli elementi usati per modellare il messaggio di posta elettronica.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Tipo complesso sendEmailType Utilità di pianificazione
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0242700b2f22050741d9de175b7dae532cc5ef4bb2097fadb23799ce3b2f82b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356343"
---
# <a name="sendemailtype-complex-type"></a>Tipo complesso sendEmailType

Definisce il tipo di azione usato per specificare che verrà inviato un messaggio di posta elettronica quando viene eseguita un'attività. Questo tipo definisce tutti gli elementi usati per modellare il messaggio di posta elettronica.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                        | Tipo                                                                         | Descrizione                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Allegati**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Specifica un elenco di allegati nel messaggio di posta elettronica.<br/>                                 |
| [**Bcc**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Specifica gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.<br/>               |
| [**Corpo**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Specifica il testo nel corpo del messaggio di posta elettronica.<br/>                                  |
| [**Cc**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Specifica gli indirizzi di posta elettronica usati nella riga Cc di un messaggio di posta elettronica.<br/>                |
| [**Da**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Specifica l'indirizzo di posta elettronica del mittente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Specifica i campi di intestazione e i relativi valori utilizzati nell'intestazione del messaggio di posta elettronica.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Specifica gli indirizzi di posta elettronica a cui viene inviata una risposta nel messaggio di posta elettronica.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Specifica il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica. <br/>                           |
| [**Oggetto**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Specifica l'oggetto del messaggio di posta elettronica.<br/>                                           |
| [**A**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Specifica gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.<br/>                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





