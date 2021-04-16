---
description: Se nessuno dei due file ha un numero di versione, il Windows Installer usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Nessun file ha una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559928"
---
# <a name="neither-file-has-a-version"></a>Nessun file ha una versione

Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.

Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.

Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) . Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

![regole di controllo delle versioni dei file predefinite quando nessuno dei due file ha un numero di versione](images/waiflow2.png)

Vedere gli esempi di controllo delle versioni dei file predefiniti per la [sostituzione dei file esistenti](replacing-existing-files.md).

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessun file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



