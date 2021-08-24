---
description: Frame effettivo del driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Struttura FRAME (Netmon.h)
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
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910951"
---
# <a name="frame-structure"></a>Struttura FRAME

La **struttura FRAME** è un frame effettivo del driver.

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

**Timestamp**
</dt> <dd>

Tempo trascorso, in microsecondi, tra l'inizio dell'acquisizione e il momento in cui è stato acquisito il frame.

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




