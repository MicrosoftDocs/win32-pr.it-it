---
description: 'Altre informazioni su: Parametri della cache del database'
title: Parametri della cache del database
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 43d51be7e2db82d64c70f6fa810be3caf4c6fbd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984094"
---
# <a name="database-cache-parameters"></a>Parametri della cache del database


_**Si applica a:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Parametri della cache del database

Questo argomento contiene i parametri usati per la cache del database.

*JET_paramBatchIOBufferMax*  
22  

Questo parametro controlla le dimensioni di una parte ausiliaria della cache delle pagine del database usata per simulare l'I/O di raccolta a dispersione quando non è altrimenti disponibile. Le dimensioni sono in pagine di database.

**Windows XP e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>256</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0, 2 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCacheSize*  
41  

Questo parametro può essere usato per controllare le dimensioni della cache delle pagine del database in fase di esecuzione. In genere, la cache ottimizza automaticamente le dimensioni in funzione dei livelli di attività del database e del computer. Se l'applicazione imposta questo parametro su zero, la cache ottimizza le proprie dimensioni in questo modo. Tuttavia, se l'applicazione imposta questo parametro su un valore diverso da zero, la cache verrà adattata alle dimensioni di destinazione (nelle pagine di database). La cache conterà quindi le dimensioni a tale soglia fino a quando non vengono specificate nuove dimensioni o fino a quando non viene rilasciata per scegliere le proprie dimensioni.

**Nota:**  Le dimensioni della cache sono ancora soggette ai limiti imposti da JET_paramCacheSizeMin **e** **JET_paramCacheSizeMax**.

Quando questo parametro viene letto, vengono restituite le dimensioni effettive della cache nelle pagine di database. Queste dimensioni possono essere usate dall'applicazione come input per guidare la regolazione manuale delle dimensioni della cache.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Speciali</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 1 - 1048575</p><p><strong>Windows XP:</strong> 1 - 4294967295</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCacheSizeMin*  
60  

Questo parametro configura le dimensioni minime della cache delle pagine del database. Le dimensioni sono in pagine di database.

Per impostazione predefinita, la cache del database regola automaticamente le dimensioni tra i limiti impostati JET_paramCacheSizeMin **e** **JET_paramCacheSizeMax**.

**Windows 2000:**  In Windows 2000, questo parametro deve essere impostato su un valore approssimativamente uguale a quattro volte il numero di thread che si trovaranno contemporaneamente all'interno dell'API ESE. Questa operazione è necessaria per evitare deadlock causati da un numero insufficiente di buffer della cache delle pagine del database per eseguire operazioni complesse come le divisioni dell'albero B+.

**Windows XP e versioni successive:**  Gestione cache imposta automaticamente le proprie dimensioni minime della cache per evitare deadlock.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows XP:</strong> 1</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 1 - 1048575</p><p><strong>Windows XP:</strong> 1 - 4294967295</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCacheSizeMax*  
23  

Questo parametro configura le dimensioni massime della cache delle pagine del database. Le dimensioni sono in pagine di database.

Per impostazione predefinita, la cache del database regola automaticamente le dimensioni tra i limiti impostati JET_paramCacheSizeMin **e** **JET_paramCacheSizeMax**.

**Nota:**   Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulla dimensione della memoria fisica quando viene chiamato [JetInit.](./jetinit-function.md)

**Windows Vista:**  A Windows Vista, il valore predefinito di questo parametro è stato modificato per chiarire questo comportamento.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 512</p><p><strong>Windows Vista:</strong> 2000000000</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 1 - 1048575</p><p><strong>Windows XP:</strong> 1 - 4294967295</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  No</p><p><strong>Windows XP:</strong>  Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows XP e Windows 2000:</strong>  No</p><p><strong>Windows Vista e Windows Server 2003:</strong>  Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCheckpointDepthMax*  
24 

Questo parametro controlla l'aggressività con cui le pagine di database vengono scaricate dalla cache delle pagine del database per ridurre al minimo il tempo necessario per il ripristino da un arresto anomalo del sistema. Il parametro è una soglia in byte per il numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo.

Se la registrazione circolare è [abilitata JET_paramCircularLog,](./transaction-log-parameters.md) questo parametro controlla anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.

È importante che questo parametro non sia impostato troppo basso. Quando il valore di questo parametro si avvicina a zero, la cache diventerà sempre più aggressiva quando si scaricano le pagine del database su disco. Ciò non solo comporta un numero maggiore di scritture nei file di database, ma provoca anche indirettamente un numero maggiore di operazioni di lettura in tali file. Ciò può causare problemi di prestazioni molto significativi in alcuni casi. Sfortunatamente, l'impostazione del valore ottimale più piccolo per questo parametro può essere eseguita solo usando la sperimentazione con l'applicazione di destinazione.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>20971520</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Tutti i valori</p> | 
| <p>Ambito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Questo parametro è globale.</p><p><strong>Windows Vista:</strong>  Questo parametro è per ogni istanza.</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCheckpointIOMax*  
135  

