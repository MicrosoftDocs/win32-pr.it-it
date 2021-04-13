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
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526022"
---
# <a name="providernametype-simple-type"></a>Tipo semplice providerNameType

Il tipo semplice **providerNameType** definisce un tipo stringa per l'elemento [**providerName**](schema-providername-providertype-element.md) nel profilo Mobile Broadband. Questa stringa ha una lunghezza compresa tra almeno un carattere e un massimo di 20 caratteri.

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
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




