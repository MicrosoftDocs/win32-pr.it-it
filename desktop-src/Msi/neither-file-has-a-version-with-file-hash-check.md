---
description: L'hashing dei file è disponibile con Windows Installer. Per ulteriori informazioni, vedere MsiGetFileHash e la tabella MsiFileHash. La tabella MsiFileHash può essere utilizzata solo con file senza versione.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nessun file ha una versione con controllo hash file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528171"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Nessun file ha una versione con controllo hash file

L'hashing dei file è disponibile con Windows Installer. Per ulteriori informazioni, vedere [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash](msifilehash-table.md). La tabella MsiFileHash può essere utilizzata solo con file senza versione.

Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.

Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.

Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) . Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

![regole predefinite di controllo delle versioni dei file quando ne viene eseguito l'override dall'impostazione della proprietà REINSTALLMODE](images/waiflow2b.png)

Vedere gli esempi di controllo delle versioni dei file predefiniti per la [sostituzione dei file esistenti](replacing-existing-files.md).

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessun file ha una versione](neither-file-has-a-version.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



