---
title: Elemento SendEmail (actionGroup)
description: Rappresenta un'azione che invia un messaggio di posta elettronica.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Utilità di pianificazione elemento SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964672"
---
# <a name="sendemail-actiongroup-element"></a>Elemento SendEmail (actionGroup)

Rappresenta un'azione che invia un messaggio di posta elettronica.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

L'elemento **SendEmail** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                         | Derivato da                                                       | Descrizione                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene le azioni eseguite dall'attività.<br/> |



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



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere l'interfaccia [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Per lo sviluppo di script, vedere l'oggetto [**EmailAction**](emailaction.md) .

**Windows 8 e Windows Server 2012:** Questo elemento è stato rimosso. Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un'azione di posta elettronica, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |
| Fine del supporto client<br/>    | Windows 7<br/>                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                    |



 

