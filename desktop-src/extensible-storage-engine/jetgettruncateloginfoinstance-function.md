---
description: 'Altre informazioni su: Funzione JetGetTruncateLogInfoInstance'
title: Funzione JetGetTruncateLogInfoInstance
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36583267277f7c5254adc85047ce99631f6c03ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479077"
---
# <a name="jetgettruncateloginfoinstance-function"></a>Funzione JetGetTruncateLogInfoInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetgettruncateloginfoinstance-function"></a>Funzione JetGetTruncateLogInfoInstance

La funzione **JetGetTruncateLogInfoInstance** viene usata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza per i nomi dei file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.

**Windows XP:****JetGetTruncateLogInfoInstance** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

*Szz*

Buffer di output che riceve l'elenco di stringhe con terminazione Null che descrivono il set di file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.

L'elenco di stringhe restituite in questo buffer è nello stesso formato di una stringa multipla usata dal Registro di sistema. Ogni stringa con terminazione Null viene restituita in sequenza e seguita da un terminatore Null finale.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Puntatore al buffer di output che riceve la quantità effettiva di dati stringa.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</p><p><strong>Windows XP e versioni successive:</strong>  Questa operazione può verificarsi <strong>per JetGetTruncateLogInfoInstance</strong> quando l'handle di istanza specificato non è valido.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a></p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p><strong>JetGetTruncateLogInfoInstance</strong></p> | <p>Sono presenti handle di file in sospeso creati usando <a href="gg269249(v=exchg.10).md">JetOpenFile per</a> l'istanza.</p> | 



Se questa funzione ha esito positivo, le informazioni richieste sul set di file di log delle transazioni che possono essere eliminate in modo sicuro dopo il completamento del backup verranno inserite nei buffer di output in cui vengono forniti. La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito. Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.

Se questa funzione ha esito negativo, lo stato dei buffer di output non è definito. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza.

#### <a name="remarks"></a>Commenti

Questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup. L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive di questo elenco e usare tali informazioni per determinare se l'elenco è stato troncato.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) e <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
