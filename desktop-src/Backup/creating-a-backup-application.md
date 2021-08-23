---
title: Creazione di un'applicazione di backup
description: Per eseguire l'input o l'output su un nastro, un'applicazione di backup deve prima ottenere un handle del dispositivo nastro. L'esempio di codice seguente illustra come usare la funzione CreateFile per aprire un dispositivo nastro.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Backup di applicazioni di backup
- creazione di applicazioni di backup Backup
- backup backup, creazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086e51bce928b682d3e61518de29118abdc48461a77f79e48a4a4cb4b0f2c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529481"
---
# <a name="creating-a-backup-application"></a>Creazione di un'applicazione di backup

Per eseguire l'input o l'output su un nastro, un'applicazione di backup deve prima ottenere un handle del dispositivo nastro. L'esempio di codice seguente illustra come usare la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un dispositivo nastro.


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



Per eseguire il backup di un albero di directory in un nastro, un'applicazione deve usare le [**funzioni FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) per attraversare l'albero di directory. Ogni volta che viene trovato un file, l'applicazione deve ottenere gli attributi del file usando la [**funzione GetFileAttributes.**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa)

Se sono presenti collegamenti rigidi, un'applicazione deve determinare il numero di collegamenti e salvare l'identificatore univoco del file in una tabella per confronti futuri. La prima volta che viene trovato un file, l'applicazione deve usare [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file e la [**funzione BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) per avviare il backup. Può quindi usare ripetutamente la [**funzione WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per trasferire tutte le informazioni nel buffer usato da **BackupRead** sul nastro. La seconda volta che viene trovato un file (controllato rispetto alla tabella degli identificatori di file quando sono presenti collegamenti rigidi), l'applicazione può scrivere le informazioni generali sul file sul nastro, seguito da un flusso con un identificatore che è **BACKUP \_ LINK**.

Quando si ripristinano file da nastro a disco, un'applicazione deve usare le [**funzioni CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)e [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Per ogni file su nastro, l'applicazione deve usare **CreateFile** per creare un nuovo file su disco e **BackupWrite** per iniziare a ripristinare il file. L'applicazione deve quindi usare **ReadFile** ripetutamente fino a quando tutte le informazioni per il file non vengono lette dal nastro nel buffer riempito da **BackupWrite**.

Se uno dei flussi nel buffer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) ha un identificatore di flusso **BACKUP \_ LINK,** l'applicazione deve stabilire un collegamento rigido. Se i dati necessari per stabilire il collegamento non esistono, **BackupWrite non** riesce. L'applicazione può usare un catalogo preesiste per individuare e ripristinare i dati originali oppure può inviare una notifica all'utente che i dati del file da ripristinare si trova in un percorso diverso.

 

 