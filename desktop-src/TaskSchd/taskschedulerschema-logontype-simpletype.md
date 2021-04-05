---
title: Tipo semplice logonType
description: Definisce i valori possibili dell'elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Utilità di pianificazione di tipo semplice logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120794"
---
# <a name="logontype-simple-type"></a>Tipo semplice logonType

Definisce i valori possibili dell'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **LogonType** definisce i valori seguenti.



| Valore                      | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                                                                                                                                          |
| Password                   | L'utente deve eseguire l'accesso con una password.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Non più in uso; attualmente identico a una password.<br/> **Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista e Windows server 2008:** L'attività verrà eseguita in una sessione interattiva esistente oppure l'utente dovrà effettuare l'accesso con una password.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi semplici dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





