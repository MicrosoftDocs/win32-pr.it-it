---
description: Se nessuno dei due file ha un numero di versione, il programma di installazione di Windows usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Nessuno dei due file ha una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065936"
---
# <a name="neither-file-has-a-version"></a>Nessuno dei due file ha una versione

Se il file di chiave di un componente installato (copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.

Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, tutti i file del componente vengono sostituiti.

Si noti che questo diagramma illustra le regole [di controllo delle versioni](file-versioning-rules.md)dei file predefinite, che possono essere sostituite impostando la proprietà [**REINSTALLMODE.**](reinstallmode.md) Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

![regole di controllo delle versioni dei file predefinite quando nessuno dei due file ha un numero di versione](images/waiflow2.png)

Vedere gli esempi di controllo delle versioni predefinite dei file in [Sostituzione di file esistenti](replacing-existing-files.md).

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessuno dei due file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



