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
# <a name="creating-a-backup-application"></a><span data-ttu-id="f18ea-107">Creazione di un'applicazione di backup</span><span class="sxs-lookup"><span data-stu-id="f18ea-107">Creating a Backup Application</span></span>

<span data-ttu-id="f18ea-108">Per eseguire l'input o l'output su un nastro, un'applicazione di backup deve prima ottenere un handle del dispositivo nastro.</span><span class="sxs-lookup"><span data-stu-id="f18ea-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="f18ea-109">Nell'esempio di codice seguente viene illustrato come utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un dispositivo nastro.</span><span class="sxs-lookup"><span data-stu-id="f18ea-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


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



<span data-ttu-id="f18ea-110">Per eseguire il backup di un albero di directory su un nastro, un'applicazione deve usare le funzioni [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) per attraversare l'albero di directory.</span><span class="sxs-lookup"><span data-stu-id="f18ea-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="f18ea-111">Ogni volta che viene trovato un file, l'applicazione deve ottenere gli attributi del file tramite la funzione [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="f18ea-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="f18ea-112">Se sono presenti collegamenti reali, un'applicazione deve determinare il numero di collegamenti e salvare l'identificatore univoco del file in una tabella per i confronti futuri.</span><span class="sxs-lookup"><span data-stu-id="f18ea-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="f18ea-113">La prima volta che viene trovato un file, l'applicazione deve utilizzare [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file e la funzione [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) per avviare il backup.</span><span class="sxs-lookup"><span data-stu-id="f18ea-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="f18ea-114">Quindi, può utilizzare ripetutamente la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per trasferire al nastro tutte le informazioni contenute nel buffer utilizzato da **BackupRead** .</span><span class="sxs-lookup"><span data-stu-id="f18ea-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="f18ea-115">La seconda volta che un file viene trovato (verificato rispetto alla tabella degli identificatori di file quando sono presenti collegamenti reali), l'applicazione può scrivere le informazioni sul file generale sul nastro, seguite da un flusso con un identificatore che **è \_ collegamento di backup**.</span><span class="sxs-lookup"><span data-stu-id="f18ea-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="f18ea-116">Quando si ripristinano file da nastro a disco, un'applicazione deve usare le funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)e [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="f18ea-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="f18ea-117">Per ogni file su un nastro, l'applicazione deve utilizzare **CreateFile** per creare un nuovo file su disco e **BackupWrite** per iniziare a ripristinare il file.</span><span class="sxs-lookup"><span data-stu-id="f18ea-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="f18ea-118">Quindi, l'applicazione deve usare **ReadFile** ripetutamente fino a quando tutte le informazioni per il file non vengono lette dal nastro nel buffer riempito da **BackupWrite**.</span><span class="sxs-lookup"><span data-stu-id="f18ea-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="f18ea-119">Se uno dei flussi nel buffer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) dispone di un identificatore di flusso del **\_ collegamento di backup** , l'applicazione deve stabilire un collegamento reale.</span><span class="sxs-lookup"><span data-stu-id="f18ea-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="f18ea-120">Se i dati necessari per stabilire il collegamento non esistono, **BackupWrite** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f18ea-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="f18ea-121">L'applicazione può utilizzare un catalogo preesistente per individuare e ripristinare i dati originali oppure notificare all'utente che i dati del file da ripristinare si trovano in una posizione diversa.</span><span class="sxs-lookup"><span data-stu-id="f18ea-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 