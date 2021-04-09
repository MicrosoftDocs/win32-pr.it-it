---
description: Definisce un tipo stringa per gli identificatori dei set di servizi (SSID).
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
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968308"
---
# <a name="networknametype-simple-type"></a>Tipo semplice networkNameType

Il tipo semplice networkNameType definisce un tipo stringa per gli identificatori dei set di servizi (SSID). Un SSID è una stringa con una lunghezza di almeno un carattere e una lunghezza massima di 32 caratteri.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




