---
description: Definisce un tipo di stringa per il profilo Mobile Broadband.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo semplice nameType (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: 9b07bfb62e23b0c82ef69bc924147675caad10d61258a5c49edc906c4b6bf2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881405"
---
# <a name="nametype-simple-type-mobile-broadband"></a>tipo semplice nameType (Mobile Broadband)

Il **tipo semplice nameType** definisce un tipo stringa per il profilo Mobile Broadband. Questa stringa è lunga almeno un carattere e al massimo 255 caratteri.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
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
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




