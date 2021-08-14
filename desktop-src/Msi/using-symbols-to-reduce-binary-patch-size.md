---
description: L'uso di simboli pubblici per i file binari dell'immagine di destinazione e di aggiornamento può ridurre di circa la metà le dimensioni delle patch binarie.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Uso dei simboli per ridurre le dimensioni binarie delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c11a1a6b058db8c9f4a7c9bde897034c3b4affa8c02d1b049d754013f4455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804083"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Uso dei simboli per ridurre le dimensioni binarie delle patch

L'uso di simboli pubblici per i file binari dell'immagine di destinazione e di aggiornamento può ridurre di circa la metà le dimensioni delle patch binarie. La riduzione effettiva dipende dai simboli usati. Si noti che l'uso dei simboli può comportare tempi di creazione delle patch più lenti perché l'elaborazione dei file di simboli richiede più tempo.

Per ridurre le dimensioni di una patch binaria usando i simboli, è necessario fornire simboli per i file binari dell'immagine di destinazione e di aggiornamento. Specificare i simboli nella colonna SymbolPaths della tabella [TargetImages](targetimages-table-patchwiz-dll-.md) e nella colonna SymbolPaths [della tabella UpgradedImages.](upgradedimages-table-patchwiz-dll-.md) È necessario usare Visual C++ per generare simboli nel formato di file del database di programma (PDB). Le versioni più Visual C++ forniscono tutte le informazioni necessarie nel file PDB. Le versioni precedenti Visual C++ generano anche il formato di file di debug (DBG). In questo caso, il valore SymbolsPaths deve specificare il percorso dei file PDB e DBG.

Ad esempio, TargetImage per una patch potrebbe essere il pacchetto di installazione fornito con Windows 2000 e che installa la versione 1.1.1029.0 di MSI.DLL. UpgradedImage potrebbe essere il pacchetto di installazione aggiornato fornito con Windows 2000 con Service Pack 1 (SP1) e che installa la versione 1.11.1314.0 di MSI.DLL. Sarà quindi necessario creare due file di proprietà di creazione patch (PCP), uno con la colonna SymbolPaths delle tabelle [TargetImages](targetimages-table-patchwiz-dll-.md) e [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) lasciato NULL (vuoto) e l'altro con la colonna SymbolPaths delle tabelle TargetImages e UpgradedImages popolata con il percorso dei simboli per i file binari. In questo caso, le dimensioni della patch generata senza usare i simboli possono essere circa tre volte le dimensioni della patch generata usando i simboli.

LMpatch.exe utilità può essere usata per testare la generazione di patch binarie per un singolo file e per verificare se i simboli sono validi. LMpatch.exe utilità è inclusa in [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). L'output Mpatch.exe indicherà se i simboli non corrispondono.

Ad esempio, immettere la riga di comando seguente per verificare se i simboli sono validi.

**mpatch.exe -NEWSYMPATH:d: \\ update -OLDSYMPATH:d: \\ target d: targetexample.dll \\ \\ d: updateexample.dll \\ \\ example.pat**

Se i simboli non sono nella posizione corretta, l'output Mpatch.exe può includere l'avviso seguente.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



