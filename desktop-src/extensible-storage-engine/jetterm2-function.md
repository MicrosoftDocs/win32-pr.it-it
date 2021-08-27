---
description: 'Altre informazioni su: Funzione JetTerm2'
title: Funzione JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9f8e5f278a0ef3eb44efd64314745d2fed6d89b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466618"
---
# <a name="jetterm2-function"></a>Funzione JetTerm2


_**Si applica a:** Windows | Windows Server_

## <a name="jetterm2-function"></a>Funzione JetTerm2

La **funzione JetTerm2** avvia l'arresto di un'istanza inizializzata da [JetInit.](./jetinit-function.md)

**JetTerm2 può** anche eliminare un'istanza non inizializzata creata da [JetCreateInstance.](./jetcreateinstance-function.md)

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **NULL.**

**Windows XP e versioni successive:**  Questo parametro è sottoposto a overload. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **NULL** o contenere l'istanza effettiva restituita da [JetInit.](./jetinit-function.md) Se il motore funziona in modalità a istanza multipla, questo parametro deve essere un puntatore a un'istanza creata usando [JetCreateInstance.](./jetcreateinstance-function.md)

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTermComplete</p> | <p>Richiede che l'istanza di sia arrestata in modo pulito. Tutte le operazioni di pulizia facoltative che normalmente vengono eseguite in background in fase di esecuzione vengono completate immediatamente.</p> | 
| <p>JET_bitTermAbrupt</p> | <p>Richiede che l'istanza di sia arrestata il più rapidamente possibile. Qualsiasi operazione facoltativa che normalmente verrebbe eseguita in background in fase di esecuzione viene abbandonata.</p><p><strong>Nota</strong>  Questa opzione può causare una perdita di spazio temporanea o permanente nel database. Questo spazio perso può sempre essere recuperato tramite una deframmentazione offline del database.</p> | 
| <p>JET_bitTermStopBackup</p> | <p>Richiede l'arresto dell'istanza anche se è attualmente in corso un backup. In genere, un backup in sospeso causa <a href="gg269298(v=exchg.10).md">l'esito</a> negativo di JetTerm con JET_errBackupInProgress. Quando questo parametro non è presente, si presuppone che il relativo valore sia JET_bitTermAbrupt.</p> | 
| <p>JET_bitTermDirty</p> | <p>Richiede che l'istanza di sia arrestata con tutti i database collegati rimasti in uno stato dirty.</p><p>Windows 7: JET_bitTermDirty è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di backup nell'istanza.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto. Questo errore verrà restituito da <a href="gg269298(v=exchg.10).md">JetTerm</a> quando il motore è in modalità a istanza multipla e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché l'istanza è in fase di arresto.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>Impossibile arrestare l'istanza perché esistono attualmente sessioni con transazioni attive per l'istanza specificata. Questo errore si verifica solo se viene JET_bitTermComplete'oggetto .</p> | 



Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata. Anche l'handle di istanza verrà chiuso e reso non disponibile per qualsiasi API che accetta un handle di istanza. Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni. Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.

Se questa funzione ha esito negativo a causa di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non viene modificato nulla. In caso contrario, l'istanza viene comunque arrestata come indicato per il caso di esito positivo. La differenza è che l'istanza dovrà eseguire il ripristino in caso di arresto anomalo del sistema alla successiva inizializzazione. Il motore tenterà di scaricare il maggior numero possibile di dati per ridurre al minimo la quantità di ripristino necessaria. Concettualmente, un errore di questo tipo di [JetTerm](./jetterm-function.md) non è diverso da un arresto anomalo del processo.

#### <a name="remarks"></a>Commenti

Vedere [JetTerm.](./jetterm-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
