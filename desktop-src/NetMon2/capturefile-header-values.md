---
description: Definisce la struttura Network Monitor file di intestazione.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: CAPTUREFILE_HEADER_VALUES struttura (Netmon.h)
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
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367417"
---
# <a name="capturefile_header_values-structure"></a>Struttura CAPTUREFILE \_ HEADER \_ VALUES

La **struttura CAPTUREFILE \_ HEADER \_ VALUES** definisce la struttura Network Monitor file di intestazione.

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

Identificatore univoco: 'GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Decimale binario codificato (secondario). Il valore di questo membro deve essere zero (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Decimale codificato binario (principale). Questo valore deve essere 2.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo di topologia.

</dd> <dt>

**Timestamp**
</dt> <dd>

Ora di acquisizione.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Tabella dell'indice dei frame.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Dimensioni della tabella dell'indice dei frame.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Offset dei dati utente.

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

Offset della **struttura STATISTICS.**

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Lunghezza della **struttura STATISTICS.**

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Offset della **struttura NETWORKINFO.**

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Lunghezza della **struttura NETWORKINFO.**

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




