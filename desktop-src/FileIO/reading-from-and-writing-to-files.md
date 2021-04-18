---
description: Un'applicazione legge e scrive in un file usando le funzioni ReadFile, ReadFileEx, WriteFile e WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lettura e scrittura nei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315931"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="b76e6-103">Lettura e scrittura nei file</span><span class="sxs-lookup"><span data-stu-id="b76e6-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="b76e6-104">Un'applicazione legge e scrive in un file usando le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .</span><span class="sxs-lookup"><span data-stu-id="b76e6-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="b76e6-105">Queste funzioni richiedono un handle per un file da aprire rispettivamente per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="b76e6-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="b76e6-106">Leggono e scrivono un numero specificato di byte nella posizione indicata dal puntatore del file.</span><span class="sxs-lookup"><span data-stu-id="b76e6-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="b76e6-107">I dati vengono letti e scritti esattamente come specificato; le funzioni non formattano i dati.</span><span class="sxs-lookup"><span data-stu-id="b76e6-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="b76e6-108">Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non viene letto alcun byte.</span><span class="sxs-lookup"><span data-stu-id="b76e6-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="b76e6-109">Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file.</span><span class="sxs-lookup"><span data-stu-id="b76e6-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="b76e6-110">La scrittura di zero byte non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="b76e6-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="b76e6-111">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b76e6-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b76e6-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b76e6-112">In this section</span></span>



| <span data-ttu-id="b76e6-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="b76e6-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="b76e6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76e6-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b76e6-115">Posizionamento di un puntatore di file</span><span class="sxs-lookup"><span data-stu-id="b76e6-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="b76e6-116">Windows utilizza un puntatore di file per tenere traccia dei byte letti o scritti.</span><span class="sxs-lookup"><span data-stu-id="b76e6-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="b76e6-117">Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="b76e6-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="b76e6-118">Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="b76e6-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="b76e6-119">Scaricamento di System-Buffered dati di I/O su disco</span><span class="sxs-lookup"><span data-stu-id="b76e6-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="b76e6-120">Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="b76e6-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="b76e6-121">Troncamento o estensione di file</span><span class="sxs-lookup"><span data-stu-id="b76e6-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="b76e6-122">Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="b76e6-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




