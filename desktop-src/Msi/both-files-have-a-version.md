---
description: Se entrambi i file hanno un numero di versione, il Windows Installer usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Entrambi i file hanno una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881073"
---
# <a name="both-files-have-a-version"></a>Entrambi i file hanno una versione

Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione e la lingua dei due file.

Se entrambi i file hanno un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.

Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) . Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

![regole di controllo delle versioni dei file predefinite quando entrambi i file hanno lo stesso nome o numero di versione](images/waiflow1.png)

Il diagramma precedente può essere usato anche con i file senza lingua specificata. Se Copy-A ha una lingua specificata e copy-B non ha un linguaggio specificato, Copy-B viene sostituito con Copy-A. Se per Copy-A e copy-B non è specificato alcun linguaggio, Copy-B non viene sostituito.

Per la [sostituzione dei file esistenti](replacing-existing-files.md), vedere esempi di controllo delle versioni dei file predefiniti.

-   [Nessun file ha una versione](neither-file-has-a-version.md)
-   [Nessun file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



