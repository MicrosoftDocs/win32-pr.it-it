---
description: Definisce il tipo utilizzato per specificare i valori validi per il colore di determinati elementi in un file XML del journal.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo semplice ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305695"
---
# <a name="colortype-simple-type"></a>Tipo semplice ColorType

Definisce il tipo utilizzato per specificare i valori validi per il colore di determinati elementi in un file XML del journal.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Commenti

Un colore può essere un valore RGB esadecimale nel formato \# RRGGBB. Deve corrispondere all'espressione regolare seguente: \# \[ 0-9A-fa-F \] {6} . Ad esempio: " \# 4a79B5".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




