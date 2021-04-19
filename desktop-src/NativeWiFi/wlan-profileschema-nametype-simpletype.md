---
description: Includere il nome o una descrizione di un profilo LAN wireless.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Tipo semplice nameType (LAN_policy) (profilo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334340"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>Tipo semplice nameType (LAN_policy) per profileschema

Il tipo semplice nameType può contenere il nome o una descrizione di un profilo LAN wireless. Il valore della stringa deve avere una lunghezza compresa tra 1 e 255 caratteri.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



 

 




