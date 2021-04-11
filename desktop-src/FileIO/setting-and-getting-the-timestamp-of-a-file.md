---
description: Le applicazioni possono recuperare e impostare la data e l'ora di creazione, dell'Ultima modifica o dell'ultimo accesso di un file tramite le funzioni GetFileTime ha provocato e SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Impostazione e recupero del timestamp di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226262"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="4730e-103">Impostazione e recupero del timestamp di un file</span><span class="sxs-lookup"><span data-stu-id="4730e-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="4730e-104">Le applicazioni possono recuperare e impostare la data e l'ora di creazione, dell'Ultima modifica o dell'ultimo accesso di un file tramite le funzioni [**GetFileTime ha provocato**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="4730e-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="4730e-105">Per ulteriori informazioni, vedere [file Times](/windows/desktop/SysInfo/file-times).</span><span class="sxs-lookup"><span data-stu-id="4730e-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="4730e-106">Non tutti i file System possono registrare i tempi di creazione e di ultimo accesso e non tutti i file System li registrano nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="4730e-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="4730e-107">Ad esempio, in file system FAT, l'ora di creazione ha una risoluzione di 10 millisecondi, l'ora di scrittura ha una risoluzione di 2 secondi e l'ora di accesso ha una risoluzione di 1 giorno (in realtà, la data di accesso).</span><span class="sxs-lookup"><span data-stu-id="4730e-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="4730e-108">Il file system NTFS ritarda l'aggiornamento all'ora dell'ultimo accesso per un file fino a un'ora dopo l'ultimo accesso.</span><span class="sxs-lookup"><span data-stu-id="4730e-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
