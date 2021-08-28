---
description: 'Altre informazioni su: Parametri di I/O'
title: Parametri di I/O
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 62cc1183f14e3de113ff5f34eaf6367bc2ff0f9a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981984"
---
# <a name="io-parameters"></a>Parametri di I/O


_**Si applica a:** Windows | Windows Server_

## <a name="io-parameters"></a>Parametri di I/O

Questo argomento contiene i parametri usati per l'input e l'output (I/O).

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP e versioni successive:**  Questo parametro consente di configurare la durata (in millisecondi) che il motore di database userà per accedere a un file bloccato prima che si verifica un errore JET_errFileAccessDenied. Questo ritardo è progettato per risolvere i problemi del software antivirus che potrebbe contenere alcuni file del motore di database aperti brevemente dopo la chiusura.

**Nota**  In seguito alla logica di ripetizione dei tentativi precedente, qualsiasi tentativo di connettersi a un database o usare un file di log già in uso dal motore di database comporta un ritardo di queste dimensioni prima che la chiamata API restituisca un errore (legittimo). Questo parametro può essere usato per disattivare tale ritardo nel caso in cui si tratta di uno scenario comune.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>10000</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 4294967295</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Quando questo parametro è impostato su true, qualsiasi cartella mancante in un percorso di file system utilizzato dal motore di database verrà creata automaticamente. In caso contrario, l'operazione che usa il percorso file system mancante avrà esito negativo con JET_errInvalidPath.


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



*JET_paramEnableFileCache*  
126  

Quando questo parametro è **True,** il motore di database userà la cache Windows file come cache di lettura per tutti i vari file. Verrà inoltre utilizzato come cache di scrittura per il database temporaneo o per i database aperti con il recupero disabilitato. Il motore di database deve disabilitare la memorizzazione nella cache di scrittura per i database normali, i file di log delle transazioni e i file di checkpoint per proteggere l'integrità transazionale dei database.

È importante notare che l'uso della cache dei file Windows aggiungerà un secondo livello di memorizzazione nella cache per i file di database. La cache del database userà comunque la propria memoria per memorizzare nella cache i file di database. Lo scopo di questa modalità è consentire all'applicazione di configurare il motore di database con una piccola cache dedicata e di consentire al Windows di donare memoria disponibile per migliorare ulteriormente la memorizzazione nella cache dei dati del database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramIOPriority*  
152  

Questo parametro controlla il modo in cui ESE gestisce le operazioni di I/O. I valori possono essere impostati su 0 (JET_IOPriorityNormal) per il normale funzionamento o su 1 (JET_IOPriorityLow) per l'operazione con priorità bassa. Quando la priorità è impostata su JET_IOPriorityLow, ESE usa la nuova funzionalità di priorità di I/O del thread disponibile in Windows Vista per ridurre la priorità di I/O nel thread in modo che le operazioni di I/O successive siano eseguite con la nuova priorità bassa.

**Windows Vista:**  JET_paramIOPriority è stato introdotto in Windows Vista.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>0</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 - 1</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Questo parametro controlla il numero di I/O di file di database che possono essere accodati contemporaneamente nel sistema operativo host.

Un valore maggiore per questo parametro può contribuire in modo significativo alle prestazioni di un'applicazione di database di grandi dimensioni.

**Windows XP e Windows Server 2003:**  Questo parametro viene ignorato in Windows XP e Windows Server 2003 e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows Vista:</strong> 1024</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000:</strong> 8 - 2147483647</p><p><strong>Windows Vista:</strong> 0 - 65536</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Numero massimo di byte che è possibile raggruppare per un'operazione di lettura coalesced.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>262144</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0-1073741824</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Numero massimo di byte che è possibile raggruppare per un'operazione di scrittura coalesced.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>393216</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0-1073741824</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Numero massimo di byte che è possibile trovare per un'operazione di I/O di scrittura coalesced.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>262144</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0-1073741824</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Numero massimo di byte che è possibile trovare per un'operazione di I/O di lettura coalesced.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>393216</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0-1073741824</p> | 
| <p>Ambito:</p> | <p>Globale</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
