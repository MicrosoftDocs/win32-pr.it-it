---
description: Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto .
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Handle di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc8f983748154a781e5dd2923e0c3e3351a26acb47c2230d3142d6ad6444513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015220"
---
# <a name="directory-handles"></a>Handle di directory

Ogni volta che un processo crea o apre un oggetto directory, riceve un handle per l'oggetto .

Per ottenere un handle per una directory esistente, chiamare la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **FILE FLAG BACKUP \_ \_ \_ SEMANTICS.**

È possibile passare un handle di directory alle funzioni seguenti.



| Funzione                                                         | Descrizione                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Eseguire il backup di un file o di una directory, incluse le informazioni di sicurezza.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Cerca in avanti in un flusso di dati a cui si accede inizialmente usando la [**funzione BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) [**o BackupWrite.**](/windows/desktop/api/winbase/nf-winbase-backupwrite)<br/> |
| [**BackupCrittura**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Ripristinare un file o una directory di cui è stato eseguito il backup usando [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Recupera le informazioni sul file per il file specificato.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Recupera le dimensioni del file specificato, in byte.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la data e l'ora di creazione, ultimo accesso e ultima modifica di un file o di una directory.<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Recupera il tipo di file del file specificato.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Recupera informazioni che descrivono le modifiche all'interno della directory specificata.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Imposta la data e l'ora di creazione, ultimo accesso o ultima modifica del file o della directory specificata.<br/>                                             |



 

 

