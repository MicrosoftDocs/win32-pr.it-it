---
title: Ottimizzazione delle prestazioni dei DVD per i giochi di Windows
description: Questo articolo illustra come ottimizzare le prestazioni dei DVD per i giochi di Windows.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb15063d0441423ccb3a9f67db84caa134f801c6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300047"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Ottimizzazione delle prestazioni dei DVD per i giochi di Windows

Una percentuale elevata di computer che eseguono Windows hanno un'unità DVD e molti giochi sono disponibili su DVD. Di conseguenza, è consigliabile assicurarsi che i giochi usino l'unità DVD al suo pieno vantaggio. Comprendendo il modo in cui i dati vengono letti da un DVD e il modo in cui la posizione dei dati influisca sul tempo di lettura, è possibile ridurre i tempi di caricamento e migliorare le prestazioni complessive durante la riproduzione del gioco. Questo articolo illustra come ottimizzare le prestazioni dei DVD per i giochi di Windows.

-   [Layout di base di un DVD](#basic-layout-of-a-dvd)
-   [Lettura da un DVD](#reading-from-a-dvd)
-   [Lettura degli errori](#reading-errors)
-   [Velocità effettiva dei dati](#data-throughput)
-   [Esempi di velocità effettiva sprecata](#examples-of-wasted-throughput)
-   [Lettura sincrona rispetto a asincrona](#reading-synchronously-vs-asynchronously)
-   [Lettura ottimale](#reading-optimally)
-   [Compatibilità con DVD](#dvd-compatibility)
-   [Summary](#summary)

## <a name="basic-layout-of-a-dvd"></a>Layout di base di un DVD

Questa figura illustra il layout di base di un DVD.

![layout DVD](images/dvdsector.png)

I dati in un DVD vengono archiviati come spirale continua, ad esempio in un CD; Tuttavia, i file vengono suddivisi in blocchi e settori. I file vengono distribuiti nei blocchi del codice di correzione degli errori (ECC) e ogni blocco è diviso in settori di 16 2 KB, ovvero 32 KB di dati in ogni blocco. I file sono allineati lungo i limiti del settore e qualsiasi spazio inutilizzato in un settore viene lasciato vuoto. Se un file ha solo 10 byte, il resto dello spazio in quel settore da 2 KB viene sprecato; quindi, quando possibile, aggregare i file in incrementi di 2 KB per ottenere la migliore densità di dati. Tenere presente che queste specifiche sono solo per DVD e per CD e HD-DVD sono disponibili specifiche differenti.

## <a name="reading-from-a-dvd"></a>Lettura da un DVD

Di seguito è illustrata la sequenza di esecuzione di un'unità DVD alla ricezione di una richiesta di lettura da un DVD:

1.  Modificare i livelli, se necessario
2.  Seek
3.  Riattivazione dell'unità di prelievo ottico (OPU) per la lettura dei dati
4.  Controllare la posizione effettiva
5.  Modifica e Ripeti fino a quando non vengono trovati i dati corretti

Le operazioni di lettura unità sono quantizzate in modo diverso, a seconda che si tratti di letture di unità logiche o letture di unità fisiche. Le letture di unità logiche possono leggere solo una quantità intera di settori DVD, mentre una richiesta di lettura dell'unità fisica può leggere solo una quantità intera di blocchi ECC. In genere, l'unità fisica riceve una richiesta di lettura; verrà eseguito un tentativo di riempimento della cache. Le dimensioni della cache dell'unità DVD dipendono dalle specifiche delle singole unità.

Quando un'unità DVD riceve una richiesta di lettura che supera la dimensione della cache, la richiesta viene suddivisa in richieste di dimensioni della cache. L'unità cerca il blocco ECC che contiene il primo settore della richiesta e legge l'intero blocco ECC. Il firmware dell'unità decodifica il blocco ECC e quindi legge il blocco ECC successivo. Il processo viene ripetuto fino a quando non viene riempita la cache dell'unità o tutte le richieste vengono soddisfatte. Il kernel legge quindi i dati decodificati dalla cache dell'unità. Scarica quindi la cache e avvia la successiva operazione di lettura, se vengono mantenute le richieste di lettura.

> [!Note]  
> Ogni lettura non memorizzata nella cache Scarica la cache dell'unità.

 

## <a name="reading-errors"></a>Lettura degli errori

Le unità DVD e DVD non sono perfette ed è possibile che si verifichino errori durante la lettura. Analogamente a CDs, le parti di un DVD possono diventare illeggibili da polvere o graffi. Se una parte di un blocco è illeggibile, l'intero blocco viene considerato illeggibile. Se si verifica un errore di lettura, l'unità tenta di rileggere il blocco ECC. Se il blocco è ancora illeggibile, l'unità interrompe l'operazione di lettura e restituisce un valore al kernel che indica che il blocco è stato illeggibile. Il kernel decide quindi quale passaggio eseguire successivamente. Il kernel può eseguire nuovamente la richiesta, interrompere completamente la lettura oppure ruotare l'unità e rieseguire la richiesta.

## <a name="data-throughput"></a>Velocità effettiva dei dati

La velocità effettiva dei dati di un'unità DVD dipende da più fattori: la posizione dei dati richiesti, il modo in cui il disco è pulito o graffiato, il numero di flussi letti dal disco, le dimensioni dei buffer associati a tali flussi e le specifiche della singola unità. La velocità effettiva dipende anche dal fatto che l'unità abbia una velocità angolare costante (CAV) o una velocità lineare costante (CLV). Se un'unità ruota con CAV, il disco si gira alla stessa velocità indipendentemente dalla posizione in cui si trova l'unità di prelievo ottico (OPU). Ciò significa che la traccia dei dati viene spostata oltre il OPU più velocemente perché il OPU si avvicina al bordo esterno del disco. Con CLV, il disco si sposta più lentamente mentre il OPU si sposta verso l'esterno, quindi la traccia dei dati passa oltre il OPU a una velocità costante. Le unità DVD nella maggior parte dei PC usano CLV.

Mentre l'unità Cerca e modifica i livelli, i dati non possono essere letti dal disco. È consigliabile ridurre al minimo queste operazioni, soprattutto quando si leggono i dati per una schermata di caricamento iniziale.

## <a name="examples-of-wasted-throughput"></a>Esempi di velocità effettiva sprecata

Per comprendere in che modo la velocità effettiva dei dati può essere sprecata, considerare un'unità ipotetica e un DVD. Si supponga che sia necessario leggere un file al centro del disco. La velocità effettiva dall'area del disco è circa 8,25 MB/sec. Se il tratto di ricerca è una metà o un terzo di pieno, il tempo medio di ricerca è 150 ms. In questo esempio, 1,2 MB (150 MS × 8,25 MB/sec) potrebbero essere stati letti nel momento in cui è stato richiesto solo per ottenere il OPU in cui è possibile leggere. L'aggiunta di una modifica di livello aumenta la velocità effettiva sprecata a 1,8 MB (225 ms × 8,25 MB/sec).

Un altro esempio che dimostra una velocità effettiva sprecata è il caricamento di 20 file individuati in modo non corretto da un'unità CAV senza modifiche al livello. Se il tempo di ricerca per ogni file, più la latenza prima che i dati possano essere letti, è di circa 200 ms, vengono spesi 4 secondi (20 file × 200 ms) solo cercando i dati. Se i file si trovano sul diametro esterno e si leggono a 11 ×, la velocità effettiva è media di 15,2 MB/sec (11 velocità/12 velocità × 16 MB/sec). La velocità effettiva sprecata in questo esempio è circa 60,8 MB (15,2 MB/sec × 4 sec).

## <a name="reading-synchronously-vs-asynchronously"></a>Lettura sincrona rispetto a asincrona

La lettura asincrona è più efficiente della lettura sincrona. Quando si esegue la lettura in modo sincrono, uno o più blocchi di dati ECC vengono letti nella memoria di sistema prima di essere copiati nella memoria dell'applicazione. Al contrario, la lettura asincrona copia i blocchi ECC decodificati direttamente nella memoria dell'applicazione, evitando la cache L2 e creando un minor overhead della CPU. Per leggere in modo asincrono, usare il \_ flag Overlapped del flag file \_ quando si usa la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire i file. Per eseguire l'I/O asincrono, per la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) è necessaria anche una struttura sovrapposta valida.

Per ulteriori informazioni sull'I/O asincrono [, vedere i/o sincrono e asincrono](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o).

## <a name="reading-optimally"></a>Lettura ottimale

Il principio migliore per la lettura da un DVD consiste nell'evitare la ricerca e la lettura di piccole quantità di dati. Quando la quantità di dati letti è inferiore alla capacità di un blocco ECC, ovvero inferiore a 32 KB, il resto del blocco viene sprecato. Poiché le dimensioni della cache variano da unità a unità, gli sviluppatori devono decidere una quantità minima di dati per le richieste di lettura e non ridurli. Le dimensioni minime devono essere un multiplo Integer di un blocco ECC per evitare di sprecare tempo per la lettura e la decodifica dei dati che non verranno usati. È anche importante evitare di cercare tutti i costi, perché il tempo impiegato per la ricerca è il tempo impiegato per la lettura dei dati.

## <a name="dvd-compatibility"></a>Compatibilità con DVD

Quando si rilascia un DVD, è necessario tenere presenti alcuni importanti problemi di compatibilità. Per prima cosa, le unità DVD nei computer basati su Windows possono variare in base alle prestazioni, pertanto se il DVD presenta un requisito specifico per la velocità effettiva, è importante assicurarsi che l'hardware degli utenti soddisfi tali requisiti. Inoltre, i DVD multistrato possono causare problemi di compatibilità in alcune unità DVD. Per evitare questi problemi, è consigliabile distribuire un DVD a un solo livello o testare accuratamente un DVD a più livelli nella maggior parte delle unità prima del rilascio.

## <a name="summary"></a>Riepilogo

Per migliorare le prestazioni del DVD, è possibile applicare alcune regole generali. Le tecniche seguenti consentono di ottimizzare la velocità effettiva e di ridurre i dati sprecati:

-   Evitare letture di dimensioni inferiori a 32 KB
-   Layout dei dati per ridurre o eliminare le ricerche
-   Layout dei dati nei limiti di blocco ECC
-   Massimizza la capacità aggregando i file di piccole dimensioni in blocchi da 2 KB e Riduci lo spazio di riempimento nei settori DVD
-   Lettura asincrona per ridurre il carico della CPU e un utilizzo eccessivo della memoria
-   Evitare di rilasciare DVD multistrato

 

 