---
description: 'Altre informazioni su: Parametri delle risorse'
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
ms.openlocfilehash: ac1a6aba2eda729c3e705cf5acdda837c2670564
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472447"
---
# <a name="resource-parameters"></a>Parametri delle risorse


_**Si applica a:** Windows | Windows Server_

## <a name="resource-parameters"></a>Parametri delle risorse

Questo argomento contiene i parametri usati per le risorse.

*JET_paramCachedClosedTables*  
125  

Questo parametro controlla il numero di risorse albero B+ memorizzate nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.

Valori di grandi dimensioni per questo parametro causeranno l'uso di una quantità maggiore di memoria da parte del motore di database, ma aumenterà la velocità con cui un numero elevato di tabelle può essere aperto in modo casuale dall'applicazione. Ciò è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.


| | | <p>Valore predefinito:</p> | <p>64</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramDisablePerfmon*  
107  

Questo parametro può essere utilizzato per impedire al motore di database di pubblicare dati sulle relative prestazioni Windows. Questa operazione può essere eseguita per ridurre l'attività del thread del servizio del motore di database.


| | | <p>Valore predefinito:</p> | <p>Falso</p> | | <p>Digitare:</p> | <p>Boolean</p> | | <p>Intervallo valido:</p> | <p>False, True</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramGlobalMinVerPages*  
81  

Questo parametro consente alle applicazioni che operano in modalità a istanza multipla di preallocare memoria per le pagine della versione in un pool globale per emulare il comportamento precedente. Ciò è utile nel caso in cui l'applicazione voglia garantire che le transazioni di una determinata dimensione possano avere esito positivo in un secondo momento anche se la memoria diventa insufficiente.

