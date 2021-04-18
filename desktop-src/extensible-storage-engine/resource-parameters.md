---
description: 'Altre informazioni su: parametri delle risorse'
title: Parametri delle risorse
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313078"
---
# <a name="resource-parameters"></a>Parametri delle risorse


_**Si applica a:** Windows | Windows Server_

## <a name="resource-parameters"></a>Parametri delle risorse

Questo argomento contiene i parametri usati per le risorse.

*JET_paramCachedClosedTables*  
125  

Questo parametro controlla il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.

I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle. Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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


*JET_paramDisablePerfmon*  
107  

Questo parametro può essere utilizzato per impedire al motore di database di pubblicare dati sulle prestazioni di Windows. Questa operazione può essere eseguita per ridurre l'attività del thread del servizio del motore di database.

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
<td><p>No</p></td>
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


*JET_paramGlobalMinVerPages*  
81  

Questo parametro consente alle applicazioni che operano in modalità a istanze diverse di pre-allocare memoria per le pagine della versione in un pool globale per emulare il comportamento precedente. Questa operazione è utile nel caso in cui l'applicazione voglia garantire che le transazioni di una determinata dimensione possano avere esito positivo in un secondo momento anche se la memoria risulterà limitata.

**Windows 2000:**  Memoria sufficiente per eseguire il backup di tutte le pagine della versione è sempre riservata in fase di [JetInit](./jetinit-function.md) .

**Windows XP:**  A partire da Windows XP, questo è ancora vero in modalità a istanza singola. Tuttavia, la memoria della pagina della versione viene allocata in modo dinamico in modalità a istanze diverse.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1 – 2147483647</p></td>
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
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCursors*  
8  

Questo parametro riserva il numero richiesto di risorse del cursore per l'utilizzo da parte di un'istanza. Una risorsa di cursore corrisponde direttamente a un tipo di dati [JET_TABLEID](./jet-tableid.md) . Questa impostazione influirà sul numero di cursori che possono essere utilizzati contemporaneamente. Una risorsa cursore non può essere condivisa da sessioni diverse, pertanto questo parametro deve essere impostato su un valore sufficientemente elevato in modo che ogni sessione possa usare tutti i cursori richiesti.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxInstances*  
104  

Questo parametro controlla il numero massimo di istanze che è possibile creare in un singolo processo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1-1024</p></td>
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
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxOpenTables*  
6  

Questo parametro riserva il numero richiesto di risorse dell'albero B + per l'utilizzo da parte di un'istanza. Questa impostazione influirà sul numero di tabelle che possono essere usate contemporaneamente. Questo parametro deve essere impostato in relazione allo schema fisico dei database utilizzati dal motore di database, pertanto questa impostazione non è semplice come potrebbe essere.

In generale, sono necessarie due risorse e una risorsa per ogni indice secondario per ogni tabella nell'uso simultaneo da parte dell'applicazione.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>300</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxSessions*  
5  

Questo parametro riserva il numero richiesto di risorse della sessione per l'utilizzo da parte di un'istanza. Una risorsa di sessione corrisponde direttamente a un tipo di dati [JET_SESID](./jet-sesid.md) . Questa impostazione influirà sul numero di sessioni che possono essere usate contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 30000</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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
<td><p>No</p></td>
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


*JET_paramMaxTemporaryTables*  
10  

Questo parametro riserva il numero richiesto di risorse della tabella temporanea per l'utilizzo da parte di un'istanza di. Questa impostazione influirà sul numero di tabelle temporanee che possono essere usate contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.

**Windows XP e versioni successive:**  Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e le attività che richiedono l'utilizzo del database temporaneo avranno esito negativo. Questa impostazione può essere utile per evitare l'i/O necessario per creare il database temporaneo se è noto che non verrà utilizzato.

**Nota**  Per l'utilizzo di una tabella temporanea è inoltre necessaria una risorsa Cursor.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>20</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
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


*JET_paramMaxVerPages*  
9  

Questo parametro riserva il numero richiesto di pagine dell'archivio versioni per l'utilizzo da parte di un'istanza. L'archivio versione include un record live di tutte le diverse versioni di ogni voce di record o di indice nel database che possono essere visualizzate da tutte le transazioni attive. Queste versioni vengono utilizzate per supportare il controllo della concorrenza multiversione utilizzato dal motore di database per supportare le transazioni mediante l'isolamento dello snapshot. Questa impostazione influirà sul numero di aggiornamenti che possono essere conservati in memoria alla volta. Ciò a sua volta influirà sul numero massimo di aggiornamenti che possono essere eseguiti da una singola transazione, sulla durata massima consentita di una transazione, sul carico simultaneo massimo per l'aggiornamento delle transazioni nel sistema o su una combinazione di questi.

