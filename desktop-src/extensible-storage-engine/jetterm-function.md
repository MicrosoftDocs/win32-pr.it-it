---
description: 'Altre informazioni su: Funzione JetTerm'
title: Funzione JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832f98d32f164e91cd9dfc8befac4cbd0e518632
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481157"
---
# <a name="jetterm-function"></a>Funzione JetTerm


_**Si applica a:** Windows | Windows Server_

## <a name="jetterm-function"></a>Funzione JetTerm

La **funzione JetTerm** avvia l'arresto di un'istanza inizializzata da [JetInit](./jetinit-function.md).

**È anche** possibile usare JetTerm per eliminare un'istanza non inizializzata creata da [JetCreateInstance.](./jetcreateinstance-function.md)

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Specifica l'istanza di da utilizzare per questa chiamata.

**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **NULL.**

**Windows XP e versioni successive:**  Questo parametro è sottoposto a overload. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **NULL** o potrebbe contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md). Se il motore funziona in modalità a più istanze, questo parametro deve essere un puntatore a un'istanza creata tramite [JetCreateInstance](./jetcreateinstance-function.md).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto oppure la combinazione di diversi parametri ha restituito un risultato imprevisto. Questo errore verrà restituito da <strong>JetTerm</strong> quando il motore è in modalità a più istanze e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché l'istanza è in fase di arresto.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di .</p> | 
| <p>JET_errBackupInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di backup nell'istanza di .</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>Impossibile arrestare l'istanza perché sono attualmente presenti sessioni con transazioni attive per l'istanza specificata. Questo errore si verifica solo se JET_bitTermComplete viene usato .</p> | 



Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata. Anche l'handle dell'istanza verrà chiuso e reso non disponibile per qualsiasi API che accetta un handle di istanza. Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni. Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.

Se questa funzione ha esito negativo come risultato di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non cambia nulla. In caso contrario, l'istanza viene comunque arrestata in base al caso di esito positivo. La differenza è che l'istanza dovrà eseguire il ripristino dell'arresto anomalo del sistema alla successiva inizializzazione. Il motore tenterà di scaricare il maggior numero possibile di dati per ridurre al minimo la quantità di ripristino necessaria. Concettualmente, tale errore di **JetTerm** non è diverso da un arresto anomalo del processo.

#### <a name="remarks"></a>Commenti

Se il processo host di un'istanza viene chiuso per qualsiasi motivo prima che **JetTerm** venga chiamato correttamente su tale istanza, l'istanza viene considerata in uno stato di arresto anomalo. Il ripristino dell'arresto anomalo del sistema si verificherà al successivo tentativo di inizializzare l'istanza.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
