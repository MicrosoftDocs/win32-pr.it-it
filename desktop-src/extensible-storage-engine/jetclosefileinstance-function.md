---
description: Altre informazioni sulla funzione JetCloseFileInstance
title: Funzione JetCloseFileInstance
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d837d1932559c39d6a3b249f934ef77cc56de11a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982980"
---
# <a name="jetclosefileinstance-function"></a>Funzione JetCloseFileInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetclosefileinstance-function"></a>Funzione JetCloseFileInstance

La **funzione JetCloseFileInstance** chiude un file aperto con [JetOpenFileInstance](./jetopenfileinstance-function.md) dopo l'estrazione dei dati da tale file [tramite JetReadFileInstance](./jetreadfileinstance-function.md).

**Windows XP: JetCloseFileInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo JET_errRunningInMultiInstanceMode.

*hfFile*

Handle del file da leggere.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto oppure la combinazione di diversi valori di parametro ha restituito un risultato imprevisto. Questo problema può verificarsi <strong>per JetCloseFileInstance</strong> quando:</p><ul><li><p>L'handle di istanza specificato non è valido (Windows XP e versioni successive)</p></li><li><p>L'handle di file specificato non è valido</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di file viene chiuso. Se un file di database è stato chiuso, il file di patch del database associato (se presente) viene eliminato.

In caso di errore, non viene apportata alcuna modifica.

#### <a name="remarks"></a>Commenti

Il motore di database attualmente supporta solo un file aperto tramite [JetOpenFileInstance](./jetopenfileinstance-function.md) alla volta. Se un handle di file viene aperto [usando JetOpenFileInstance,](./jetopenfileinstance-function.md) è necessario chiuderlo usando **JetCloseFileInstance** prima di poter aprire un altro file.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
