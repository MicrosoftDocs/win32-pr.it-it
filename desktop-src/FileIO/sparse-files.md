---
description: La compressione di file che contengono per lo più zeri consente un uso efficiente dello spazio su disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: File sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb89a8fd3e8c067d5328756e57d511d4c38d615f2bb19c579208462c3f5bdbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951050"
---
# <a name="sparse-files"></a>File sparse

Un file in cui gran parte dei dati è zero è detto che contiene un *set di dati di tipo sparse*. File come questi sono in genere molto grandi, ad esempio un file che contiene dati immagine da elaborare o una matrice all'interno di un database ad alta velocità. Il problema dei file che contengono set di dati di tipo sparse è che la maggior parte del file non contiene dati utili e, per questo, si tratta di un uso inefficiente dello spazio su disco.

La compressione dei file nel file system NTFS è una soluzione parziale al problema. Tutti i dati nel file non scritti in modo esplicito vengono impostati in modo esplicito su zero. La compressione file compatta questi intervalli di zeri. Tuttavia, uno svantaggio della compressione dei file è che il tempo di accesso può aumentare a causa della compressione e della decompressione dei dati.

Il supporto per i file di tipo sparse è stato introdotto nel file system NTFS come un altro modo per rendere più efficiente l'utilizzo dello spazio su disco. Quando la funzionalità dei file di tipo sparse è abilitata, il sistema non alloca spazio su disco rigido a un file, ad eccezione delle aree in cui contiene dati diversi da zero. Quando viene tentata un'operazione di scrittura in cui una grande quantità di dati nel buffer è zero, gli zeri non vengono scritti nel file. L'file system crea invece un elenco interno contenente i percorsi degli zeri nel file e questo elenco viene consultato durante tutte le operazioni di lettura. Quando viene eseguita un'operazione di lettura nelle aree del file in cui si trovavano zeri, il file system restituisce il numero appropriato di zeri nel buffer allocato per l'operazione di lettura. In questo modo, la manutenzione del file di tipo sparse è trasparente per tutti i processi che vi accedono ed è più efficiente della compressione per questo particolare scenario.

Il valore di dati predefinito di un file di tipo sparse è zero. tuttavia, può essere impostato su altri valori.

Per altre informazioni sui file di tipo sparse, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Operazioni sui file di tipo sparse](sparse-file-operations.md)<br/>                           | Determinare se file system supporta file di tipo sparse chiamando la funzione GetVolumeInformation.<br/>                                                                                |
| [Recupero delle dimensioni di un file di tipo sparse](obtaining-the-size-of-a-sparse-file.md)<br/> | Ottenere le dimensioni allocate o le dimensioni totali per un file usando la [**funzione GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) o [**GetFileSize.**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)<br/> |
| [File di tipo sparse e quote disco](sparse-files-and-disk-quota.md)<br/>                | Un file di tipo sparse influisce sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva allocata di spazio su disco.<br/>                                                                  |



 

 

 




