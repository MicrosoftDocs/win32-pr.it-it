---
description: Un puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui viene scritto il byte successivo.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Puntatori a file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226874"
---
# <a name="file-pointers"></a><span data-ttu-id="75f22-103">Puntatori a file</span><span class="sxs-lookup"><span data-stu-id="75f22-103">File Pointers</span></span>

<span data-ttu-id="75f22-104">Quando un file viene aperto, Windows associa un *puntatore di file* al flusso predefinito.</span><span class="sxs-lookup"><span data-stu-id="75f22-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="75f22-105">Questo puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui viene scritto il byte successivo.</span><span class="sxs-lookup"><span data-stu-id="75f22-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="75f22-106">Ogni volta che un file viene aperto, il sistema posiziona il puntatore del file all'inizio del file, ovvero l'offset zero.</span><span class="sxs-lookup"><span data-stu-id="75f22-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="75f22-107">Ogni operazione di lettura e scrittura sposta il puntatore del file in base al numero di byte letti e scritti.</span><span class="sxs-lookup"><span data-stu-id="75f22-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="75f22-108">Se, ad esempio, il puntatore del file si trova all'inizio del file e viene richiesta un'operazione di lettura di 5 byte, il puntatore del file sarà posizionato in corrispondenza dell'offset 5 immediatamente dopo l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="75f22-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="75f22-109">Poiché ogni byte viene letto o scritto, il sistema sposta in avanti il puntatore del file.</span><span class="sxs-lookup"><span data-stu-id="75f22-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="75f22-110">Il puntatore del file può essere riposizionato anche chiamando la funzione [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .</span><span class="sxs-lookup"><span data-stu-id="75f22-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="75f22-111">Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non viene letto alcun byte.</span><span class="sxs-lookup"><span data-stu-id="75f22-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="75f22-112">Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file.</span><span class="sxs-lookup"><span data-stu-id="75f22-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="75f22-113">La scrittura di zero byte non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="75f22-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="75f22-114">Un'applicazione può troncare o estendere un file tramite la funzione [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) .</span><span class="sxs-lookup"><span data-stu-id="75f22-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="75f22-115">Questa funzione imposta la fine del file sulla posizione corrente del puntatore del file.</span><span class="sxs-lookup"><span data-stu-id="75f22-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



