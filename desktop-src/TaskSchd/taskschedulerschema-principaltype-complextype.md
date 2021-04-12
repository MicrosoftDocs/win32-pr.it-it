---
title: Tipo complesso principalType
description: Definisce l'attributo, gli elementi figlio e le informazioni di sequenziazione per l'elemento Principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- Utilità di pianificazione di tipo complesso principalType
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478167"
---
# <a name="principaltype-complex-type"></a>Tipo complesso principalType

Definisce l'attributo, gli elementi figlio e le informazioni di sequenziazione per l'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) .

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                             | Tipo                                                                                     | Descrizione                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | string                                                                                   | Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | Specifica i tipi di ID di sicurezza (SID) del processo che possono essere utilizzati dalle attività.<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Specifica i privilegi necessari per eseguire l'attività.<br/>                                                               |
| [**RunLevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | Specifica il livello di autorizzazione in cui verrà eseguita l'attività.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.<br/>              |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                                           |
|------|------|-------------------------------------------------------|
| id   | ID   | Specifica l'identificatore dell'entità.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





