---
description: I diagrammi di flusso nelle sezioni seguenti illustrano le regole di controllo delle versioni dei file predefinite usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controllo delle versioni dei file predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c239cd7989308e79dbb0ee621241560ac33a7a049c83c0a44d2cb1c3c32f5fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039991"
---
# <a name="default-file-versioning"></a>Controllo delle versioni dei file predefinito

I diagrammi di flusso nelle sezioni seguenti illustrano le regole di controllo delle versioni dei file predefinite usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione. Il controllo delle versioni dei file predefinito è illustrato anche in [Sostituzione di file esistenti.](replacing-existing-files.md)

Si noti che con Windows installer è disponibile l'hashing dei file per ottimizzare la copia dei file. Per informazioni dettagliate, [**vedere MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash.](msifilehash-table.md) La tabella MsiFileHash può essere usata solo con file senza versione.

-   [Entrambi i file hanno una versione](both-files-have-a-version.md)
-   [Nessuno dei due file ha una versione](neither-file-has-a-version.md)
-   [Nessuno dei due file ha una versione con controllo hash file](neither-file-has-a-version-with-file-hash-check.md)
-   [Un file ha una versione](one-file-has-a-version.md)

 

 



