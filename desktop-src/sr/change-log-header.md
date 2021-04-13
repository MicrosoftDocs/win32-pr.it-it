---
title: Struttura CHANGE_LOG_HEADER
description: Intestazione del log delle modifiche.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Ripristino del sistema della struttura CHANGE_LOG_HEADER
- Ripristino del sistema del puntatore della struttura PCHANGE_LOG_HEADER
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400292"
---
# <a name="change_log_header-structure"></a>MODIFICARE \_ la \_ struttura dell'intestazione del log

\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]

Intestazione del log delle modifiche.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**RecordHeader**
</dt> <dd>

Struttura [**di \_ intestazione**](record-header.md) di un record. Il membro **dwRecordType** deve essere impostato su RecordTypeLogHeader (0). Il membro **dwRecordSize** deve tenere conto di tutti i membri, più il valore **DWORD** aggiuntivo che segue questa intestazione. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Questo membro deve essere impostato su 0xabcdef12.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Questo membro deve essere impostato su 2.

</dd> <dt>

**Dataheader**
</dt> <dd>

Struttura [**di \_ intestazione**](record-header.md) di un record. Il membro **dwRecordType** deve essere impostato su **RecordTypeVolumePath** (2).

</dd> <dt>

**byteData**
</dt> <dd>

Inizio di una stringa con terminazione null che specifica il percorso del volume.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa intestazione è seguita da un valore **DWORD** che deve essere identico al valore del membro **dwRecordSize** di **RecordHeader**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                            |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                       |



 

 





