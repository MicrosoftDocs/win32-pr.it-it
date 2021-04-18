---
title: Tipo complesso sendEmailType
description: Definisce il tipo di azione utilizzato per specificare che un messaggio di posta elettronica verrà inviato quando viene eseguita un'attività. Questo tipo definisce tutti gli elementi utilizzati per modellare il messaggio di posta elettronica.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Utilità di pianificazione di tipo complesso sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302681"
---
# <a name="sendemailtype-complex-type"></a>Tipo complesso sendEmailType

Definisce il tipo di azione utilizzato per specificare che un messaggio di posta elettronica verrà inviato quando viene eseguita un'attività. Questo tipo definisce tutti gli elementi utilizzati per modellare il messaggio di posta elettronica.

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
| [**CC**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Specifica gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.<br/>                |
| [**Da**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Specifica l'indirizzo di posta elettronica del mittente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Specifica gli indirizzi di posta elettronica a cui risponde nel messaggio di posta elettronica.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Specifica il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica. <br/>                           |
| [**Oggetto**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Specifica l'oggetto del messaggio di posta elettronica.<br/>                                           |
| [**A**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Specifica gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.<br/>                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





