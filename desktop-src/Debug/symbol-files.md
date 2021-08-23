---
description: In genere, le informazioni di debug vengono archiviate in un file di simboli separato dal file eseguibile.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: File di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642181"
---
# <a name="symbol-files"></a>File di simboli

In genere, le informazioni di debug vengono archiviate in un file di simboli separato dal file eseguibile. L'implementazione di queste informazioni di debug è cambiata nel corso degli anni e la documentazione seguente fornirà indicazioni su queste diverse implementazioni.

## <a name="pdb-files"></a>PDB (file)

Tutte le versioni moderne dei compilatori Microsoft archiviano le informazioni di debug relative a un eseguibile compilato in un file di database di *programma* separato (con estensione pdb). Questo file viene comunemente definito *PDB.* I dati vengono archiviati in un file separato dal file eseguibile per limitare le dimensioni del file eseguibile, risparmiando spazio di archiviazione su disco e riducendo il tempo necessario per caricare i dati. Questa metodologia consente anche di distribuire il file eseguibile senza disaccontire queste informazioni significative che potrebbero rendere il programma più facile da decodificare.

Per creare un file PDB, compilare il file eseguibile con le informazioni di debug in base alle istruzioni per gli strumenti di compilazione.

L'API DbgHelp è in grado di usare PDB per ottenere le informazioni seguenti.

-   publics ed exports
-   simboli globali
-   simboli locali
-   dati di tipo
-   file di origine
-   numeri di riga

## <a name="dbg-files-and-embedded-debug-information"></a>File DBG e informazioni di debug incorporate

Le versioni precedenti del set di strumenti Microsoft usavano per incorporare le informazioni di debug nel file eseguibile, ma in genere verrebbero separate in un file separato con estensione dbg. Questo è comunemente noto come file *DBG.* I file DBG usano lo stesso formato di file PE dei file eseguibili.

Il supporto dell'API DbgHelp per i dbg e le informazioni di debug incorporate è limitato e include quanto segue.

-   publics ed exports
-   simboli globali

 

 



