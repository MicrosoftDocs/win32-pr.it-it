---
description: Funzioni da utilizzare per creare, eliminare e gestire i file.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Creazione, eliminazione e gestione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317803"
---
# <a name="creating-deleting-and-maintaining-files"></a>Creazione, eliminazione e gestione di file

Negli argomenti seguenti viene descritto come creare, eliminare e gestire i file.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)<br/>     | Regole, convenzioni e limitazioni dei nomi per i file e le directory, incluse le convenzioni di denominazione, i nomi di file brevi e i nomi di file lunghi, i percorsi completi e i percorsi relativi, il limite massimo per la lunghezza del percorso, i nomi file 8,3 e gli spazi dei nomi.<br/>            |
| [Creazione e apertura di file](creating-and-opening-files.md)<br/> | Considerazioni per la creazione o l'apertura di un file tramite la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .<br/>                                                                                                                                                            |
| [Trasferimento e sostituzione di file](moving-and-replacing-files.md)<br/> | Considerazioni per lo spostamento e la sostituzione dei file tramite le funzioni CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.<br/>                                                                                                                                        |
| [Chiusura ed eliminazione di file](closing-and-deleting-files.md)<br/> | Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.<br/> |
| [Deframmentazione di file](defragmenting-files.md)<br/>               | La *deframmentazione* è il processo di trasferimento di parti di file in un disco per deframmentare i file, ovvero il processo di trasferimento dei cluster di file su un disco per renderli contigui.<br/>                                                                               |



 

 

