---
description: 'Altre informazioni su: Parametri di database temporanei'
title: Parametri del database temporaneo
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: 427ed51c2757075ccb28fd70e5554c49dc8db4e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986824"
---
# <a name="temporary-database-parameters"></a>Parametri del database temporaneo


_**Si applica a:** Windows | Windows Server_

## <a name="temporary-database-parameters"></a>Parametri del database temporaneo

Questo argomento contiene i parametri usati per il database temporaneo.

*JET_paramEnableTempTableVersioning*  
46  

Questo parametro controlla l'uso delle transazioni nelle tabelle temporanee. Quando questo parametro è false, le tabelle temporanee saranno più veloci, ma non sarà possibile eseguire il rollback degli aggiornamenti apportati in una transazione.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Vero</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramPageTempDBMin*  
19  

Questo parametro controlla le dimensioni iniziali del database temporaneo. Le dimensioni sono in pagine di database. Una dimensione pari a zero indica che devono essere usate le dimensioni predefinite di un database comune.

È spesso consigliabile per le applicazioni di piccole dimensioni configurare il database temporaneo in modo che sia il più piccolo possibile. L'impostazione di questo parametro su 14 consente di ottenere il database temporaneo più piccolo possibile. Si noti che è anche possibile eliminare completamente il database temporaneo impostando **JET_paramMaxTemporaryTables** su zero.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>0</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramTempPath*  
1  

Questo parametro indica il percorso relativo o file system assoluto della cartella o del file che conterrà il database temporaneo per l'istanza. Se il percorso è una cartella che conterrà il database temporaneo, è necessario terminarlo con un carattere barra rovesciata. Il database temporaneo viene usato per contenere i dati volatili generati nel processo di gestione delle chiamate di informazioni sull'API ESE, creazione di indici o archiviazione del contenuto di una tabella temporanea.

**Nota:**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che usa il motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>"tmp.edb"</p> | 
| <p>Digitare:</p> | <p>Percorso (stringa)</p> | 
| <p>Intervallo valido:</p> | <p>Da 0 a 247 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
