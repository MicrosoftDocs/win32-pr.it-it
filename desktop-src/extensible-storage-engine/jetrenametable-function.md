---
description: Altre informazioni sulla funzione JetRenameTable
title: Funzione JetRenameTable
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d91f7af4896e5cb3145321de087a2803aaddd09
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985744"
---
# <a name="jetrenametable-function"></a>Funzione JetRenameTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetrenametable-function"></a>Funzione JetRenameTable

La **funzione JetRenameTable** può essere usata per modificare il nome di una tabella esistente.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*Dbid*

Database da utilizzare per questa chiamata.

*Szname*

Nome corrente della tabella che verrà rinominata.

*szNameNew*

Nuovo nome della tabella che verrà rinominata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Il database specificato non è valido.</p><p>Questo errore viene restituito solo in Windows 2000 quando viene tentata un'operazione di ridenominazione della tabella nel database temporaneo. JET_errInvalidDatabaseId restituito per questo caso nelle versioni successive.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L'ID database specificato non è valido.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi degli oggetti devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p><ul><li><p>I nomi degli oggetti devono essere costituiti da caratteri ASCII.</p></li><li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li><li><p>I nomi degli oggetti non possono superare JET_cbNameMost (64) caratteri.</p></li><li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li><li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li><li><p>I nomi degli oggetti non possono contenere un punto esclamativo (!), un punto (.), una parentesi quadra aperta ([) o una parentesi quadra chiusa (]): dopo la convalida, per il nome dell'oggetto verrà usata solo la parte della stringa fino al primo spazio (se presente). Ciò significa che anche i nomi degli oggetti potrebbero non contenere uno spazio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi <strong>per JetRenameTable</strong> quando:</p><ul><li><p><em>szName</em> è NULL.</p></li><li><p><em>szNameNew</em> è NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La tabella specificata non esiste per questo database.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Non è possibile eseguire un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 



In caso di esito positivo, il nome della tabella specificata nel database specificato viene modificato in modo permanente nel nuovo nome.

In caso di errore, non verrà apportata alcuna modifica allo stato del database.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetRenameTableW</strong> (Unicode) e <strong>JetRenameTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
