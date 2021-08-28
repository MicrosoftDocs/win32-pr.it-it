---
description: 'Altre informazioni su: Parametri di backup e ripristino'
title: Parametri di backup e ripristino
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6b82d3ffa1f55d79ac516ede469d422e7aced99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982964"
---
# <a name="backup-and-restore-parameters"></a>Parametri di backup e ripristino


_**Si applica a:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Parametri di backup e ripristino

Questo argomento contiene i parametri utilizzati per il backup e il ripristino.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Il percorso completo di ogni database viene salvato in modo permanente nei log delle transazioni in fase di esecuzione. In genere, questi database devono rimanere nella posizione originale per il corretto funzionamento della riproduzione delle transazioni. Questo parametro può essere utilizzato per forzare il recupero con arresto anomalo del sistema o un'operazione di ripristino per cercare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>""</p> | 
| <p>Digitare:</p> | <p>Percorso cartella (stringa)</p> | 
| <p>Intervallo valido:</p> | <p>Da 0 a 246 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Questo parametro controlla il risultato di [JetInit](./jetinit-function.md) quando il motore di database è configurato per iniziare a usare file di log delle transazioni su disco di dimensioni diverse da quelle configurate. In [genere, JetInit](./jetinit-function.md) recupererà correttamente i database, ma avrà esito JET_errLogFileSizeMismatchDatabasesConsistent per indicare che le dimensioni del file di log non sono configurate correttamente. Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i file di log precedente, avvia un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate e restituirà JET_errSuccess.

Questo parametro è utile quando l'applicazione vuole modificare in modo trasparente le dimensioni del file di log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Quando questo parametro è true, tutti i file di log delle transazioni trovati su disco che non fanno parte della sequenza corrente di file di log verranno eliminati da [JetInit.](./jetinit-function.md) Può essere usato per pulire automaticamente i file di log estranei dopo un'operazione di ripristino.

**Windows XP:**  Introdotto in Windows XP.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Questo parametro configura la quantità di tempo consentita tra una chiamata a [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) [e JetOSSnapshotThaw](./jetossnapshotthaw-function.md) prima che si verifichi un timeout. Per altre [informazioni, vedere JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) Il timeout è espresso in millisecondi.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>20000 (Windows XP e Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Quando questo parametro è true, ogni pagina di un database sottoposto a un backup di streaming verrà eliminata. È importante notare che le pagine di database di cui si sta per eseguire lo scrubbing sono su disco. Il backup completo del set di dati viene eseguito prima del processo di scrubbing.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
