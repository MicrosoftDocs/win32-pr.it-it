---
description: La compressione dei file che contengono principalmente zeri consente un uso efficiente dello spazio su disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: File sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307932"
---
# <a name="sparse-files"></a>File sparse

Un file in cui la maggior parte dei dati è pari a zero viene detto che contiene un *set di dati di tipo sparse*. File come questi sono in genere molto grandi, ad esempio, un file che contiene i dati dell'immagine da elaborare o una matrice all'interno di un database ad alta velocità. Il problema con i file che contengono set di dati di tipo sparse è che la maggior parte del file non contiene dati utili e, per questo motivo, rappresentano un uso inefficiente dello spazio su disco.

La compressione dei file nel file system NTFS è una soluzione parziale al problema. Tutti i dati del file non scritti in modo esplicito vengono impostati in modo esplicito su zero. Compressione file compatta questi intervalli di zeri. Tuttavia, uno svantaggio della compressione dei file è che il tempo di accesso può aumentare a causa della compressione e della decompressione dei dati.

Il supporto per i file sparse è stato introdotto nel file system NTFS come un altro modo per rendere più efficiente l'utilizzo dello spazio su disco. Quando è abilitata la funzionalità file sparse, il sistema non alloca lo spazio su disco rigido a un file, tranne nelle aree in cui contiene dati diversi da zero. Quando si tenta di eseguire un'operazione di scrittura in cui una grande quantità di dati nel buffer è pari a zero, gli zeri non vengono scritti nel file. Il file system crea invece un elenco interno contenente le posizioni degli zeri nel file e questo elenco viene consultato durante tutte le operazioni di lettura. Quando viene eseguita un'operazione di lettura in aree del file in cui sono stati individuati zeri, il file system restituisce il numero appropriato di zeri nel buffer allocato per l'operazione di lettura. In questo modo, la manutenzione del file sparse è trasparente per tutti i processi che vi accedono ed è più efficiente della compressione per questo particolare scenario.

Il valore di dati predefinito di un file sparse è zero; Tuttavia, può essere impostato su altri valori.

Per ulteriori informazioni sui file sparse, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Operazioni su file sparse](sparse-file-operations.md)<br/>                           | Determinare se un file system supporta i file sparse chiamando la funzione GetVolumeInformation.<br/>                                                                                |
| [Recupero delle dimensioni di un file sparse](obtaining-the-size-of-a-sparse-file.md)<br/> | Ottenere la dimensione allocata o la dimensione totale per un file usando la funzione [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) o [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .<br/> |
| [File sparse e quote disco](sparse-files-and-disk-quota.md)<br/>                | Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata.<br/>                                                                  |



 

 

 




