---
description: 'Altre informazioni: Funzione JetStopBackup'
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
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469698"
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

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Non è chiaro quale istanza preparare per la terminazione quando si usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con la modalità a più istanze.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 



Se questa funzione ha esito positivo, l'istanza inizierà a non riuscire con le nuove API di backup di streaming.

Se questa funzione ha esito negativo, non verrà eseguita alcuna procedura per preparare la terminazione del backup nell'istanza e non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Il backup viene in genere attivato da un evento esterno al meccanismo del processo e, usando questa API, l'applicazione ESENT stessa effettua altre chiamate alle API di backup di streaming in modo che non riescano. La maggior parte delle API di backup di streaming inizierà a non riuscire JET_errBackupAbortByServer. Di conseguenza, qualsiasi avanzamento del backup di streaming (ad esempio [JetReadFileInstance](./jetreadfileinstance-function.md)) restituirà un errore. Le operazioni di backup che fanno parte della terminazione del backup ( ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) saranno comunque consentite.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
