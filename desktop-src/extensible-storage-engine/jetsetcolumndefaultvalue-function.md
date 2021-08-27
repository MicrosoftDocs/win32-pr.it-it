---
description: Altre informazioni sulla funzione JetSetColumnDefaultValue
title: Funzione JetSetColumnDefaultValue
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402326a34a0551262d453b93db2287c69a7160b3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469718"
---
# <a name="jetsetcolumndefaultvalue-function"></a>Funzione JetSetColumnDefaultValue


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>Funzione JetSetColumnDefaultValue

La **funzione JetSetColumnDefaultValue** può essere usata per modificare il valore predefinito di una colonna esistente.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*Dbid*

Database da utilizzare per questa chiamata.

*szTableName*

Nome della tabella contenente la colonna che verrà interessata.

*szColumnName*

Nome della colonna il cui valore predefinito verrà modificato.

*pvData*

Buffer di input contenente il nuovo valore predefinito.

*cbData*

Dimensione del buffer di input contenente il nuovo valore predefinito.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Uguale a JET_errNullInvalid.</p> | 
| <p>JET_errColumnInUse</p> | <p>Questa colonna specificata è attualmente utilizzata da un indice.</p><p><strong>JetSetColumnDefaultValue non</strong> può modificare il valore predefinito di una colonna a cui viene fatto riferimento nella definizione di un indice. Ciò è dovuto al fatto che questa operazione potrebbe modificare il contenuto dell'indice.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna specificata non esiste per questa tabella.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L'ID database specificato non è valido.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi degli oggetti devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p><ul><li><p>I nomi degli oggetti devono essere costituiti da caratteri ASCII.</p></li><li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li><li><p>I nomi degli oggetti non possono superare JET_cbNameMost (64) caratteri.</p></li><li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li><li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li><li><p>I nomi degli oggetti non possono contenere un punto esclamativo (!), un punto (.), una parentesi quadra aperta ([) o una parentesi quadra chiusa (]).</p></li><li><p>Dopo la convalida, per il nome dell'oggetto verrà usata solo la parte della stringa fino al primo spazio (se presente). Ciò significa che anche i nomi degli oggetti non possono contenere uno spazio.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNullInvalid</p> | <p>Impossibile impostare la colonna su NULL. Ciò si verifica <strong>per JetSetColumnDefaultValue</strong> quando:</p><ul><li><p><em>cbData</em> è zero.</p></li><li><p><strong>pvData</strong> è NULL.</p></li></ul><p>Pertanto, non è possibile impostare il valore predefinito di una colonna (indietro) su NULL o su un valore di lunghezza zero.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La tabella specificata non esiste per questo database.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTableInUse</p> | <p>Questa tabella specificata è utilizzata da un'altra sessione.</p><p><strong>JetSetColumnDefaultValue</strong> richiede l'accesso esclusivo a una tabella per modificare il valore predefinito della colonna per le versioni precedenti Windows Server 2003.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Non è valido tentare un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errWriteConflict</p> | <p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. L'aggiornamento tentato da questa sessione avrà esito negativo.</p> | 



In caso di esito positivo, il valore predefinito della colonna specificata nella tabella specificata nel database specificato viene modificato in modo permanente nel nuovo valore predefinito.

In caso di errore, non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Non è possibile modificare il valore predefinito di una colonna in una tabella modello.

Il motore di database tronca automaticamente il valore predefinito di una colonna a 255 byte per le colonne long text e long binary.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetSetColumnDefaultValueW</strong> (Unicode) e <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
