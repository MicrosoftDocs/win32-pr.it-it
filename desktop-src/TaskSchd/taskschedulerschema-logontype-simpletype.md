---
title: Tipo semplice logonType
description: Definisce i valori possibili dell'elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Tipo semplice logonType Utilità di pianificazione
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f40301957ec323b8abf7c09829bf3b551e2e1665a811409622d342784d86e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758893"
---
# <a name="logontype-simple-type"></a>Tipo semplice logonType

Definisce i valori possibili [**dell'elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)

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

Il **tipo semplice logonType** definisce i valori seguenti.



| Valore                      | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4u                        | L'utente deve accedere usando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, non viene archiviata alcuna password dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                                                                                                                                          |
| Password                   | L'utente deve accedere usando una password.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Non più in uso; attualmente identico a Password.<br/> **Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista e Windows Server 2008:** L'attività verrà eseguita in una sessione interattiva esistente oppure l'utente deve accedere usando una password.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione semplici dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





