---
description: Altre informazioni sulla funzione JetGetLogInfoInstance
title: Funzione JetGetLogInfoInstance
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c790a0aaaab1f9da3779a4852f879b0e3abb2d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472557"
---
# <a name="jetgetloginfoinstance-function"></a>Funzione JetGetLogInfoInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetloginfoinstance-function"></a>Funzione JetGetLogInfoInstance

La **funzione JetGetLogInfoInstance** viene usata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza per i nomi dei file di patch del database e dei file di log delle transazioni che devono diventare parte del set di file di backup. Questi file possono essere successivamente aperti usando [JetOpenFile](./jetopenfile-function.md) e letti con [JetReadFile](./jetreadfile-function.md).

**Windows XP: JetGetLogInfoInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.

*Szz*

Buffer di output che riceverà l'elenco di stringhe con terminazione Null che descrivono il set di file di patch del database e file di log delle transazioni che devono far parte del set di file di backup.

L'elenco di stringhe restituite in questo buffer ha lo stesso formato di una stringa multipla usata dal Registro di sistema. Ogni stringa con terminazione Null viene restituita in sequenza seguita da un terminatore Null finale.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve la quantità effettiva di dati stringa ricevuti nel buffer di output.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza. <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> restituirà questo errore se sono presenti handle di file in sospeso creati <a href="gg269249(v=exchg.10).md">usando JetOpenFile</a> per l'istanza.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, le informazioni richieste sul set di file di patch del database e sui file di log delle transazioni che devono far parte del set di file di backup verranno inserite nei buffer di output, se disponibili. La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito. Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.

In caso di errore, lo stato dei buffer di output non è definito. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza.

#### <a name="remarks"></a>Commenti

È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup. L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive di questo elenco e usare tali informazioni per determinare se l'elenco è stato troncato.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetLogInfoInstanceW</strong> (Unicode) e <strong>JetGetLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
