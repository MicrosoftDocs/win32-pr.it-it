---
description: Definisce un tipo stringa per il nome o la descrizione di un profilo del criterio LAN wireless.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo semplice nameType (LAN_policy)
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
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318261"
---
# <a name="nametype-simple-type-lan_policy"></a>Tipo semplice nameType (LAN_policy)

Il tipo semplice nameType definisce un tipo stringa per il nome o la descrizione di un profilo di criteri LAN wireless. I nomi e le descrizioni sono stringhe con almeno un carattere e una lunghezza massima di 255 caratteri.

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
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




