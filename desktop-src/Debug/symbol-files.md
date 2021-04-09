---
description: In genere, le informazioni di debug vengono archiviate in un file di simboli separato dall'eseguibile.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: File di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126054"
---
# <a name="symbol-files"></a>File di simboli

In genere, le informazioni di debug vengono archiviate in un file di simboli separato dall'eseguibile. L'implementazione di queste informazioni di debug è cambiata negli anni e la documentazione seguente fornirà indicazioni su queste diverse implementazioni.

## <a name="pdb-files"></a>PDB (file)

Tutte le versioni moderne dei compilatori Microsoft archiviano le informazioni di debug su un eseguibile compilato in un file di *database di programma* (con estensione pdb) separato. Questo file viene comunemente definito *PDB*. I dati vengono archiviati in un file separato dall'eseguibile per limitare le dimensioni del file eseguibile, salvando lo spazio di archiviazione su disco e riducendo il tempo necessario per caricare i dati. Questa metodologia consente inoltre la distribuzione del file eseguibile senza divulgare queste informazioni significative che potrebbero rendere il programma più semplice da decodificare.

Per creare un PDB, compilare il file eseguibile con le informazioni di debug in base alle istruzioni per gli strumenti di compilazione.

L'API DbgHelp è in grado di usare pdb per ottenere le informazioni seguenti.

-   pubbliche ed esportazioni
-   simboli globali
-   simboli locali
-   dati di tipo
-   file di origine
-   numeri di riga

## <a name="dbg-files-and-embedded-debug-information"></a>File DBG e informazioni di debug incorporate

Le versioni precedenti del set di strumenti Microsoft usavano per incorporare le informazioni di debug nel file eseguibile, tuttavia verrebbero normalmente rimosse in un file separato con estensione dbg. Questo è comunemente noto come file *dbg* . I file DBG utilizzano lo stesso formato di file PE degli eseguibili.

Il supporto dell'API DbgHelp per DBGs e informazioni di debug incorporate è limitato e include quanto segue.

-   pubbliche ed esportazioni
-   simboli globali

 

 



