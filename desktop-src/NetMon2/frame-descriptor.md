---
description: La struttura FRAME \_ DESCRIPTOR fornisce informazioni descrittive sui frame non elaborati.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: FRAME_DESCRIPTOR struttura (Netmon.h)
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
ms.openlocfilehash: 1e675c07eae46096878e7c0aa71b53ba5bf22194e82ad8cc5aa5b6070d7e27e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938572"
---
# <a name="frame_descriptor-structure"></a>Struttura \_ FRAME DESCRIPTOR

La **struttura FRAME \_ DESCRIPTOR** fornisce informazioni descrittive sui frame non elaborati.

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

**Timestamp**
</dt> <dd>

Ora di sistema, in microsecondi, in cui è stato acquisito il frame. Questo tempo viene in genere usato per determinare l'intervallo tra i due fotogrammi acquisiti.

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

Nome del tipo.

</dd> <dt>

**Sap**
</dt> <dd>

Valore SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Indice del protocollo trovato.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Offset ai dati del protocollo ottenuti **da LowProtocol**.

</dd> <dt>

**HighPort**
</dt> <dd>

Porta del protocollo alto identificata in **LowProtocol.**

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




