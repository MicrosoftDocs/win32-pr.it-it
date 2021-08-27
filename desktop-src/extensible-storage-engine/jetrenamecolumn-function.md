---
description: 'Altre informazioni su: Funzione JetRenameColumn'
title: Funzione JetRenameColumn
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c60418a0723214b2d2312ebe67a4f47184814e0a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470238"
---
# <a name="jetrenamecolumn-function"></a>Funzione JetRenameColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>Funzione JetRenameColumn

La **funzione JetRenameColumn** può essere usata per modificare il nome di una colonna esistente in una tabella.

**Windows XP:****JetRenameColumn** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*Szname*

Nome corrente della colonna che verrà rinominata.

*szNameNew*

Nuovo nome della colonna che verrà rinominata.

*grbit*

Questo parametro deve essere 0.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna specificata non esiste per questa tabella.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi degli oggetti devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p><ul><li><p>I nomi degli oggetti devono essere costituiti da caratteri ASCII.</p></li><li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li><li><p>I nomi degli oggetti non possono superare JET_cbNameMost (64) caratteri.</p></li><li><p>I nomi degli oggetti non possono iniziare con uno spazio. I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li><li><p>I nomi degli oggetti non possono contenere un punto esclamativo (!), un punto (.), una parentesi quadra aperta ([) o una parentesi quadra chiusa (]).</p></li><li><p>Dopo la convalida, per il nome dell'oggetto verrà usata solo la parte della stringa fino al primo spazio (se presente). Ciò significa che anche i nomi degli oggetti potrebbero non contenere uno spazio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi <strong>per JetRenameColumn</strong> quando:</p><ul><li><p><em>szName</em> è NULL.</p></li><li><p><em>szNameNew</em> è NULL.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInTransaction</p> | <p>Questa operazione può essere eseguita solo quando la sessione non si trova attualmente all'interno di una transazione.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Non è possibile eseguire un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 



In caso di esito positivo, il nome della colonna specificata nella tabella associata al cursore viene modificato in modo permanente nel nuovo nome. Verranno aggiornati anche tutti gli indici che fanno riferimento a tale colonna.

In caso di errore, non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

L'operazione di ridenominazione della colonna è insolita perché, a differenza di altre operazioni sullo schema, non viene eseguita come transazione. Quando una colonna in una determinata tabella viene rinominata in una sessione, qualsiasi altra sessione che usa tale tabella visualizza immediatamente la modifica, anche se si trova in una transazione che impedirebbe a tale sessione di visualizzare qualsiasi altra modifica apportata dalla sessione durante l'operazione di ridenominazione.

L'ID di colonna di una colonna non è interessato dall'operazione di ridenominazione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
