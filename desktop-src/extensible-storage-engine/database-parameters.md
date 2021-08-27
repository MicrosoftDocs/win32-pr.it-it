---
description: 'Altre informazioni su: Parametri di database'
title: Parametri del database
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: cdccfca7e7a68ea997c9b564939f89799634e344
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471837"
---
# <a name="database-parameters"></a>Parametri del database


_**Si applica a:** Windows | Windows Server_

## <a name="database-parameters"></a>Parametri del database

In questo argomento sono contenuti i parametri utilizzati per il database.

*JET_paramCheckFormatWhenOpenFail*  
44  

Questo parametro, se impostato, fa in modo che [JetInit](./jetinit-function.md) restituirà un errore speciale quando viene aperto un database o un log delle transazioni da una versione precedente del motore di database. Questi errori sono:


| <p>Errore</p> | <p>Descrizione</p> | 
|--------------|--------------------|
| <p>JET_errDatabase200Format</p> | <p>I file di database e/o di log delle transazioni sono stati creati con il motore di database Windows NT 3.51.</p> | 
| <p>JET_errDatabase400Format</p> | <p>I file di database e/o di log delle transazioni sono stati creati con il motore di database in una versione di test precedente Windows NT Server 4.0.</p> | 
| <p>JET_errDatabase500Format</p> | <p>I file di database e/o di log delle transazioni sono stati creati con il motore di database in Windows NT Server 4.0.</p> | 



**Windows Vista:**  Per Windows Vista e versioni successive, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| | | <p>Valore predefinito:</p> | <p>Vero</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramDatabasePageSize*  
64  

Questo parametro configura le dimensioni della pagina per il database. Le dimensioni della pagina sono l'unità più piccola possibile di allocazione dello spazio per un file di database. Anche le dimensioni della pagina del database sono molto importanti perché impostano il limite superiore per le dimensioni di un singolo record nel database.

**Nota** Al momento è supportata una sola dimensione di pagina del database per processo. Ciò significa che se si è in un unico processo che contiene applicazioni diverse che usano il motore di database, è necessario che tutte le applicazioni concordino sulle dimensioni della pagina del database.


| | | <p>Valore predefinito:</p> | <p>4096</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>2048, 4096, 8192</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>Sì</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramDbExtensionSize*  
18  

Questo parametro controlla la quantità di spazio che viene aggiunta a un file di database ogni volta che è necessario aumentare per contenere più dati. Le dimensioni sono in pagine di database.


| | | <p>Valore predefinito:</p> | <p>256</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p><p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramEnableIndexChecking*  
45  

Quando questo parametro è true, ogni database viene controllato al momento di [JetAttachDatabase](./jetattachdatabase-function.md) per gli indici su colonne chiave Unicode compilate usando una versione precedente della libreria NLS nel sistema operativo. Questa operazione deve essere eseguita perché il motore di database rende persistenti le chiavi di ordinamento generate da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e il valore di queste chiavi di ordinamento cambia da rilascio a rilascio.

Se viene rilevato che un indice primario si trova in questo stato, [JetAttachDatabase](./jetattachdatabase-function.md) avrà sempre esito negativo con JET_errPrimaryIndexCorrupted.

Se viene rilevato che uno degli indici secondari è in questo stato, esistono due possibili risultati. Se JET_bitDbDeleteCorruptIndexes passato a [JetAttachDatabase,](./jetattachdatabase-function.md) questi indici verranno eliminati e JET_wrnCorruptIndexDeleted restituiti da [JetAttachDatabase](./jetattachdatabase-function.md). Questi indici dovranno essere ricreati dall'applicazione. Se JET_bitDbDeleteCorruptIndexes non è stato passato [a JetAttachDatabase,](./jetattachdatabase-function.md) la chiamata avrà esito negativo con JET_errSecondaryIndexCorrupted.

**Nota** È consigliabile impostare questo parametro su True dall'applicazione.

**Nota** È consigliabile che le applicazioni evitino l'uso di colonne chiave Unicode negli indici di chiave primaria (cluster).


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Globale</p><p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramEnableIndexCleanup*  
54  

Quando questo parametro è impostato su true, il motore di database può pulire automaticamente gli indici sulle colonne chiave Unicode all'ora [JetInit](./jetinit-function.md) in base alle esigenze per evitare le modifiche al formato del database causate dalle modifiche apportate alla libreria NLS in Windows. Tali modifiche vengono apportate regolarmente alla libreria NLS per aggiungere il supporto per nuove lingue, aggiungere caratteri mancanti a una lingua, aggiungere un ordine delle regole di confronto a una lingua o correggere i bug nell'ordine delle regole di confronto di una lingua. Queste modifiche influiscono sulle chiavi di ordinamento prodotte da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) che vengono rese persistenti dal motore di database come componenti delle chiavi di indice.

È importante tenere conto che è possibile che le modifiche apportate all'indice siano così importanti che non è possibile eseguire una pulizia incrementale. In questo caso, l'indice verrà gestito come indicato da **JET_paramEnableIndexChecking**.

