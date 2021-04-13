---
title: Tipo semplice processTokenSidType
description: Definisce i valori possibili per l'elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Utilità di pianificazione di tipo semplice processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400472"
---
# <a name="processtokensidtype-simple-type"></a>Tipo semplice processTokenSidType

Definisce i valori possibili per l'elemento [**ProcessTokenSidType (PrincipalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **processTokenSidType** definisce i valori seguenti.



| Valore        | Descrizione                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| nessuno         | Le attività vengono eseguite in un processo che non contiene un SID del token di processo. non verrà apportata alcuna modifica all'elenco dei gruppi di token di processo.<br/> |
| Senza restrizioni | Un SID attività sarà derivato dal percorso completo dell'attività e verrà aggiunto all'elenco dei gruppi di token di processo.<br/>                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





