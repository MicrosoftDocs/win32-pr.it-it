---
title: Struttura MPRESOURCE_STATS (MpClient. h)
description: Statistiche correlate alle risorse.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Struttura MPRESOURCE_STATS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESOURCE_STATS
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477657"
---
# <a name="mpresource_stats-structure"></a>\_Struttura statistiche MPRESOURCE

Statistiche correlate alle risorse.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Members

<dl> <dt>

**PPMProgress**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Avanzamento approssimativo per l'analisi in ppm (parti per milione). Impostare su **MPPROGRESS \_ non valido** se le informazioni sullo stato non sono disponibili.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Tipo: **UInt64**

</dd> <dd>

Numero di processi analizzati.

</dd> <dt>

**FileCount**
</dt> <dd>

Tipo: **UInt64**

</dd> <dd>

Numero di file analizzati.

</dd> <dt>

**FileBytesCount**
</dt> <dd>

Tipo: **UInt64**

</dd> <dd>

Numero di byte analizzati per i file.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Tipo: **UInt64**

</dd> <dd>

Numero di RegKeys analizzati.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **UInt64 \[ 4 \]**

</dd> <dd>

Campi riservati per utilizzi futuri.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





