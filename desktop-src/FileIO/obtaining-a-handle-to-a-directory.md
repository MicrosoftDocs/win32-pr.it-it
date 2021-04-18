---
description: Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Handle di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319067"
---
# <a name="directory-handles"></a>Handle di directory

Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto.

Per ottenere un handle per una directory esistente, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag del **backup della \_ \_ \_ semantica del flag di file** .

È possibile passare un handle di directory alle funzioni seguenti.



| Funzione                                                         | Descrizione                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Eseguire il backup di un file o di una directory, incluse le informazioni di sicurezza.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Cerca in futuro in un flusso di dati a cui si accede inizialmente tramite la funzione [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Ripristinare un file o una directory di cui è stato eseguito il backup con [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Recupera le informazioni sui file per il file specificato.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Recupera le dimensioni in byte del file specificato.<br/>                                                                                                   |
| [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la data e l'ora di creazione di un file o di una directory, dell'ultimo accesso e dell'Ultima modifica.<br/>                                                   |
| [**Filetype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Recupera il tipo di file del file specificato.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Recupera le informazioni che descrivono le modifiche all'interno della directory specificata.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Imposta la data e l'ora in cui è stato creato, ultimo accesso o Ultima modifica la directory o il file specificato.<br/>                                             |



 

 

