---
description: La \_ struttura del descrittore di frame fornisce informazioni descrittive sui frame non elaborati.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Struttura FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305926"
---
# <a name="frame_descriptor-structure"></a>\_Struttura del descrittore di frame

La struttura del **\_ descrittore di frame** fornisce informazioni descrittive sui frame non elaborati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Members

<dl> <dt>

**FramePointer**
</dt> <dd>

Puntatore ai dati del frame.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Tempo di sistema, in microsecondi, quando il frame è stato acquisito. Questo tempo viene in genere usato per determinare l'intervallo tra l'acquisizione di due frame.

</dd> <dt>

**FrameLength**
</dt> <dd>

Lunghezza del frame.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Lunghezza effettiva del frame copiata.

</dd> <dt>

**Etype**
</dt> <dd>

Nome etype.

</dd> <dt>

**SAP**
</dt> <dd>

Valore SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Indice del protocollo trovato.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Offset ai dati del protocollo ottenuti da **LowProtocol**.

</dd> <dt>

**HighPort**
</dt> <dd>

Porta del protocollo elevato identificato in **LowProtocol**.

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Offset ai dati del protocollo ottenuti da **HighPort**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




