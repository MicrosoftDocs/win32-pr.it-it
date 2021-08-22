---
description: Definisce un tipo stringa per l'elemento ProviderName nel profilo Mobile Broadband.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo semplice providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744391"
---
# <a name="providernametype-simple-type"></a>Tipo semplice providerNameType

Il **tipo semplice providerNameType** definisce un tipo stringa per l'elemento [**ProviderName**](schema-providername-providertype-element.md) nel profilo Mobile Broadband. Questa stringa è lunga almeno un carattere e al massimo 20 caratteri.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




