---
description: Definisce un tipo stringa per l'elemento ICONFilePath nel profilo Mobile Broadband.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo semplice iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129014"
---
# <a name="iconfiletype-simple-type"></a>Tipo semplice iconFileType

Il tipo semplice **iconFileType** definisce un tipo stringa per l'elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) nel profilo Mobile Broadband. Questa stringa ha una lunghezza compresa tra almeno un carattere e una lunghezza massima di 1024 caratteri.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




