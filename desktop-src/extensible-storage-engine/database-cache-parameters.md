---
description: 'Altre informazioni su: parametri della cache del database'
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308552"
---
# <a name="database-cache-parameters"></a>Parametri della cache del database


_**Si applica a:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Parametri della cache del database

Questo argomento contiene i parametri usati per la cache del database.

*JET_paramBatchIOBufferMax*  
22  

Questo parametro controlla la dimensione di una parte ausiliaria della cache delle pagine del database usata per simulare l'I/O della raccolta di dispersione quando non è disponibile in altro modo. Le dimensioni sono le pagine del database.

**Windows XP e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0, 2 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSize*  
41  

Questo parametro può essere utilizzato per controllare le dimensioni della cache delle pagine del database in fase di esecuzione. In genere, la cache ne ottimizza automaticamente le dimensioni come funzione dei livelli di attività del database e del computer. Se l'applicazione imposta questo parametro su zero, le dimensioni della cache vengono ottimizzate in questo modo. Tuttavia, se l'applicazione imposta questo parametro su un valore diverso da zero, la cache si adatterà a tale dimensione di destinazione (nelle pagine del database). La cache manterrà quindi le dimensioni a tale soglia fino a quando non vengono rilasciate nuove dimensioni o fino a quando non vengono rilasciate per scegliere le proprie dimensioni.

**Nota**  Le dimensioni della cache sono comunque soggette ai limiti imposti da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

Quando questo parametro viene letto, vengono restituite le dimensioni effettive della cache nelle pagine del database. Questa dimensione può essere usata dall'applicazione come input per guidare la regolazione manuale della dimensione della cache.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Speciali</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMin*  
60  

Questo parametro consente di configurare la dimensione minima della cache delle pagine del database. Le dimensioni sono le pagine del database.

Per impostazione predefinita, le dimensioni della cache del database vengono regolate automaticamente tra i limiti impostati da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Windows 2000:**  In Windows 2000, questo parametro deve essere impostato su un valore approssimativamente pari a quattro volte il numero di thread che saranno presenti all'interno dell'API ESE nello stesso momento. Questa operazione è necessaria per evitare deadlock causati da un numero insufficiente di buffer della cache delle pagine del database per eseguire operazioni complesse come le divisioni dell'albero B +.

**Windows XP e versioni successive:**  Gestione cache imposterà automaticamente le dimensioni minime della cache per evitare deadlock.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000:</strong>  64</p>
<p><strong>Windows XP:</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMax*  
23  

Questo parametro consente di configurare la dimensione massima della cache delle pagine del database. Le dimensioni sono le pagine del database.

Per impostazione predefinita, le dimensioni della cache del database vengono regolate automaticamente tra i limiti impostati da **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Nota**   Se questo parametro viene lasciato al valore predefinito, le dimensioni massime della cache verranno impostate sulle dimensioni della memoria fisica quando viene chiamato [JetInit](./jetinit-function.md) .

**Windows Vista:**  A partire da Windows Vista, il valore predefinito di questo parametro è stato modificato per chiarire questo comportamento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  512</p>
<p><strong>Windows Vista:</strong>  2 miliardi</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  No</p>
<p><strong>Windows XP:</strong>  Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP e windows 2000:</strong>  No</p>
<p><strong>Windows Vista e Windows Server 2003:</strong>  Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointDepthMax*  
24 

Questo parametro controlla il modo in cui le pagine del database vengono scaricate dalla cache delle pagine del database per ridurre al minimo il tempo necessario per il ripristino da un arresto anomalo del sistema. Il parametro è una soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema.

Se la registrazione circolare è abilitata usando [JET_paramCircularLog](./transaction-log-parameters.md) , questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.

