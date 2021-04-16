---
title: Elemento RegistrationInfo (taskType)
description: Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informazioni di registrazione Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477783"
---
# <a name="registrationinfo-tasktype-element"></a>Elemento RegistrationInfo (taskType)

Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

L'elemento **RegistrationInfo** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definisce l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                  | Tipo     | Descrizione                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autore (registrationInfoType)**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Specifica l'autore dell'attività.<br/>                                                                              |
| [**Data (registrationInfoType)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Specifica la data e l'ora di registrazione dell'attività.<br/>                                                       |
| [**Descrizione (registrationInfoType)**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Specifica la descrizione dell'attività.<br/>                                                                         |
| [**Documentazione (registrationInfoType)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Specifica qualsiasi documentazione aggiuntiva per l'attività.<br/>                                                           |
| [**SecurityDescriptor (registrationInfoType)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Specifica il descrittore di sicurezza dell'attività.<br/>                                                                 |
| [**Origine (registrationInfoType)**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Specifica la posizione da cui ha avuto origine l'attività. Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.<br/> |
| [**URI (registrationInfoType)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Specifica l'URI dell'attività.<br/>                                                                                 |
| [**Versione (registrationInfoType)**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Specifica il numero di versione dell'attività.<br/>                                                                      |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le informazioni di registrazione di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .

Per lo sviluppo in C++, le informazioni di registrazione di un'attività vengono specificate utilizzando la [**Proprietà RegistrationInfo di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





