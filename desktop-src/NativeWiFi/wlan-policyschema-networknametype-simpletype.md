---
description: Definisce un tipo di stringa per gli identificatori di set di servizi (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Tipo semplice networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f653c84f36730ed9f6f078b3713dde414fbf63469bd4ea43f632842d33d7e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064751"
---
# <a name="networknametype-simple-type"></a>Tipo semplice networkNameType

Il tipo semplice networkNameType definisce un tipo stringa per gli identificatori di set di servizi (SSID). Un SSID è una stringa lunga almeno un carattere e lunga al massimo 32 caratteri.

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