Questo parametro controlla il numero massimo di scritture simultanee che il motore di database userà per scaricare le pagine di database modificate allo scopo di far avanzare il checkpoint. Il valore di questo parametro può essere usato per bilanciare la velocità con cui il checkpoint può essere avanzato rispetto all'impatto negativo che questo processo avrà sul tempo di risposta per altre operazioni di I/O ai dischi che contiene il database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>96</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>8 – 1024</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramEnableViewCache*  
127  

Quando questo parametro è **True,** il motore di database userà i dati del database direttamente dalla cache dei file Windows anziché copiare i dati memorizzati nella cache nella propria memoria privata. Tutti i dati del database modificati verranno comunque memorizzati nella cache nella memoria privata.

Questa modalità consente di ridurre ulteriormente la quantità di memoria privata usata dal motore di database per memorizzare nella cache i dati del database.

La cache di visualizzazione può essere usata solo se l'uso della cache Windows file è abilitato impostando JET_paramEnableFileCache su **True**.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramLRUKCorrInterval*  
25  

Questo parametro imposta l'intervallo di tempo in microsecondi rispetto al quale vengono considerati correlati due accessi alle pagine del database. Questo intervallo di correlazione controlla la riservatezza dell'algoritmo di sostituzione delle pagine della cache (LRU-K) agli accessi successivi alla pagina. Ciò influirà a sua volta sulle pagine che sceglie di mantenere memorizzate nella cache.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>128000</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Tutti i valori</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLRUKHistoryMax*  
26  

Questo parametro imposta il numero massimo di pagine di database non memorizzate nella cache per le quali verranno mantenuti i tempi di accesso alle pagine del database. Questi record di cronologia consentono all'algoritmo di sostituzione delle pagine della cache (LRU-K) di rilevare in modo più accurato le pagine più popolari che sono state evase in modo errato dalla cache delle pagine del database.

**Windows XP e Windows Server 2003:**  Questo parametro viene ignorato in Windows XP e Windows Server 2003 e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000:</strong> 1024</p><p><strong>Windows Vista:</strong> 100000</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 0 - 4194303</p><p><strong>Windows Vista:</strong>  Tutti i valori</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLRUKPolicy*  
27  

Questo parametro configura il numero di accessi alle pagine del database considerati per determinare l'utilità della pagina. Questo parametro è essenzialmente K in LRU-K, l'algoritmo di sostituzione delle pagine della cache delle pagine del database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>2</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>Da 1 a 2</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLRUKTimeout*  
28

Questo parametro indica il periodo di tempo in secondi dopo il quale una pagina nella cache delle pagine del database viene considerata persa da un accesso alla pagina allo scopo di considerare l'utilità della pagina.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>100</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 1 - 2147483647</p><p><strong>Windows Vista:</strong> 1 - 4294967295</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLRUKTrxCorrInterval*  
29  

Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

*JET_paramStartFlushThreshold*  
31  

Questo parametro controlla quando la cache delle pagine del database inizia a eliminare le pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, verrà avviato un processo in background per riempire il pool di buffer disponibili. Questa soglia è sempre relativa alla dimensione massima della cache impostata **da** JET_paramCacheSizeMax . Questa soglia deve essere sempre inferiore alla soglia di arresto impostata da JET_paramStopFlushThreshold **.**

L'altezza della distanza della soglia iniziale determinerà il tempo di risposta che la cache delle pagine del database deve avere per produrre buffer disponibili prima che l'applicazione ne abbia bisogno. Una soglia di avvio elevata offrirà al processo in background più tempo per reagire. Tuttavia, una soglia di avvio elevata implica una soglia di arresto più elevata che ridurrà le dimensioni effettive della cache delle pagine del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 5 (1%)</p><p><strong>Windows Vista:</strong> 20000000 (1%)</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 1 - 1048575</p><p><strong>Windows XP:</strong> 1 - 4294967295</p><p><strong>Windows Vista:</strong>  Tutti i valori</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramStopFlushThreshold*  
32  

Questo parametro controlla quando la cache delle pagine del database termina di eliminare le pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background avviato per riempire il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alla dimensione massima della cache impostata **da** JET_paramCacheSizeMax . Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata **da** JET_paramStartFlushThreshold .

La distanza tra la soglia di inizio e la soglia di arresto influisce sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore rende più probabile che le scritture nelle pagine adiacenti possano essere combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 10 (2%)</p><p><strong>Windows Vista:</strong> 40000000 (2%)</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 1 - 1048575</p><p><strong>Windows XP:</strong> 1 - 4294967295</p><p><strong>Windows Vista:</strong>  Tutti i valori</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
