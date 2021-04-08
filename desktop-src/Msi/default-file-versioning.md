---
description: I diagrammi di flusso nelle sezioni seguenti illustrano le regole predefinite di controllo delle versioni dei file usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controllo delle versioni dei file predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883005"
---
# <a name="default-file-versioning"></a>Controllo delle versioni dei file predefinito

I diagrammi di flusso nelle sezioni seguenti illustrano le regole predefinite di controllo delle versioni dei file usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione. Il controllo delle versioni dei file predefinito è illustrato anche in [sostituzione dei file esistenti](replacing-existing-files.md).

Si noti che con Windows Installer, l'hashing dei file è disponibile per ottimizzare la copia di file. Per informazioni dettagliate, vedere [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash](msifilehash-table.md). La tabella MsiFileHash può essere utilizzata solo con file senza versione.

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessun file ha una versione](neither-file-has-a-version.md)
-   [Nessun file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



