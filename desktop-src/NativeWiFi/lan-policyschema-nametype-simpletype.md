---
description: Definisce un tipo stringa per il nome o la descrizione di un profilo di criteri LAN cablata.
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967897"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo semplice nameType (LAN_policy)

Il tipo semplice nameType definisce un tipo stringa per il nome o la descrizione di un profilo di criteri LAN cablata. I nomi e le descrizioni sono stringhe con almeno un carattere e una lunghezza massima di 255 caratteri.

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



 

 




