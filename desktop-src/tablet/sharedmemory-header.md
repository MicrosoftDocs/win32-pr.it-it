---
description: Archivia informazioni sulle sezioni di memoria condivisa.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae596819feb4bd70aa47e7881521e5a69e5bd0a509b974e591d08907efda51c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966800"
---
# <a name="sharedmemory_header-structure"></a>Struttura SHAREDMEMORY \_ HEADER

Archivia informazioni sulle sezioni di memoria condivisa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**cbTotal**
</dt> <dd>

Dimensione, in byte, dei dati a cui fa riferimento questa struttura di intestazione.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

Dimensione, in byte, dell'offset dei numeri di serie rispetto alla struttura dell'intestazione.

</dd> <dt>

**idxEvent**
</dt> <dd>

Indice dell'evento. Questo valore viene incrementato con eventi successivi.

</dd> <dt>

**dwEvent**
</dt> <dd>

Evento associato a questa intestazione.

</dd> <dt>

**Cid**
</dt> <dd>

Identificatore di cursore a cui fa riferimento l'intestazione di memoria condivisa.

</dd> <dt>

**sn**
</dt> <dd>

Numero di serie per l'intestazione di memoria condivisa.

</dd> <dt>

**sysEvt**
</dt> <dd>

Evento di sistema, con edizione Standard \_ \* , associato a questa intestazione. Per altre informazioni, vedere la sezione osservazioni.

</dd> <dt>

**sysEvtData**
</dt> <dd>

Struttura [**SYSTEM \_ EVENT \_ DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associata all'evento di sistema.

</dd> <dt>

**cPackets**
</dt> <dd>

Conteggio dei pacchetti associati alla sezione di memoria condivisa corrente.

</dd> <dt>

**cbPackets**
</dt> <dd>

Dimensione, in byte, dei pacchetti associati alla sezione di memoria condivisa corrente.

</dd> <dt>

**fSnsPresent**
</dt> <dd>

Flag che indica se i numeri di serie sono presenti nella sezione corrente della memoria condivisa.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori seguenti sono definiti per il **membro sysEvt.**


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DATI \_ DEGLI EVENTI DI \_ SISTEMA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



