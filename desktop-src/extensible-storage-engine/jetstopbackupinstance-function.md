---
description: Altre informazioni sulla funzione JetStopBackupInstance
title: Funzione JetStopBackupInstance
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987244"
---
# <a name="jetstopbackupinstance-function"></a>Funzione JetStopBackupInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopbackupinstance-function"></a>Funzione JetStopBackupInstance

La **funzione JetStopBackupInstance** impedisce che l'attività correlata al backup di streaming continui in un'istanza in esecuzione specifica, terminando così il backup di flusso in modo prevedibile.

**Windows XP:****JetStopBackupInstance** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Identifica l'istanza in esecuzione da usare per la chiamata API.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il parametro di istanza specificato ha un valore non valido (non un'istanza attualmente in esecuzione).</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 



Se questa funzione ha esito positivo, l'istanza specificata inizierà a non riuscire con le nuove API di backup di streaming.

Se questa funzione ha esito negativo, non verranno eseguiti passaggi per preparare la terminazione del backup nell'istanza e non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Il backup viene in genere attivato da un evento esterno al meccanismo del processo e, usando questa API, l'applicazione ESENT stessa effettua altre chiamate alle API di backup di streaming in modo che non riescano. La maggior parte delle API di backup di streaming inizierà a non riuscire con JET_errBackupAbortByServer. Di conseguenza, qualsiasi stato di avanzamento del backup del flusso (ad [esempio JetReadFileInstance](./jetreadfileinstance-function.md)) restituirà un errore. Le operazioni di backup che fanno parte della terminazione del backup ( ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) saranno comunque consentite.

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
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
