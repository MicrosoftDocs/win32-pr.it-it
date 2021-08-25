---
description: L'hashing dei file è disponibile con Windows Installer. Per altre informazioni, vedere MsiGetFileHash e la tabella MsiFileHash. La tabella MsiFileHash può essere usata solo con file senza versione.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nessuno dei due file ha una versione con controllo hash file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869197"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Nessuno dei due file ha una versione con controllo hash file

L'hashing dei file è disponibile con Windows Installer. Per altre informazioni, vedere [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash](msifilehash-table.md). La tabella MsiFileHash può essere usata solo con file senza versione.

Se il file di chiave di un componente installato (copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.

Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente. Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, tutti i file del componente vengono sostituiti.

Si noti che questo diagramma illustra le regole [di controllo delle versioni](file-versioning-rules.md)dei file predefinite, che possono essere sostituite impostando la proprietà [**REINSTALLMODE.**](reinstallmode.md) Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

![regole di controllo delle versioni dei file predefinite quando ne viene eseguito l'override tramite l'impostazione della proprietà reinstallmode](images/waiflow2b.png)

Vedere gli esempi di controllo delle versioni predefinite dei file in [Sostituzione di file esistenti](replacing-existing-files.md).

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessuno dei due file ha una versione](neither-file-has-a-version.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



