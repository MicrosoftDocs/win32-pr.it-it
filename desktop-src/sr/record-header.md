---
title: Struttura RECORD_HEADER
description: Intestazione del record utilizzata dalla voce del \_ registro delle modifiche e dalle strutture dell'intestazione del log delle \_ modifiche \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Ripristino del sistema della struttura RECORD_HEADER
- Ripristino del sistema del puntatore della struttura PRECORD_HEADER
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478292"
---
# <a name="record_header-structure"></a>Struttura di intestazione del RECORD \_

\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]

Intestazione del record utilizzata dalla [**voce del \_ registro \_ delle modifiche**](change-log-entry.md) e dalle strutture dell' [**\_ \_ intestazione del log delle modifiche**](change-log-header.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**dwRecordSize**
</dt> <dd>

Dimensioni totali del record, inclusa l'intestazione, in byte.

</dd> <dt>

**dwRecordType**
</dt> <dd>

Tipo di record. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**RecordTypeLogHeader**</dt> <dt>0</dt> </dl>     | Il record è l'intestazione del log delle modifiche.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**RecordTypeLogEntry**</dt> <dt>1</dt> </dl>         | Il record è l'intestazione di una voce del log delle modifiche.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**RecordTypeVolumePath**</dt> <dt>2</dt> </dl> | I dati sono il percorso del volume per la voce del log delle modifiche.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**RecordTypeFirstPath**</dt> <dt>3</dt> </dl>     | I dati sono il percorso del file per la voce del log delle modifiche.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**RecordTypeSecondPath**</dt> <dt>4</dt> </dl> | I dati vengono utilizzati durante la ridenominazione delle voci del log delle modifiche. Questo percorso è la posizione in cui è archiviato il file rinominato.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**RecordTypeTempPath**</dt> <dt>5</dt> </dl>         | I dati sono il nome del file di backup utilizzato per ripristinare la voce del log delle modifiche. I file di backup si trovano nella cartella RP *n* . Il nome del file ha il formato seguente: un *xxxxxxx*. *ext*, dove *xxxxxxx* è un numero a sette cifre ed *ext* è l'estensione del nome di file.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**RecordTypeAclInline**</dt> <dt>6</dt> </dl>     | I dati sono un ACL. Il formato dei dati è una struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Questo valore non può essere superiore a 8.192 byte. Per specificare un valore maggiore di 8.192 byte, usare il membro **RecordTypeAclFile** .<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**RecordTypeAclFile**</dt> <dt>7</dt> </dl>             | I dati sono il nome del file ACL usato per archiviare l'ACL. I file ACL si trovano nella cartella RP *n* . Il nome del file ha il formato seguente: S *xxxxxxx*. ACL, dove *xxxxxxx* è un numero a sette cifre.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**RecordTypeDebugInfo**</dt> <dt>8</dt> </dl>     | I dati sono informazioni di debug per la voce del log delle modifiche. Il formato dei dati è una struttura di **\_ informazioni di \_ debug \_ del log SR** . Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**RecordTypeShortName**</dt> <dt>9</dt> </dl>     | I dati sono il nome breve del file di backup.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura delle **\_ informazioni di \_ debug \_ del log SR** è definita come indicato di seguito.

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                            |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                       |



 

