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
ms.openlocfilehash: 87c8c93e70950aca360e4aa9bad62b8280611c6713156dec80e4d11414f346d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978601"
---
# <a name="resource-parameters"></a>Parametri delle risorse


_**Si applica a:** Windows | Windows Server_

## <a name="resource-parameters"></a>Parametri delle risorse

Questo argomento contiene i parametri usati per le risorse.

*JET_paramCachedClosedTables*  
125  

Questo parametro controlla il numero di risorse albero B+ memorizzate nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.

Valori di grandi dimensioni per questo parametro causeranno l'uso di una quantità maggiore di memoria da parte del motore di database, ma aumenterà la velocità con cui un numero elevato di tabelle può essere aperto in modo casuale dall'applicazione. Ciò è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.

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
<td><p>Intero</p></td>
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
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro può essere utilizzato per impedire al motore di database di pubblicare dati sulle relative prestazioni Windows. Questa operazione può essere eseguita per ridurre l'attività del thread del servizio del motore di database.

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
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro consente alle applicazioni che operano in modalità a istanza multipla di preallocare memoria per le pagine della versione in un pool globale per emulare il comportamento precedente. Ciò è utile nel caso in cui l'applicazione voglia garantire che le transazioni di una determinata dimensione possano avere esito positivo in un secondo momento anche se la memoria diventa insufficiente.

