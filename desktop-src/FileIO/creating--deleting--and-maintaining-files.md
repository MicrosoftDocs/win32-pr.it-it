---
description: Funzioni da usare per creare, eliminare e gestire file.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Creazione, eliminazione e gestione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982121"
---
# <a name="creating-deleting-and-maintaining-files"></a>Creazione, eliminazione e gestione di file

Negli argomenti seguenti viene descritto come creare, eliminare e gestire file.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Denominazione di file, percorsi e spazi dei nomi](naming-a-file.md)<br/>     | Regole, convenzioni e limitazioni dei nomi per file e directory, tra cui convenzioni di denominazione, nomi di file brevi e nomi di file lunghi, percorsi completi e percorsi relativi, limitazione della lunghezza massima del percorso, nomi di file 8.3 e spazi dei nomi.<br/>            |
| [Creazione e apertura di file](creating-and-opening-files.md)<br/> | Considerazioni per la creazione o l'apertura di un file tramite la [**funzione CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)<br/>                                                                                                                                                            |
| [Spostamento e sostituzione di file](moving-and-replacing-files.md)<br/> | Considerazioni per lo spostamento e la sostituzione di file tramite le funzioni CopyFileEx, CreateFile, Replacefile e MoveFileEx.<br/>                                                                                                                                        |
| [Chiusura ed eliminazione di file](closing-and-deleting-files.md)<br/> | Per usare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari usando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Se un file viene aperto al termine di un'applicazione, il sistema lo chiude automaticamente.<br/> |
| [Deframmentazione di file](defragmenting-files.md)<br/>               | *La deframmentazione* è il processo di spostamento di parti di file su un disco per deframmentare i file, cio' il processo di spostamento dei cluster di file su un disco per renderli contigui.<br/>                                                                               |



 

 

