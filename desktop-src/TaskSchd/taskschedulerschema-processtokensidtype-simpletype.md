---
title: Tipo semplice processTokenSidType
description: Definisce i valori possibili per l'elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Tipo semplice processTokenSidType Utilità di pianificazione
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611903"
---
# <a name="processtokensidtype-simple-type"></a>Tipo semplice processTokenSidType

Definisce i valori possibili per [**l'elemento ProcessTokenSidType (principalType).**](taskschedulerschema-processtokensidtype-principaltype-element.md)

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
| nessuno         | Le attività vengono eseguite in un processo che non contiene un SID del token di processo (non verranno apportate modifiche all'elenco dei gruppi di token di processo).<br/> |
| Senza restrizioni | Un SID dell'attività verrà derivato dal percorso completo dell'attività e verrà aggiunto all'elenco dei gruppi di token di processo.<br/>                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





