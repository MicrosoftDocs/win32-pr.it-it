---
description: Altre informazioni sulla funzione JetGetAttachInfo
title: Funzione JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0847fdef5b522a31192eeb153a286784f7bc73f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465058"
---
# <a name="jetgetattachinfo-function"></a>Funzione JetGetAttachInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetattachinfo-function"></a>Funzione JetGetAttachInfo

La **funzione JetGetAttachInfo** viene usata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza per i nomi dei file di database che devono diventare parte del set di file di backup. Verranno considerati solo i database attualmente collegati all'istanza [tramite JetAttachDatabase.](./jetattachdatabase-function.md) Questi file possono essere successivamente aperti usando [JetOpenFile](./jetopenfile-function.md) e letti con [JetReadFile](./jetreadfile-function.md).

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*Szz*

Buffer di output che riceve l'elenco di stringhe con terminazione Null che descrivono il set di file di database che deve far parte del set di file di backup. L'elenco di stringhe restituite in questo buffer ha lo stesso formato di una stringa multipla usata dal Registro di sistema. Ogni stringa con terminazione Null viene restituita in sequenza seguita da un terminatore Null finale.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Puntatore al buffer di output che ha ricevuto la quantità effettiva di dati stringa.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza. <strong>JetGetAttachInfo</strong> restituirà questo errore se il backup corrente non è un backup completo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Questo problema può verificarsi <strong>per JetGetAttachInfo</strong> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, le informazioni richieste sul set di file di database che devono far parte del set di file di backup verranno inserite nei buffer di output, se disponibili.

In caso di errore, lo stato dei buffer di output non è definito. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza.

#### <a name="remarks"></a>Commenti

È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup. L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive di questo elenco e usare tali informazioni per determinare se l'elenco è stato troncato.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetAttachInfoW</strong> (Unicode) e <strong>JetGetAttachInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
