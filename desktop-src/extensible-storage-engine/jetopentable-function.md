---
description: Altre informazioni sulla funzione JetOpenTable
title: Funzione JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 816bed58b4c886cc2e9984a44e1e4e10f7768f4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472522"
---
# <a name="jetopentable-function"></a>Funzione JetOpenTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentable-function"></a>Funzione JetOpenTable

La **funzione JetOpenTable** apre un cursore su una tabella creata in precedenza.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da utilizzare.

*Dbid*

Identificatore del database da utilizzare per trovare la tabella.

*szTableName*

Nome della tabella da aprire.

*pvParameters*

Deprecato. Impostare su **NULL.**

*cbParameters*

Deprecato. Impostare su 0 (zero).

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTableDenyRead</p> | <p>La tabella non può essere aperta per l'accesso in lettura da un'altra sessione di database.</p> | 
| <p>JET_bitTableDenyWrite</p> | <p>La tabella non può essere aperta per l'accesso in scrittura da un'altra sessione di database.</p> | 
| <p>JET_bitTableNoCache</p> | <p>Non memorizzare nella cache le pagine per questa tabella.</p> | 
| <p>JET_bitTablePermitDDL</p> | <p>Consente la modifica DDL nelle tabelle contrassegnate come FixedDDL. Questa opzione deve essere usata con l'JET_bitTableDenyRead predefinita.</p> | 
| <p>JET_bitTablePreread</p> | <p>Fornisce un hint che indica che la tabella probabilmente non si trova nella cache del buffer e che la pre-lettura può essere vantaggiosa per le prestazioni.</p> | 
| <p>JET_bitTableReadOnly</p> | <p>Richiede l'accesso in sola lettura alla tabella.</p> | 
| <p>JET_bitTableSequential</p> | <p>La tabella deve essere preletturata in modo molto aggressivo dal disco perché l'applicazione la analerà in sequenza.</p> | 
| <p>JET_bitTableUpdatable</p> | <p>Richiede l'accesso in scrittura alla tabella.</p> | 



*ptableid*

In caso di esito positivo, punta all'identificatore della tabella. In caso di errore, il contenuto di *ptableid* non è definito.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p><em>dbid non</em> è un identificatore di database valido.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>È stata passata una combinazione non valida di <em>grbit.</em></p> | 
| <p>JET_errInvalidName</p> | <p>Il nome specificato in <em>szTableName</em> non è valido.</p><p>Per altre informazioni sui nomi di tabella validi, vedere il <em>parametro szTableName</em> in <a href="gg269210(v=exchg.10).md">JetCreateTable.</a></p> | 
| <p>JET_errObjectNotFound</p> | <p>Si è tentato di aprire una tabella che non esiste nel database.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Vedere la sezione relativa alle osservazioni.</p> | 
| <p>JET_errTableInUse</p> | <p>La tabella è utilizzata da un'altra operazione di database.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Avviso non irreversibile che indica che la tabella viene utilizzata dal sistema.</p> | 
| <p>JET_errTableLocked</p> | <p>La tabella è bloccata da un'altra operazione di database.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Si è tentato di aprire troppe tabelle univoche contemporaneamente. Vedere la sezione relativa alle osservazioni.</p> | 



#### <a name="remarks"></a>Commenti

Le tabelle aperte **con JetOpenTable** devono in genere essere chiuse [con JetCloseTable.](./jetclosetable-function.md) L'eccezione a questa regola si verifica quando **JetOpenTable** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback).](./jetrollback-function.md) Quando si esegue il rollback di una transazione, la tabella viene chiusa automaticamente. In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).

È possibile aprire tabelle di sistema **con JetOpenTable,** ad esempio MSysObjects, MSysUnicodeFixup. Lo schema delle tabelle di sistema può cambiare, pertanto l'accesso alle tabelle di sistema è sconsigliato. Il numero di tabelle univoche che possono essere aperte contemporaneamente è influenzato direttamente da *JET_paramMaxOpenTables*. Se la tabella è attualmente aperta, verrà creato un nuovo cursore sulla tabella. Le risorse cursore vengono [configurate usando JetSetSystemParameter](./jetsetsystemparameter-function.md) *con JET_paramMaxCursors*. Vedere anche [JetDupCursor.](./jetdupcursor-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)
