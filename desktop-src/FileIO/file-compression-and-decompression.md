---
description: Il file system NTFS usa Lempel-Ziv compressione, ovvero un algoritmo di compressione senza perdita di dati.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compressione e decompressione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61c19449d1bfb31dfdd6e55e8c5ffa204bda36af597c43204693c55b13254e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927801"
---
# <a name="file-compression-and-decompression"></a>Compressione e decompressione di file

I volumi FILE SYSTEM NTFS supportano la compressione dei file su singoli file. L'algoritmo di compressione file utilizzato dal file system NTFS Lempel-Ziv compressione. Si tratta  di un algoritmo di compressione senza perdita di dati, il che significa  che non vengono persi dati durante la compressione e la decompressione del file, anziché algoritmi di compressione con perdita di dati, ad esempio JPEG, in cui alcuni dati vengono persi ogni volta che si verifica la compressione e la decompressione dei dati.

La compressione dei dati riduce le dimensioni di un file riducendo al minimo i dati ridondanti. In un file di testo, i dati ridondanti possono essere caratteri che si verificano di frequente, ad esempio lo spazio o vocali comuni, ad esempio le lettere e e a; può anche verificarsi di frequente stringhe di caratteri. La compressione dei dati crea una versione compressa di un file riducendo al minimo questi dati ridondanti.

Ogni tipo di algoritmo di compressione dei dati riduce al minimo i dati ridondanti in modo univoco. Ad esempio, *l'algoritmo di codifica Huffman* assegna un codice ai caratteri in un file in base alla frequenza con cui tali caratteri si verificano. Un altro algoritmo di compressione, denominato codifica della lunghezza di *esecuzione,* genera un valore in due parti per i caratteri ripetuti: la prima parte specifica il numero di volte in cui il carattere viene ripetuto e la seconda parte identifica il carattere. Un altro algoritmo di compressione, noto come *algoritmo Lempel-Ziv,* converte le stringhe a lunghezza variabile in codici a lunghezza fissa che utilizzano meno spazio rispetto alle stringhe originali.

## <a name="the-ntfs-file-system-file-compression"></a>Compressione del file system NTFS

Nel sistema NTFS file system la compressione viene eseguita in modo trasparente. Ciò significa che può essere usato senza richiedere modifiche alle applicazioni esistenti. I byte compressi del file non sono accessibili alle applicazioni. visualizzano solo i dati non compressi. Pertanto, le applicazioni che aprono un file compresso possono operare su di esso come se non fosse compresso. Tuttavia, questi file non possono essere copiati in un altro file system.

Se si comprime un file di dimensioni superiori a 30 gigabyte, la compressione potrebbe non riuscire.

Negli argomenti seguenti viene identificata la compressione file system file NTFS:

-   [Attributo di compressione](compression-attribute.md)
-   [Stato di compressione](compression-state.md)
-   [Recupero delle dimensioni di un file compresso](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Librerie di compressione e decompressione dei file

Le librerie di compressione e decompressione dei file accettano uno o più file esistenti e producono uno o più file che sono versioni compresse degli originali. Anche la compressione è senza perdita di dati, ma la compressione non è trasparente per le applicazioni. Un'applicazione può operare solo su tali file con l'assistenza di una libreria di compressione file. Inoltre, le uniche operazioni che è possibile eseguire su tali file sono la creazione di un file compresso da un originale e il ripristino dei dati originali dalla versione decompressa. La modifica non è in genere supportata e la ricerca è limitata se supportata.

In genere, un'applicazione chiama le Lz32.dll per decomprimere i dati compressi usando Compress.exe. Le funzioni possono anche elaborare i file senza tentare di decomprimerli.

È possibile usare le funzioni in Lz32.dll decomprimere uno o più file. È anche possibile usarli per decomprimere i file compressi una parte alla volta.

Negli argomenti seguenti viene identificata la decompressione di file fornita dalle funzioni in Lz32.dll:

-   [Decompressione di un singolo file](decompressing-a-single-file.md)
-   [Decompressione di più file](decompressing-multiple-files.md)
-   [Lettura da file compressi](reading-from-compressed-files.md)

## <a name="cabinets"></a>Armadi

I file CAB vengono creati da una libreria di compressione che supporta funzionalità quali lo spanning del disco e la compressione di più file. Per altre informazioni, vedere Cabinet Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Attributo di compressione](compression-attribute.md)<br/>                                     | In un volume ntfs file system, ogni file e directory ha un attributo *di compressione*.<br/>                                         |
| [Stato di compressione](compression-state.md)<br/>                                             | Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno *stato di compressione*.<br/> |
| [Recupero delle dimensioni di un file compresso](obtaining-the-size-of-a-compressed-file.md)<br/> | Per ottenere le dimensioni compresse di un file, usare la funzione GetCompressedFileSize.<br/>                                               |
| [Decompressione di un singolo file](decompressing-a-single-file.md)<br/>                         | Un'applicazione può decomprimere un singolo file compresso usando le funzioni LZOpenFile, LZCopy e LZClose.<br/>                |
| [Decompressione di più file](decompressing-multiple-files.md)<br/>                       | Un'applicazione può decomprimere più file usando le funzioni LZOpenFile, LZCopy e LZClose.<br/>                          |
| [Lettura da file compressi](reading-from-compressed-files.md)<br/>                     | Un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni LZSeek e LZRead.<br/>                 |



 

 

