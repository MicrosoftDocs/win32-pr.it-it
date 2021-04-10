---
title: Creazione di un'applicazione di backup
description: Per eseguire l'input o l'output su un nastro, un'applicazione di backup deve prima ottenere un handle del dispositivo nastro. Nell'esempio di codice seguente viene illustrato come utilizzare la funzione CreateFile per aprire un dispositivo nastro.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- backup di applicazioni di backup
- creazione del backup di applicazioni di backup
- backup di backup, creazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047114"
---
# <a name="creating-a-backup-application"></a>Creazione di un'applicazione di backup

Per eseguire l'input o l'output su un nastro, un'applicazione di backup deve prima ottenere un handle del dispositivo nastro. Nell'esempio di codice seguente viene illustrato come utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un dispositivo nastro.


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



Per eseguire il backup di un albero di directory su un nastro, un'applicazione deve usare le funzioni [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) per attraversare l'albero di directory. Ogni volta che viene trovato un file, l'applicazione deve ottenere gli attributi del file tramite la funzione [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .

Se sono presenti collegamenti reali, un'applicazione deve determinare il numero di collegamenti e salvare l'identificatore univoco del file in una tabella per i confronti futuri. La prima volta che viene trovato un file, l'applicazione deve utilizzare [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file e la funzione [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) per avviare il backup. Quindi, può utilizzare ripetutamente la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per trasferire al nastro tutte le informazioni contenute nel buffer utilizzato da **BackupRead** . La seconda volta che un file viene trovato (verificato rispetto alla tabella degli identificatori di file quando sono presenti collegamenti reali), l'applicazione può scrivere le informazioni sul file generale sul nastro, seguite da un flusso con un identificatore che **è \_ collegamento di backup**.

Quando si ripristinano file da nastro a disco, un'applicazione deve usare le funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)e [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Per ogni file su un nastro, l'applicazione deve utilizzare **CreateFile** per creare un nuovo file su disco e **BackupWrite** per iniziare a ripristinare il file. Quindi, l'applicazione deve usare **ReadFile** ripetutamente fino a quando tutte le informazioni per il file non vengono lette dal nastro nel buffer riempito da **BackupWrite**.

Se uno dei flussi nel buffer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) dispone di un identificatore di flusso del **\_ collegamento di backup** , l'applicazione deve stabilire un collegamento reale. Se i dati necessari per stabilire il collegamento non esistono, **BackupWrite** ha esito negativo. L'applicazione può utilizzare un catalogo preesistente per individuare e ripristinare i dati originali oppure notificare all'utente che i dati del file da ripristinare si trovano in una posizione diversa.

 

 