È importante che il parametro non sia impostato su un livello troppo basso. Poiché il valore di questo parametro si avvicina a zero, la cache diventa sempre più aggressiva quando si scaricano le pagine di database su disco. In questo modo non solo si ottiene un numero maggiore di scritture nei file di database, ma anche indirettamente un numero maggiore di letture in tali file. Questo può causare problemi di prestazioni molto significativi in alcuni casi. Sfortunatamente, l'impostazione del valore ottimale più piccolo per questo parametro può essere eseguita solo usando la sperimentazione con l'applicazione di destinazione.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Tutti i valori</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Questo parametro è globale.</p>
<p><strong>Windows Vista:</strong>  Questo parametro è per istanza.</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointIOMax*  
135  

Questo parametro controlla il numero massimo di scritture simultanee che verrà utilizzato dal motore di database per scaricare le pagine di database modificate allo scopo di avanzare il checkpoint. Il valore di questo parametro può essere usato per bilanciare la velocità con cui il Checkpoint può essere avanzato rispetto all'impatto negativo che questo processo avrà sul tempo di risposta per le altre operazioni di I/O sui dischi che contengono il database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>8-1024</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows Vista e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

Quando questo parametro è **true**, il motore di database utilizzerà i dati del database direttamente dalla cache dei file di Windows invece di copiare i dati memorizzati nella cache nella propria memoria privata. Tutti i dati del database modificati verranno comunque memorizzati nella cache privata.

Lo scopo di questa modalità è ridurre ulteriormente la quantità di memoria privata utilizzata dal motore di database per memorizzare nella cache i dati del database.

La cache di visualizzazione può essere utilizzata solo se l'utilizzo della cache dei file di Windows viene abilitato impostando JET_paramEnableFileCache su **true**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows Vista e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

Questo parametro imposta l'intervallo di tempo in microsecondi rispetto al quale due accessi alle pagine del database sono considerati correlati. Questo intervallo di correlazione controlla la riservatezza dell'algoritmo di sostituzione della pagina della cache (LRU-K) agli accessi successivi alle pagine. Questo, a sua volta, avrà effetto sulle pagine che sceglie di memorizzare nella cache.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>128000</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>    0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Tutti i valori</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKHistoryMax*  
26  

Questo parametro imposta il numero massimo di pagine del database non memorizzate nella cache per cui verranno conservati i tempi di accesso alle pagine del database. Questi record della cronologia consentono all'algoritmo di sostituzione della pagina della cache (LRU-K) di rilevare più accuratamente le pagine popolari che sono state eliminate in modo errato dalla cache delle pagine del database.

**Windows XP e Windows Server 2003:**  Questo parametro viene ignorato in Windows XP e Windows Server 2003 e non influisce sul funzionamento del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000:</strong>  1024</p>
<p><strong>Windows Vista:</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  0 – 4194303</p>
<p><strong>Windows Vista:</strong>  Tutti i valori</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKPolicy*  
27  

Questo parametro configura il numero di accessi alle pagine del database considerati per determinare l'utilità della pagina. Questo parametro è essenzialmente K in LRU-K, l'algoritmo di sostituzione della pagina della cache delle pagine del database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Da 1 a 2</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTimeout*  
28

Questo parametro indica il periodo di tempo, in secondi, dopo il quale una pagina della cache delle pagine del database ha perso l'accesso a una pagina allo scopo di considerare l'utilità della pagina.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  1 – 2147483647</p>
<p><strong>Windows Vista:</strong>   1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTrxCorrInterval*  
29  

Questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

*JET_paramStartFlushThreshold*  
31  

Questo parametro controlla quando la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal **JET_paramCacheSizeMax**. Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal **JET_paramStopFlushThreshold**.

L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione. Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere. Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  5 (1%)</p>
<p><strong>Windows Vista:</strong>  20 milioni (1%)</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Tutti i valori</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramStopFlushThreshold*  
32  

Questo parametro controlla quando la cache delle pagine del database termina la rimozione di pagine dalla cache per creare spazio per le pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal **JET_paramCacheSizeMax**. Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da **JET_paramStartFlushThreshold**.

La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache della pagina del database per le pagine modificate (Windows 2000) o per tutte le pagine (Windows XP e versioni successive).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  10 (2%)</p>
<p><strong>Windows Vista:</strong>  40 milioni (2%)</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Tutti i valori</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
