---
description: Frame effettivo dal driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Struttura cornice (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305924"
---
# <a name="frame-structure"></a>Struttura FRAME

La struttura del **frame** è un frame effettivo dal driver.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Members

<dl> <dt>

**TimeStamp**
</dt> <dd>

Tempo trascorso, in microsecondi, tra l'inizio dell'acquisizione e l'ora in cui è stato acquisito il frame.

</dd> <dt>

**FrameLength**
</dt> <dd>

Lunghezza del frame MAC.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Lunghezza effettiva del frame copiata.

</dd> <dt>

**MacFrame**
</dt> <dd>

Dati del frame.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




