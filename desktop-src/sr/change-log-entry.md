---
title: CHANGE_LOG_ENTRY struttura
description: Voce del log delle modifiche.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- CHANGE_LOG_ENTRY struttura Ripristino configurazione di sistema
- PCHANGE_LOG_ENTRY puntatore alla struttura Ripristino configurazione di sistema
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee4eca1bad0859159821d7717ba6c23c352e03b33a1fcab81721e08dba465c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452932"
---
# <a name="change_log_entry-structure"></a>Struttura CHANGE \_ LOG \_ ENTRY

\[Queste informazioni si applicano solo Windows XP con Service Pack 2 (SP2).\]

Voce del log delle modifiche.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**RecordHeader**
</dt> <dd>

Struttura [**RECORD \_ HEADER.**](record-header.md) Il **membro dwRecordType** deve essere impostato su **RecordTypeLogEntry** (1).

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Questo membro deve essere impostato su 0xabcdef12.

</dd> <dt>

**dwEntryType**
</dt> <dd>

Questo membro può essere uno dei valori seguenti:

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ACLCHANGE** (0x2)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ATTRCHANGE** (0x4)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRCREATE** (0x80)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRRENAME** (0x100)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ DIRDELETE** (0x200)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILECREATE** (0x20)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILEDELETE** (0x10)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ FILERENAME** (0x40)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ INPRECREATE** (0x100000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ISDIR** (0x20000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ ISNOTDIR** (0x40000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTCREATE** (0x400)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ MOUNTDELETE** (0x800)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ NOOPTIMIZE** (0x10000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ OPENBYID** (0x200000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ SIMULATEDELETE** (0x80000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCHANGE** (0x1)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMCREATE** (0x2000)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ STREAMOVERWRITE** (0x8)**
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

CHANGE \_ LOG \_ ENTRYTYPES \_ VOLUMEERROR** (0x1000)**
</dt> </dl> </dd> <dt>

**dwEntryFlags**
</dt> <dd>

Questo membro può essere uno dei valori seguenti:

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ ACLINFO (0x4)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ DEBUGINFO (0x8)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ SECONDPATH (0x2)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ SHORTNAME (0x10)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

**CHANGE \_ LOG \_ ENTRYFLAGS \_ TEMPPATH (0x1)**
</dt> </dl> </dd> <dt>

**Attributi dwAttributes**
</dt> <dd>

Attributi del file di log delle modifiche. Se non viene specificato alcun attributo, questo valore deve essere impostato su 0xFFFFFFFF.

</dd> <dt>

**i64SequenceNum**
</dt> <dd>

Numero di sequenza assegnato alla voce del log delle modifiche.

</dd> <dt>

**szProcName**
</dt> <dd>

Nome del processo che apporta la modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura è seguita da un numero variabile di record di dati a lunghezza variabile e da un valore **DWORD** che deve essere identico al valore del membro **dwRecordSize** di **RecordHeader**.

I record di dati a lunghezza variabile sono costituiti da una struttura [**RECORD \_ HEADER**](record-header.md) e da dati che possono essere utilizzati per ripristinare la voce del log delle modifiche. Il formato dei dati dipende dal valore del membro **dwRecordType** della struttura **RECORD \_ HEADER.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                            |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                       |



 

 





