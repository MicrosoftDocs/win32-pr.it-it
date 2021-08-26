---
description: La struttura NMCOLUMNINFO definisce una colonna nel riquadro superiore del Visualizzatore eventi.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Struttura NMCOLUMNINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037121"
---
# <a name="nmcolumninfo-structure"></a>Struttura NMCOLUMNINFO

La **struttura NMCOLUMNINFO** definisce una colonna nel riquadro superiore del Visualizzatore eventi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**szColumnName**
</dt> <dd>

Nome visualizzabile di una colonna specifica. Se il nome è troppo lungo, non sarà completamente visibile nella configurazione Visualizzatore eventi predefinita.

</dd> <dt>

**VariantData**
</dt> <dd>

Dati inseriti nella colonna.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