**Windows 2000:**  Memoria sufficiente per eseguire il backup di tutte le pagine della versione è sempre riservata [all'ora JetInit.](./jetinit-function.md)

**Windows XP:**  A Windows XP, questo vale anche in modalità a istanza singola. Tuttavia, la memoria della pagina della versione viene allocata in modo dinamico in modalità a istanze multipla.

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
<td><p>Intero</p></td>
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
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro riserva il numero richiesto di risorse del cursore per l'utilizzo da parte di un'istanza di . Una risorsa cursore corrisponde direttamente a un [tipo JET_TABLEID](./jet-tableid.md) dati. Questa impostazione influisce sul numero di cursori che è possibile usare contemporaneamente. Una risorsa cursore non può essere condivisa da sessioni diverse, pertanto questo parametro deve essere impostato su un valore sufficientemente grande in modo che ogni sessione possa utilizzare tutti i cursori necessari.

**Windows 2000, Windows XP e Windows Server 2003:**  Valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro controlla il numero massimo di istanze che possono essere create in un singolo processo.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro riserva il numero richiesto di risorse dell'albero B+ per l'uso da parte di un'istanza di . Questa impostazione influisce sul numero di tabelle che possono essere usate contemporaneamente. Questo parametro deve essere impostato in relazione allo schema fisico dei database in uso dal motore di database, quindi questa impostazione non è così semplice come potrebbe essere.

In generale, sono necessarie due risorse più una risorsa per ogni indice secondario per tabella in uso simultaneo da parte dell'applicazione.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro riserva il numero richiesto di risorse di sessione per l'uso da parte di un'istanza di . Una risorsa di sessione corrisponde direttamente a un [tipo JET_SESID](./jet-sesid.md) dati. Questa impostazione influisce sul numero di sessioni che è possibile usare contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro riserva il numero richiesto di risorse tabella temporanee per l'uso da parte di un'istanza di . Questa impostazione influisce sul numero di tabelle temporanee che possono essere usate contemporaneamente.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

**Windows XP e versioni successive:**  Se questo parametro di sistema è impostato su zero, non verrà creato alcun database temporaneo e qualsiasi attività che richiede l'uso del database temporaneo avrà esito negativo. Questa impostazione può essere utile per evitare l'I/O necessario per creare il database temporaneo se è noto che non verrà usato.

**Nota**  L'uso di una tabella temporanea richiede anche una risorsa cursore.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro riserva il numero richiesto di pagine dell'archivio versioni per l'uso da parte di un'istanza di . L'archivio versioni contiene un record attivo di tutte le diverse versioni di ogni record o voce di indice nel database che può essere visualizzato da tutte le transazioni attive. Queste versioni vengono usate per supportare il controllo della concorrenza con più versioni in uso dal motore di database per supportare le transazioni che usano l'isolamento dello snapshot. Questa impostazione influisce sul numero di aggiornamenti che possono essere mantenuti in memoria alla volta. Ciò influisce a sua volta sul numero massimo di aggiornamenti che una singola transazione può eseguire, sulla durata massima che una transazione può essere mantenuta aperta, sul carico simultaneo massimo delle transazioni di aggiornamento nel sistema o su una combinazione di questi.

Ogni pagina dell'archivio versioni configurata da questo parametro ha dimensioni di 16 KB nei computer a 32 bit e 32 KB in computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Windows 2000, Windows XP e Windows Server 2003:**  I valori di grandi dimensioni per questo parametro utilizzano lo spazio degli indirizzi e possono aumentare l'utilizzo della memoria.

**Nota**  Questa è di gran lunga la risorsa più comune che deve essere esaurita dal motore di database. È necessario prestare attenzione all'impostazione del parametro di sistema e al carico transazionale dell'applicazione per evitare di esaurire questa risorsa nel normale funzionamento. Quando questa risorsa è esaurita, gli aggiornamenti al database verranno rifiutati con JET_errVersionStoreOutOfMemory. Per rilasciare alcune di queste risorse, è necessario interrompere la transazione in attesa meno recente.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro controlla le dimensioni di una cache speciale usata per accelerare la ricerca dei puntatori di pagina figlio dell'albero B+ nella cache delle pagine del database. Le dimensioni della cache sono in byte.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro tenta di mantenere il numero di risorse dell'albero B+ in uso al di sotto della soglia specificata.

Se questo parametro è impostato su zero, il valore predefinito sarà il 100% **JET_paramMaxOpenTables**.

**Windows Vista e versioni successive:**  Questo parametro è obsoleto e non influisce sul funzionamento del motore di database. Le applicazioni devono usare JET_paramMaxCachedClosedTables.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>0 (100% delle <strong>JET_paramMaxOpenTables</strong>)</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro rappresenta una soglia relativa alla JET_paramMaxVerPages **che** controlla l'uso discrezionale delle pagine di versione da parte del motore di database. Se le dimensioni dell'archivio versioni superano questa soglia, tutte le informazioni usate solo per le attività in background facoltative, ad esempio il recupero dello spazio eliminato nel database, vengono invece sacrificate per mantenere spazio per le informazioni transazionali.

**Windows 2000, Windows XP e Windows Server 2003:**  L'impostazione di questo parametro su zero imposta la soglia sul 90% **JET_paramMaxVerPages**.

**Windows Vista e versioni successive:**  Questa operazione non è più supportata e il valore predefinito di questo parametro è stato modificato per chiarire il comportamento.

Ogni pagina dell'archivio versioni configurata da questo parametro ha dimensioni di 16 KB nei computer a 32 bit e 32 KB in computer a 64 bit.

**Windows Vista e versioni successive:**  Le dimensioni della pagina dell'archivio versioni possono essere lette e modificate tramite JET_paramVerPageSize.

**Nota**  Se il motore di database opera troppo spesso oltre questa soglia, è possibile che le prestazioni del database diminuiscano. Ciò si verifica perché i processi in background che pulisce il database non possono funzionare senza le informazioni facoltative che vengono generate in questo scenario. La deframmentazione online o offline contrasterà questo effetto.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 (90% delle JET_paramMaxVerPages)</p>
<p><strong>Windows Vista:</strong> 58</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro controlla le dimensioni delle pagine dell'archivio versioni usate dal motore di database per contenere informazioni transazionali. Il valore di questo parametro è la dimensione dell'unità per tutti gli altri parametri di sistema in termini di pagine di versione (ad esempio JET_paramMaxVerPages).

Il motore di database può scegliere di usare dimensioni di pagina dell'archivio versioni maggiori di quelle richieste.

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
<td><p>Intero</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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

Questo parametro controlla il numero di elementi di lavoro di pulizia in background che possono essere accodati al pool di thread del motore di database in qualsiasi momento.

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
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows XP e Windows Server 2003:</strong> 1 - 63</p>
<p><strong>Windows Vista:</strong> 1 - 127</p></td>
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
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP e Windows Server 2003:</strong>  No</p>
<p><strong>Windows Vista:</strong>  Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