**Nota** È consigliabile impostare questo parametro e questo **JET_paramEnableIndexChecking** su **True dall'applicazione.**


| | | <p>Valore predefinito:</p> | <p>Vero</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p><p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows Server 2003 e versioni successive</p> | 



*JET_paramOneDatabasePerSession*  
102  

Quando questo parametro è true, solo un database può essere aperto con [JetOpenDatabase](./jetopendatabase-function.md) da una determinata sessione alla volta. Il database temporaneo è escluso da questa restrizione.

**Windows XP e Windows Server 2003:**  Questo parametro è scritto solo in Windows XP e Windows Server 2003.

**Windows Vista:**  Questo parametro si comporta normalmente a Windows Vista.

**Nota**  Questo parametro è di sola scrittura.


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p><p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramEnableOnlineDefrag*  
35  

Questo parametro controlla il comportamento della deframmentazione online quando viene avviato tramite [JetDefragment.](./jetdefragment-function.md) Per altre [informazioni, vedere JetDefragment.](./jetdefragment-function.md)

Windows 2000: in Windows 2000, questo parametro era un semplice valore booleano che consente di gate della deframmentazione online quando viene avviata da [JetDefragment.](./jetdefragment-function.md) Se impostato su **TRUE,** la deframmentazione online verrà eseguita sui record di ogni tabella nel database.

**Windows XP:**  In Windows XP e versioni successive, questo parametro può essere impostato su una o più delle opzioni seguenti:


| <p>Opzione</p> | <p>Descrizione</p> | 
|---------------|--------------------|
| <p>JET_OnlineDefragDisable</p> | <p>Non eseguire la deframmentazione online. Si tratta dell'equivalente binario dell'Windows 2000 di False per questo parametro.</p> | 
| <p>JET_OnlineDefragAllOBSOLETE</p> | <p>Eseguire la deframmentazione online completa. Si tratta dell'equivalente binario dell'Windows 2000 di True per questo parametro.</p> | 
| <p>JET_OnlineDefragDatabases</p> | <p>Eseguire la deframmentazione online dei record di ogni tabella nel database.</p> | 
| <p>JET_OnlineDefragSpaceTrees</p> | <p>Eseguire la deframmentazione online degli alberi degli spazi di ogni tabella nel database.</p> | 
| <p>JET_OnlineDefragStreamingFiles</p> | <p>Questo parametro viene usato per supportare l'infrastruttura Exchange Microsoft e non deve essere usato nell'applicazione.</p> | 
| <p>JET_OnlineDefragAll</p> | <p>Eseguire la deframmentazione online completa. Questo è l'equivalente concettuale dell'Windows 2000 di True per questo parametro.</p> | 




| | | <p>Valore predefinito:</p> | <p><strong>Windows 2000:</strong>  Vero</p><p><strong>Windows XP: per Windows XP e versioni successive:</strong> JET_OnlineDefragAll</p> | | <p>Digitare:</p> | <p><strong>Windows 2000:</strong>  Boolean</p><p><strong>Windows XP e versioni successive:</strong>  JET_GRBIT (integer)</p> | | <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong>  False, True</p><p><strong>Windows XP e versioni successive:</strong> 0 - JET_OnlineDefragAll</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramPageFragment*  
20  

Questo parametro è la soglia utilizzata dal motore di database per controllare la frammentazione dello spazio disponibile. Le dimensioni sono in pagine di database.


| | | <p>Valore predefinito:</p> | <p>8</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramRecordUpgradeDirtyLevel*  
78

Questo parametro controlla l'aggressività con cui il gestore della cache delle pagine del database scriverà una pagina di database sottoposta a una conversione del formato sul posto. Queste conversioni di formato si verificano in tempo reale quando le pagine vengono caricate da un database creato con il motore di database Windows 2000 ma usato da un Windows XP o versione successiva del motore di database.


| | | <p>Valore predefinito:</p> | <p>1</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0-3</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>Sì</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramWaypointLatency*  
153  

La latenza (nei log) dietro il log tip/highest committed per rinviare gli scaricamenti delle pagine del database. L'abilitazione di questa latenza può consentire il ripristino del database in caso di perdita irreversica del file di log più recente. Vedere JET_bitReplayIgnoreLostLogs.


| | | <p>Valore predefinito:</p> | <p>0</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0-1023</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTrees*  
160  

Attivare/disattivare la deframmentazione automatica sequenziale dell'albero B.


| | | <p>Valore predefinito:</p> | <p>1</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>0-1</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>Sì</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Determina la frequenza di controllo della densità dell'albero B.


| | | <p>Valore predefinito:</p> | <p>10</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>Numero intero massimo 0</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>Sì</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramIOThrottlingTimeQuanta*  
162  

Tempo massimo, in millisecondi, che il meccanismo di limitazione delle operazioni di I/O consente a un'attività di essere eseguita perché sia considerata "completata".


| | | <p>Valore predefinito:</p> | <p>125</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0-10000</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>No</p> | | <p>Disponibilità:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
