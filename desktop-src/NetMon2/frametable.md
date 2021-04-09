---
description: La struttura FRAMETABLE, un buffer circolare di puntatori ai frame, viene restituita alle applicazioni collegate all'interfaccia ITRC dell'oggetto NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Struttura FRAMETABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128351"
---
# <a name="frametable-structure"></a>Struttura FRAMETABLE

La struttura **Frametable** , un buffer circolare di puntatori ai frame, viene restituita alle applicazioni collegate all'interfaccia **itrc** dell'oggetto NPP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**FrameTableLength**
</dt> <dd>

Lunghezza totale della tabella.

</dd> <dt>

**StartIndex**
</dt> <dd>

Primo indice all'interno della tabella.

</dd> <dt>

**EndIndex**
</dt> <dd>

Ultimo indice all'interno della tabella.

</dd> <dt>

**FrameCount**
</dt> <dd>

Numero di frame descritti da questa tabella.

</dd> <dt>

**Frame**
</dt> <dd>

Matrice effettiva di descrittori di frame.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




