---
description: Se entrambi i file hanno un numero di versione, il programma di installazione di Windows usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Entrambi i file hanno una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380823"
---
# <a name="both-files-have-a-version"></a>Entrambi i file hanno una versione

Se il file di chiave di un componente da installare (copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (copy-B), il programma di installazione confronta il numero di versione e la lingua dei due file.

Se entrambi i file hanno un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.

Si noti che questo diagramma illustra le regole predefinite di controllo delle versioni dei [file,](file-versioning-rules.md)che possono essere sostituite impostando la [**proprietà REINSTALLMODE.**](reinstallmode.md) Il valore predefinito della **proprietà REINSTALLMODE** è "omus".

![regole predefinite di controllo delle versioni dei file quando entrambi i file hanno lo stesso nome o numero di versione](images/waiflow1.png)

Il diagramma precedente può essere usato anche con i file senza specificare alcuna lingua. Se copy-A ha una lingua specificata e copy-B non ha una lingua specificata, copy-B viene sostituito con copy-A. Se copy-A e copy-B non hanno entrambi una lingua specificata, copy-B non viene sostituito.

Vedere esempi di controllo delle versioni dei file predefinito in [Sostituzione di file esistenti.](replacing-existing-files.md)

-   [Nessuno dei due file ha una versione](neither-file-has-a-version.md)
-   [Nessuno dei due file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



