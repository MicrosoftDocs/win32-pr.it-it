---
description: Il file system NTFS utilizza la compressione Lempel-Ziv, ovvero un algoritmo di compressione senza perdita di perdite.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compressione e decompressione dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317798"
---
# <a name="file-compression-and-decompression"></a>Compressione e decompressione dei file

I volumi di file system NTFS supportano la compressione dei file in base a un singolo file. L'algoritmo di compressione file utilizzato dal file system NTFS è Lempel-Ziv compressione. Si tratta di un algoritmo di compressione senza *perdita* di dati, il che significa che non viene perso alcun dato durante la compressione e la decompressione del file, in contrapposizione agli algoritmi di compressione con *perdita* di dati, ad esempio JPEG, in cui alcuni dati vengono persi ogni volta che viene eseguita la compressione e la decompressione dei dati.

La compressione dei dati riduce le dimensioni di un file riducendo al minimo i dati ridondanti. In un file di testo, i dati ridondanti possono essere caratteri che si verificano frequentemente, ad esempio il carattere spazio o le vocali comuni, ad esempio le lettere e e un oggetto; è anche possibile che si verifichino spesso stringhe di caratteri. La compressione dei dati consente di creare una versione compressa di un file riducendo al minimo questi dati ridondanti.

Ogni tipo di algoritmo di compressione dei dati consente di ridurre al minimo i dati ridondanti in modo univoco. Ad esempio, l' *algoritmo di codifica Huffman* assegna un codice ai caratteri in un file in base alla frequenza con cui si verificano tali caratteri. Un altro algoritmo di compressione, denominato *codifica di lunghezza di esecuzione*, genera un valore in due parti per i caratteri ripetuti: la prima parte specifica il numero di volte in cui il carattere viene ripetuto e la seconda parte identifica il carattere. Un altro algoritmo di compressione, noto come *algoritmo Lempel-Ziv*, converte le stringhe a lunghezza variabile in codici a lunghezza fissa che utilizzano meno spazio rispetto alle stringhe originali.

## <a name="the-ntfs-file-system-file-compression"></a>Compressione dei file system NTFS

Nella file system NTFS la compressione viene eseguita in modo trasparente. Ciò significa che può essere usato senza richiedere modifiche alle applicazioni esistenti. Byte compressi del file non accessibili alle applicazioni; vengono visualizzati solo i dati non compressi. Pertanto, le applicazioni che aprono un file compresso possono operare su di esso come se non fosse stato compresso. Tuttavia, questi file non possono essere copiati in un altro file system.

Se si comprime un file di dimensioni superiori a 30 gigabyte, la compressione potrebbe non riuscire.

Gli argomenti seguenti identificano la compressione dei file di file system NTFS:

-   [Attributo Compression](compression-attribute.md)
-   [Stato di compressione](compression-state.md)
-   [Recupero delle dimensioni di un file compresso](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Librerie di compressione e decompressione dei file

Le librerie di compressione e decompressione dei file accettano un file o file esistente e producono un file o file che sono versioni compresse degli originali. Anche la compressione è senza perdita di perdite, ma la compressione non è trasparente per le applicazioni. Un'applicazione può funzionare solo su tali file con l'assistenza di una libreria di compressione file. Inoltre, le uniche operazioni che è possibile eseguire su tali file sono la creazione di un file compresso da un originale e il recupero dei dati originali dalla versione decompressa. La modifica non è in genere supportata e la ricerca è limitata se supportata.

In genere, un'applicazione chiama funzioni in Lz32.dll per decomprimere i dati compressi con Compress.exe. Le funzioni possono anche elaborare i file senza provare a decomprimerli.

È possibile utilizzare le funzioni in Lz32.dll per decomprimere uno o più file. È anche possibile usarli per decomprimere i file compressi una parte alla volta.

Negli argomenti seguenti viene identificata la decompressione dei file fornita dalle funzioni in Lz32.dll:

-   [Decompressione di un singolo file](decompressing-a-single-file.md)
-   [Decompressione di più file](decompressing-multiple-files.md)
-   [Lettura da file compressi](reading-from-compressed-files.md)

## <a name="cabinets"></a>CAB

I cabinet vengono creati da una libreria di compressione che supporta funzionalità quali lo spanning del disco e la compressione su più file. Per ulteriori informazioni, vedere Cabinet Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Attributo Compression](compression-attribute.md)<br/>                                     | In un volume file system NTFS ogni file e directory dispone di un *attributo di compressione*.<br/>                                         |
| [Stato di compressione](compression-state.md)<br/>                                             | Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno *stato di compressione*.<br/> |
| [Recupero delle dimensioni di un file compresso](obtaining-the-size-of-a-compressed-file.md)<br/> | Per ottenere la dimensione compressa di un file, usare la funzione GetCompressedFileSize.<br/>                                               |
| [Decompressione di un singolo file](decompressing-a-single-file.md)<br/>                         | Un'applicazione può decomprimere un singolo file compresso usando le funzioni LZOpenFile, LZCopy e LZClose.<br/>                |
| [Decompressione di più file](decompressing-multiple-files.md)<br/>                       | Un'applicazione può decomprimere più file usando le funzioni LZOpenFile, LZCopy e LZClose.<br/>                          |
| [Lettura da file compressi](reading-from-compressed-files.md)<br/>                     | Un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni LZSeek e LZRead.<br/>                 |



 

 

