---
description: 'Altre informazioni su: Funzione JetStopBackup'
title: Funzione JetStopBackup
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd11857be7096ce30f2fcf06f8ab4f975185da57
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982364"
---
# <a name="jetstopbackup-function"></a>Funzione JetStopBackup


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>Funzione JetStopBackup

La **funzione JetStopBackup** impedisce a qualsiasi attività correlata al backup di streaming di continuare in un'istanza in esecuzione specifica, terminando così il backup di streaming in modo prevedibile.

**Windows XP:**  Questa funzione è stata introdotta in Windows XP.

[JetStopService è](./jetstopservice-function.md) la chiamata legacy quando è consentita una sola istanza. In questo caso, l'unica istanza attiva è quella preparata per la terminazione.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Non è chiaro quale istanza preparare per la terminazione quando si usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con la modalità a istanza multipla.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 



Se questa funzione ha esito positivo, l'istanza inizierà a non riuscire con le nuove API di backup di streaming.

Se questa funzione ha esito negativo, non verranno eseguiti passaggi per preparare la terminazione del backup nell'istanza e non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Il backup viene in genere attivato da un evento esterno al meccanismo del processo e, usando questa API, l'applicazione ESENT stessa effettua altre chiamate alle API di backup di streaming in modo che non riescano. La maggior parte delle API di backup di streaming inizierà a non riuscire con JET_errBackupAbortByServer. Di conseguenza, qualsiasi stato di avanzamento del backup del flusso (ad [esempio JetReadFileInstance](./jetreadfileinstance-function.md)) restituirà un errore. Le operazioni di backup che fanno parte della terminazione del backup ( ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) saranno comunque consentite.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
