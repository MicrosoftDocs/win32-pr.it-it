---
title: Ottimizzazione delle prestazioni dei DVD per Windows giochi
description: Questo articolo illustra come ottimizzare le prestazioni dei DVD per Windows giochi.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe08ba6188df9b8bbc25a73595bf1509b257696955c1fcbd1ae98091b3c8aecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042537"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Ottimizzazione delle prestazioni dei DVD per Windows giochi

Una percentuale elevata di computer che eseguono Windows dispone di un'unità DVD e molti giochi vengono forniti su DVD. Di conseguenza, è consigliabile assicurarsi che i giochi usino l'unità DVD a tutti i vantaggi. Comprendendo il modo in cui i dati vengono letti da un DVD e come la posizione dei dati influisce sul tempo di lettura, è possibile ridurre i tempi di caricamento e migliorare le prestazioni complessive durante il gioco. Questo articolo illustra come ottimizzare le prestazioni dei DVD per Windows giochi.

-   [Layout di base di un DVD](#basic-layout-of-a-dvd)
-   [Lettura da un DVD](#reading-from-a-dvd)
-   [Errori di lettura](#reading-errors)
-   [Velocità effettiva dei dati](#data-throughput)
-   [Esempi di velocità effettiva sprecata](#examples-of-wasted-throughput)
-   [Lettura sincrona e asincrona](#reading-synchronously-vs-asynchronously)
-   [Lettura ottimale](#reading-optimally)
-   [Compatibilità DVD](#dvd-compatibility)
-   [Summary](#summary)

## <a name="basic-layout-of-a-dvd"></a>Layout di base di un DVD

Questa figura mostra il layout di base di un DVD.

![layout dvd](images/dvdsector.png)

I dati in un DVD vengono archiviati come continuo, ad esempio in un CD. Tuttavia, i file sono suddivisi in blocchi e settori. I file vengono distribuiti in blocchi ECC (Error Correction Code) e ogni blocco è suddiviso in sedici settori da 2 KB, ovvero 32 KB di dati in ogni blocco. I file vengono allineati lungo i limiti di settore e qualsiasi spazio inutilizzato in un settore viene lasciato vuoto. Se un file ha solo 10 byte, il resto dello spazio in tale settore da 2 KB viene sprecato; Pertanto, quando possibile, aggregare i file in incrementi di 2 KB per ottenere la migliore densità dei dati. Tenere presente che queste specifiche sono solo per DVD e cd e HD-DVD hanno specifiche diverse.

## <a name="reading-from-a-dvd"></a>Lettura da un DVD

Ecco la sequenza eseguita da un'unità DVD alla ricezione di una richiesta di lettura da un DVD:

1.  Modificare i livelli, se necessario
2.  Seek
3.  Ricentrare l'unità di raccolta ottico (OPU) per leggere i dati
4.  Controllare la posizione effettiva
5.  Regolare e ripetere fino a quando non vengono trovati i dati corretti

Le operazioni di lettura delle unità vengono quantificate in modo diverso, a seconda che si tratta di letture di unità logiche o letture di unità fisiche. Le operazioni di lettura di unità logiche possono leggere solo una quantità intera di settori DVD, mentre una richiesta di lettura unità fisica può leggere solo una quantità intera di blocchi ECC. In genere, l'unità fisica riceve una richiesta di lettura. tenterà di riempire la cache. La dimensione della cache dell'unità DVD dipende dalle specifiche della singola unità.

Quando un'unità DVD riceve una richiesta di lettura che supera le dimensioni della cache, la richiesta viene suddivisa in richieste di dimensioni della cache. L'unità cerca il blocco ECC che contiene il primo settore della richiesta e legge l'intero blocco ECC. Il firmware dell'unità decodifica il blocco ECC e quindi legge il blocco ECC successivo. Il processo viene ripetuto fino a quando la cache dell'unità non viene riempita o tutte le richieste vengono soddisfatte. Il kernel legge quindi i dati decodificati dalla cache dell'unità. Scarica quindi la cache e avvia l'operazione di lettura successiva, se rimangono richieste di lettura.

> [!Note]  
> Ogni lettura non memorizzata nella cache scarica la cache dell'unità.

 

## <a name="reading-errors"></a>Errori di lettura

I DVD e le unità DVD non sono ideali e possono verificarsi errori durante la lettura. Analogamente ai CD, parti di un DVD possono diventare illeggibili dalla descrizione o dai grafchi. Se una parte di un blocco è illeggibile, l'intero blocco viene considerato illeggibile. Se si verifica un errore di lettura, l'unità prova a leggere nuovamente il blocco ECC. Se il blocco è ancora illeggibile, l'unità interrompe l'operazione di lettura e restituisce un valore al kernel che indica che il blocco è illeggibile. Il kernel decide quindi quale passaggio eseguire successivamente. Il kernel può riemettere la richiesta, interrompere completamente la lettura o ruotare l'unità e riemettere la richiesta.

## <a name="data-throughput"></a>Velocità effettiva dei dati

La velocità effettiva dei dati di un'unità DVD dipende da più fattori: la posizione dei dati richiesti, la pulizia o l'scratch del disco, il numero di flussi letti dal disco, le dimensioni dei buffer associati a tali flussi e le specifiche della singola unità. La velocità effettiva dipende anche dal fatto che l'unità abbia una velocità angolare costante (CAV) o una velocità lineare costante (CLV). Se un'unità ruota con CAV, il disco ruota alla stessa velocità indipendentemente dalla posizione dell'unità ottico di raccolta (OPU). Ciò significa che la traccia dei dati si sposta oltre l'OPU più velocemente man appena l'OPU si avvicina al bordo esterno del disco. Con la CLV, il disco ruota più lentamente mentre l'OPU si sposta verso l'esterno, in modo che la traccia dei dati passi oltre l'OPU a una velocità costante. Le unità DVD nella maggior parte dei PC usano CLV.

Mentre l'unità cerca e modifica i livelli, i dati non possono essere letti dal disco. È consigliabile ridurre al minimo queste operazioni, soprattutto durante la lettura dei dati per una schermata di caricamento iniziale.

## <a name="examples-of-wasted-throughput"></a>Esempi di velocità effettiva sprecata

Per comprendere come può essere sprecata la velocità effettiva dei dati, prendere in considerazione un'unità e un DVD ipotetici. Si supponga che sia necessario leggere un file al centro del disco. La velocità effettiva da tale area del disco è di circa 8,25 MB/sec. Se il tratto di ricerca è a metà o un terzo del tratto pieno, il tempo medio di ricerca è 150 ms. In questo esempio, 1,2 MB (150 ms × 8,25 MB/sec) potrebbero essere stati letti nel tempo impiegato solo per ottenere l'OPU in dove può leggere. L'aggiunta di una modifica del livello aumenta la velocità effettiva sprecata a 1,8 MB (225 ms × 8,25 MB/sec).

Un altro esempio che dimostra una velocità effettiva sprecata è il caricamento di 20 file con posizione non ottimale da un'unità CAV senza modifiche al livello. Se il tempo di ricerca per ogni file, più la latenza prima che i dati possano essere letti, è di circa 200 ms, vengono utilizzati 4 secondi (20 file × 200 ms) solo per la ricerca dei dati. Se i file si trovano sul diametro esterno e vengono letti a 11× velocità, la velocità effettiva media è di 15,2 MB/sec (11 velocità/12 velocità × 16 MB/sec). La velocità effettiva sprecata in questo esempio è di circa 60,8 MB (15,2 MB/sec × 4 sec).

## <a name="reading-synchronously-vs-asynchronously"></a>Lettura sincrona e asincrona

La lettura asincrona è più efficiente della lettura sincrona. Durante la lettura sincrona, uno o più blocchi di dati ECC vengono letti nella memoria di sistema prima di essere copiati nella memoria dell'applicazione. Al contrario, la lettura asincrona copia i blocchi ECC decodificati direttamente nella memoria dell'applicazione, evitando così la cache L2 e generando un minore sovraccarico della CPU. Per leggere in modo asincrono, usare il flag FILE \_ FLAG \_ OVERLAPPED quando si usa la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire i file. La [**funzione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) richiede anche una struttura OVERLAPPED valida passata per eseguire operazioni di I/O asincrone.

Altre informazioni sull'I/O asincrono sono disponibili in [I/O sincrono e asincrono.](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o)

## <a name="reading-optimally"></a>Lettura ottimale

Il principio migliore nella lettura da un DVD è evitare di cercare e leggere piccole quantità di dati. Quando la quantità di dati letti è inferiore alla capacità di un blocco ECC , inferiore a 32 KB, il resto del blocco viene sprecato. Poiché le dimensioni della cache variano da unità a unità, gli sviluppatori devono decidere una quantità minima di dati per le richieste di lettura e non renderle inferiori. La dimensione minima deve essere un numero intero multiplo di un blocco ECC per evitare di perdere tempo nella lettura e decodifica dei dati che non verranno usati. È anche importante evitare di cercare a tutti i costi, perché qualsiasi tempo impiegato per la ricerca è il tempo impiegato per non leggere i dati.

## <a name="dvd-compatibility"></a>Compatibilità DVD

Esistono alcuni importanti problemi di compatibilità da tenere presenti durante il rilascio su DVD. In primo luogo, le unità DVD nei computer basati su Windows possono variare in termini di prestazioni, quindi se il DVD ha un requisito specifico per la velocità effettiva, è importante assicurarsi che l'hardware degli utenti soddisfi tali requisiti. Inoltre, i DVD a piùlayer possono causare problemi di compatibilità in alcune unità DVD. Per evitare questi problemi, è consigliabile distribuire un DVD a livello singolo o testare accuratamente un DVD a più livelli nella maggior parte delle unità prima del rilascio.

## <a name="summary"></a>Riepilogo

Per migliorare le prestazioni dei DVD, è possibile applicare alcune regole generali. Le tecniche seguenti consentono di ottimizzare la velocità effettiva e ridurre i dati sprecati:

-   Evitare operazioni di lettura inferiori a 32 KB
-   Eseguire il lay out dei dati per ridurre o eliminare le ricerca
-   Creare il timeout dei dati nei limiti dei blocchi ECC
-   Ottimizzare la capacità mediante l'aggregazione di file di piccole dimensioni in blocchi da 2 KB e ridurre lo spazio di riempimento nei settori DVD
-   Leggere in modo asincrono per ridurre il carico della CPU e l'utilizzo eccessivo della memoria
-   Evitare di rilasciare DVD a piùlayer

 

 