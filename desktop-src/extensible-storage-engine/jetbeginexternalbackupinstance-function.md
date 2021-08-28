---
description: Altre informazioni sulla funzione JetBeginExternalBackupInstance
title: Funzione JetBeginExternalBackupInstance
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95d74873fabfe27bc9750f074cd656b17e04803e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988080"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Funzione JetBeginExternalBackupInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetbeginexternalbackupinstance-function"></a>Funzione JetBeginExternalBackupInstance

La **funzione JetBeginExternalBackupInstance** avvia un backup esterno mentre il motore e il database sono online e attivi.

**Windows XP: JetBeginExternalBackupInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza del database da utilizzare per questa chiamata.

Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo JET_errRunningInMultiInstanceMode.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Questo flag è deprecato. L'utilizzo di questo bit comporta la JET_errInvalidgrbit restituito.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log dopo l'ultimo backup completo o incrementale.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Riservato per utilizzi futuri. Definito per Windows XP.</p> | 



### <a name="return-value"></a>Valore restituito

Il sistema può generare codici di esito positivo o negativo in seguito a una chiamata a questa funzione. Per un elenco completo degli errori per questa API, vedere Codici di errore del motore Archiviazione [extensible](./extensible-storage-engine-error-codes.md).

Vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Commenti

**JetBeginExternalBackupInstance** è la prima funzione di una serie di funzioni che devono essere chiamate per eseguire correttamente un backup online (non basato su VSS). Vedere anche [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) e [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Un backup esterno può essere usato per implementare backup completi, incrementali o differenziali.

Il backup sarà fuzzy, in quanto il backup sarà coerente con un singolo punto nel tempo nella cronologia delle transazioni, ma al momento non è possibile controllare il punto esatto nel tempo.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