**Windows 2000:**  Memoria sufficiente per eseguire il backup di tutte le pagine della versione è sempre riservata [all'ora JetInit.](./jetinit-function.md)

**Windows XP:**  A Windows XP, questo vale anche in modalità a istanza singola. Tuttavia, la memoria della pagina della versione viene allocata in modo dinamico in modalità a istanze multipla.


| | | <p>Valore predefinito:</p> | <p>64</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1 – 2147483647</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramMaxCursors*  
8  

Questo parametro riserva il numero richiesto di risorse del cursore per l'utilizzo da parte di un'istanza di . Una risorsa cursore corrisponde direttamente a un [tipo JET_TABLEID](./jet-tableid.md) dati. Questa impostazione influisce sul numero di cursori che è possibile usare contemporaneamente. Una risorsa cursore non può essere condivisa da sessioni diverse, pertanto questo parametro deve essere impostato su un valore sufficientemente grande in modo che ogni sessione possa utilizzare tutti i cursori necessari.

**Windows 2000, Windows XP e Windows Server 2003:**  Valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.


| | | <p>Valore predefinito:</p> | <p>1024</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramMaxInstances*  
104  

Questo parametro controlla il numero massimo di istanze che possono essere create in un singolo processo.


| | | <p>Valore predefinito:</p> | <p>16</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1-1024</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramMaxOpenTables*  
6  

Questo parametro riserva il numero richiesto di risorse albero B+ per l'uso da parte di un'istanza di . Questa impostazione influirà sul numero di tabelle che è possibile usare contemporaneamente. Questo parametro deve essere impostato in relazione allo schema fisico dei database utilizzati dal motore di database, quindi questa impostazione non è così semplice come potrebbe essere.

In generale, saranno necessarie due risorse più una risorsa per ogni indice secondario per tabella in uso simultaneo da parte dell'applicazione.

**Windows 2000, Windows XP e Windows Server 2003:**  Valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.


| | | <p>Valore predefinito:</p> | <p>300</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramMaxSessions*  
5  

Questo parametro riserva il numero richiesto di risorse di sessione per l'uso da parte di un'istanza di . Una risorsa di sessione corrisponde direttamente a un [tipo JET_SESID](./jet-sesid.md) dati. Questa impostazione influirà sul numero di sessioni che è possibile usare contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  Valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.


| | | <p>Valore predefinito:</p> | <p>16</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 30000</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramMaxTemporaryTables*  
10  

Questo parametro riserva il numero richiesto di risorse tabella temporanee per l'uso da parte di un'istanza di . Questa impostazione influisce sul numero di tabelle temporanee che possono essere usate contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

**Windows XP e versioni successive:**  Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e qualsiasi attività che richiede l'uso del database temporaneo avrà esito negativo. Questa impostazione può essere utile per evitare l'I/O necessario per creare il database temporaneo se è noto che non verrà usato.

**Nota:**  L'uso di una tabella temporanea richiede anche una risorsa cursore.


| | | <p>Valore predefinito:</p> | <p>20</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>Sì</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramMaxVerPages*  
9  

Questo parametro riserva il numero richiesto di pagine dell'archivio versioni per l'uso da parte di un'istanza di . L'archivio versioni contiene un record attivo di tutte le diverse versioni di ogni record o voce di indice nel database che può essere vista da tutte le transazioni attive. Queste versioni vengono usate per supportare il controllo della concorrenza con più versioni in uso dal motore di database per supportare le transazioni che usano l'isolamento dello snapshot. Questa impostazione influisce sul numero di aggiornamenti che possono essere mantenuti in memoria alla volta. Ciò influisce a sua volta sul numero massimo di aggiornamenti che una singola transazione può eseguire, sulla durata massima che una transazione può essere mantenuta aperta, sul carico simultaneo massimo delle transazioni di aggiornamento nel sistema o su una combinazione di questi.

Ogni pagina dell'archivio versioni configurata da questo parametro ha dimensioni di 16 KB nei computer a 32 bit e 32 KB in computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

**Nota:**  Questa è di gran lunga la risorsa più comune che deve essere esaurita dal motore di database. È necessario prestare attenzione all'impostazione del parametro di sistema e al carico transazionale dell'applicazione per evitare di esaurire questa risorsa nel normale funzionamento. Quando questa risorsa è esaurita, gli aggiornamenti al database verranno rifiutati con JET_errVersionStoreOutOfMemory. Per rilasciare alcune di queste risorse, è necessario interrompere la transazione in attesa meno recente.


| | | <p>Valore predefinito:</p> | <p>64</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramPageHintCacheSize*  
101  

Questo parametro controlla le dimensioni di una cache speciale usata per accelerare la ricerca dei puntatori di pagina figlio dell'albero B+ nella cache delle pagine del database. Le dimensioni della cache sono in byte.


| | | <p>Valore predefinito:</p> | <p>262144</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | | <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

Questo parametro tenta di mantenere il numero di risorse dell'albero B+ in uso al di sotto della soglia specificata.

Se questo parametro è impostato su zero, il valore predefinito sarà il 100% **JET_paramMaxOpenTables**.

**Windows Vista e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database. Le applicazioni devono usare JET_paramMaxCachedClosedTables invece.


| | | <p>Valore predefinito:</p> | <p>0 (100% delle <strong>JET_paramMaxOpenTables</strong>)</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramPreferredVerPages*  
63  

Questo parametro rappresenta una soglia relativa al **JET_paramMaxVerPages** che controlla l'utilizzo discrezionale delle pagine della versione da parte del motore di database. Se le dimensioni dell'archivio versioni superano questa soglia, tutte le informazioni utilizzate solo per le attività in background facoltative, ad esempio il recupero dello spazio eliminato nel database, vengono invece mantenute per mantenere spazio per le informazioni transazionali.

**Windows 2000, Windows XP e Windows Server 2003:**  Se si imposta questo parametro su zero, la soglia verrà impostata sul 90% **JET_paramMaxVerPages**.

**Windows Vista e versioni successive:**  Questa operazione non è più supportata e il valore predefinito di questo parametro è stato modificato per chiarire il comportamento.

Ogni pagina dell'archivio versioni configurata da questo parametro ha una dimensione di 16 KB nei computer a 32 bit e di 32 KB nei computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Nota**  Se il motore di database opera troppo spesso oltre questa soglia, è possibile che le prestazioni del database diminuiscano. Ciò si verifica perché i processi in background che pulisce il database non possono funzionare senza le informazioni facoltative che vengono generate in questo scenario. La deframmentazione online o offline contrasterà questo effetto.


| | | <p>Valore predefinito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 (90% delle JET_paramMaxVerPages)</p><p><strong>Windows Vista:</strong> 58</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1 – 2147483647</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramVerPageSize*  
128  

Questo parametro controlla le dimensioni delle pagine dell'archivio versioni utilizzate dal motore di database per contenere le informazioni transazionali. Il valore di questo parametro è la dimensione dell'unità per tutti gli altri parametri di sistema in termini di pagine di versione (ad esempio, JET_paramMaxVerPages).

Il motore di database può scegliere di usare dimensioni di pagina dell'archivio versioni superiori a quelle richieste.


| | | <p>Valore predefinito:</p> | <p>16384</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p> | | <p>Ambito:</p> | <p>Globale</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>No</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>No</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

Questo parametro controlla il numero di elementi di lavoro di pulizia in background che possono essere accodati al pool di thread del motore di database in qualsiasi momento.


| | | <p>Valore predefinito:</p> | <p>32</p> | | <p>Digitare:</p> | <p>Intero</p> | | <p>Intervallo valido:</p> | <p><strong>Windows XP e Windows Server 2003:</strong> 1 - 63</p><p><strong>Windows Vista:</strong> 1 - 127</p> | | <p>Ambito:</p> | <p>Istanza</p> | | <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | | <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p><strong>Windows XP e Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sì</p> | | <p>Influisce sul layout fisico:</p> | <p>No</p> | | <p>Influisce sull'affidabilità:</p> | <p>No</p> | | <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | | <p>Influisce sulle risorse:</p> | <p>Sì</p> | | <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
