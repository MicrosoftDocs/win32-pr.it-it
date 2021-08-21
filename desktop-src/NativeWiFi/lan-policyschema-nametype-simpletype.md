---
description: Definisce un tipo di stringa per il nome o la descrizione di un profilo criteri LAN cablato.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: tipo semplice nameType (LAN_policy)
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
ms.openlocfilehash: 3b3d558717777c9b2bead2fd7e141dee38b22491af4142d4948c7f1f76aadfd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065111"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo semplice nameType (LAN_policy)

Il tipo semplice nameType definisce un tipo stringa per il nome o la descrizione di un profilo criteri LAN cablato. I nomi e le descrizioni sono stringhe lunghe almeno un carattere e al massimo 255 caratteri.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




