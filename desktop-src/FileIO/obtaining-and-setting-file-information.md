---
description: Funzioni da utilizzare per ottenere e impostare le informazioni sul file.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Recupero e impostazione delle informazioni sui file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885557"
---
# <a name="obtaining-and-setting-file-information"></a>Recupero e impostazione delle informazioni sui file

Negli argomenti seguenti viene descritto come ottenere e impostare le informazioni sul file.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recupero delle informazioni sul tipo di file](retrieving-file-type-information.md)<br/>                               | La funzione [**FileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) Recupera il tipo di file: disco, carattere (ad esempio una console), pipe o Unknown.<br/>                                                                                                                                               |
| [Determinazione delle dimensioni di un file](determining-the-size-of-a-file.md)<br/>                                   | La funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera le dimensioni di un file.<br/>                                                                                                                                                                                                      |
| [Ricerca di uno o più file](searching-for-one-or-more-files.md)<br/>                                 | Un'applicazione può eseguire ricerche nella directory corrente per tutti i nomi di file che corrispondono a un modello specificato usando le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .<br/> |
| [Impostazione e recupero del timestamp di un file](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | Le applicazioni possono recuperare e impostare la data e l'ora di creazione, dell'Ultima modifica o dell'ultimo accesso di un file tramite le funzioni [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .<br/>                                                                         |
| [Determinazione della tabella codici del set di caratteri corrente](determining-the-current-character-set-code-page.md)<br/> | La funzione [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se le funzioni di i/O dei file utilizzano la tabella codici del set di caratteri ANSI o OEM.<br/>                                                                                                                               |



 

 

