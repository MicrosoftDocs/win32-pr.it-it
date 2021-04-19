---
description: Definisce un tipo stringa per il profilo a banda larga mobile.
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
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307537"
---
# <a name="nametype-simple-type-mobile-broadband"></a>tipo semplice nameType (Mobile Broadband)

Il tipo semplice **nameType** definisce un tipo stringa per il profilo Mobile Broadband. Questa stringa ha una lunghezza compresa tra almeno un carattere e una lunghezza massima di 255 caratteri.

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
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