Ogni pagina dell'archivio delle versioni configurata da questo parametro ha dimensioni di 16KB nei computer a 32 bit e 32 KB su computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzeranno lo spazio di indirizzi e potrebbero aumentare l'utilizzo della memoria.

**Nota**  Si tratta di una risorsa di gran lunga più comune da esaurire con il motore di database. È necessario prestare attenzione all'impostazione del parametro di sistema e al carico transazionale dell'applicazione per evitare che questa risorsa venga esaurita in base al normale funzionamento. Quando questa risorsa viene esaurita, gli aggiornamenti al database verranno rifiutati con JET_errVersionStoreOutOfMemory. Per rilasciare alcune di queste risorse, è necessario interrompere la transazione in attesa meno recente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
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


*JET_paramPageHintCacheSize*  
101  

Questo parametro controlla la dimensione di una cache speciale utilizzata per accelerare la ricerca dei puntatori di pagina figlio dell'albero B + nella cache delle pagine del database. Le dimensioni della cache sono in byte.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
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
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredMaxOpenTables*  
7  

Questo parametro tenta di evitare il numero di risorse dell'albero B + in uso al di sotto della soglia specificata.

Se questo parametro è impostato su zero, il valore predefinito sarà pari al 100% del **JET_paramMaxOpenTables**.

**Windows Vista e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database. Le applicazioni devono invece usare JET_paramMaxCachedClosedTables.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>0 (100% di <strong>JET_paramMaxOpenTables</strong>)</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
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


*JET_paramPreferredVerPages*  
63  

Questo parametro rappresenta una soglia relativa ai **JET_paramMaxVerPages** che controlla l'utilizzo discrezionale delle pagine della versione da parte del motore di database. Se la dimensione dell'archivio versioni supera questa soglia, le informazioni utilizzate solo per le attività in background facoltative, ad esempio il ripristino dello spazio eliminato nel database, vengono invece sacrificate per mantenere la stanza per le informazioni transazionali.

**Windows 2000, Windows XP e Windows Server 2003:**  Impostando questo parametro su zero, la soglia sarà pari al 90% del **JET_paramMaxVerPages**.

**Windows Vista e versioni successive:**  Questa operazione non è più supportata e il valore predefinito di questo parametro è stato modificato per chiarirne il comportamento.

Ogni pagina dell'archivio delle versioni configurata da questo parametro ha dimensioni di 16KB nei computer a 32 bit e 32 KB su computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Nota**  Se il motore di database opera al di sopra di questa soglia troppo spesso, è possibile che si verifichi un peggioramento delle prestazioni del database. Ciò accade perché i processi in background che puliscono il database non possono funzionare senza le informazioni facoltative che vengono eliminate in questo scenario. La deframmentazione in linea o non in linea condurrà questo effetto.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 (90% di JET_paramMaxVerPages)</p>
<p><strong>Windows Vista:</strong>  58</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
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


*JET_paramVerPageSize*  
128  

Questo parametro controlla la dimensione delle pagine dell'archivio versioni utilizzate dal motore di database per contenere informazioni transazionali. Il valore di questo parametro corrisponde alla dimensione dell'unità per tutti gli altri parametri di sistema in termini di pagine di versione, ad esempio JET_paramMaxVerPages.

Il motore di database può scegliere di utilizzare una dimensione di pagina di archivio versioni più grande rispetto a quella richiesta.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>16384</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p></td>
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
<td><p>No</p></td>
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


*JET_paramVersionStoreTaskQueueMax*  
105  

Questo parametro controlla il numero di elementi di lavoro di pulitura in background che possono essere accodati al pool di thread del motore di database in un momento qualsiasi.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows XP e Windows Server 2003:  </strong>  1 – 63</p>
<p><strong>Windows Vista:</strong>  1 – 127</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP e Windows Server 2003:  </strong>  No</p>
<p><strong>Windows Vista:</strong>  Sì</p></td>
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
<td><p>Windows XP e versioni successive</p></td>
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
