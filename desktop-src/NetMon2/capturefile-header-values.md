---
description: Definisce la struttura del file di intestazione Network Monitor.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Struttura CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311638"
---
# <a name="capturefile_header_values-structure"></a>\_ \_ Struttura dei valori dell'intestazione CAPTUREFILE

La struttura dei **\_ \_ valori dell'intestazione CAPTUREFILE** definisce la struttura del file di intestazione Network Monitor.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Members

<dl> <dt>

**Firma**
</dt> <dd>

Identificatore univoco:' GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binario, decimale codificato (minore). Il valore di questo membro deve essere zero (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Decimal codificato binario (principale). Questo valore deve essere 2.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo di topologia.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Ora di acquisizione.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Tabella dell'indice del frame.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Dimensioni tabella indice frame.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Offset dati utente.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Lunghezza dei dati utente.

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

Offset dei dati di commento.

</dd> <dt>

**CommentDataLength**
</dt> <dd>

Lunghezza dei dati di commento.

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

Offset alla struttura delle **statistiche** .

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Lunghezza della struttura delle **statistiche** .

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Offset alla struttura **NETWORKINFO** .

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Lunghezza della struttura **NETWORKINFO** .

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

Questo membro non viene utilizzato.

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

Questo membro non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




