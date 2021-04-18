---
description: L'uso di simboli pubblici per i file binari di destinazione e di aggiornamento delle immagini può ridurre le dimensioni di una dimensione di circa una metà.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Uso di simboli per ridurre le dimensioni delle patch binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307836"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Uso di simboli per ridurre le dimensioni delle patch binarie

L'uso di simboli pubblici per i file binari di destinazione e di aggiornamento delle immagini può ridurre le dimensioni di una dimensione di circa una metà. La riduzione effettiva dipende dai simboli utilizzati. Si noti che l'uso di simboli può comportare tempi di creazione di patch più lenti perché richiede più tempo per elaborare i file di simboli.

Per ridurre le dimensioni di una patch binaria usando i simboli, è necessario specificare i simboli per i file binari di destinazione e di aggiornamento dell'immagine. Specificare i simboli nella colonna SymbolPaths della tabella [TargetImages](targetimages-table-patchwiz-dll-.md) e nella colonna SymbolPaths della tabella [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) . È necessario utilizzare Visual C++ per generare simboli nel formato di file del database di programma (PDB). Le versioni più recenti di Visual C++ forniscono tutte le informazioni necessarie nel file PDB. Le versioni precedenti di Visual C++ generano anche il formato di file di debug (DBG). In questo caso, il valore SymbolsPaths deve specificare il percorso dei file PDB e DBG.

Ad esempio, il TargetImage per una patch potrebbe essere il pacchetto di installazione fornito con Windows 2000 e che installa la versione 1.1.1029.0 di MSI.DLL. UpgradedImage potrebbe essere il pacchetto di installazione aggiornato fornito con Windows 2000 con Service Pack 1 (SP1) e che installa la versione 1.11.1314.0 di MSI.DLL. Sarà quindi necessario creare due file di proprietà di creazione patch (PCP), uno con la colonna SymbolPaths delle tabelle [TargetImages](targetimages-table-patchwiz-dll-.md) e [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) a sinistra (vuoto) e l'altro con la colonna SymbolPaths delle tabelle TargetImages e UpgradedImages popolate con la posizione dei simboli per i file binari. In questo caso, la dimensione della patch generata senza usare i simboli può essere approssimativamente tre volte la dimensione della patch generata usando i simboli.

L'utilità Mpatch.exe può essere utilizzata per testare la generazione di patch binarie per un singolo file e per verificare se i simboli sono validi o meno. L'utilità Mpatch.exe è inclusa nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). L'output di Mpatch.exe indicherà se i simboli non corrispondono.

Ad esempio, immettere la riga di comando seguente per verificare se i simboli sono validi o meno.

**mpatch.exe-NEWSYMPATH: d: \\ Update-OLDSYMPATH: d: \\ target d: \\ target \\example.dll d: \\ Update \\example.dll example. Pat**

Se i simboli non sono nella posizione corretta, l'output di Mpatch.exe può includere il seguente avviso.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



