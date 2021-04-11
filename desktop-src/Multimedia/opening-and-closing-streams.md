---
title: Apertura e chiusura di flussi
description: Apertura e chiusura di flussi
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream (funzione)
- AVIStreamRelease (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044430"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="af4c1-105">Apertura e chiusura di flussi</span><span class="sxs-lookup"><span data-stu-id="af4c1-105">Opening and Closing Streams</span></span>

<span data-ttu-id="af4c1-106">L'apertura di flussi di dati è simile all'apertura di file.</span><span class="sxs-lookup"><span data-stu-id="af4c1-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="af4c1-107">È possibile aprire un flusso usando la funzione [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) .</span><span class="sxs-lookup"><span data-stu-id="af4c1-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="af4c1-108">Questa funzione crea un'interfaccia di flusso, inserisce un handle del flusso nell'interfaccia e restituisce un puntatore all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="af4c1-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="af4c1-109">**AVIFileGetStream** gestisce anche un conteggio dei riferimenti delle applicazioni che hanno aperto un flusso, ma non quelle che lo hanno chiuso.</span><span class="sxs-lookup"><span data-stu-id="af4c1-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="af4c1-110">Se si vuole accedere a un singolo flusso in un file, è possibile aprire il file e il flusso usando la funzione [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) .</span><span class="sxs-lookup"><span data-stu-id="af4c1-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="af4c1-111">Questa funzione combina le operazioni e gli argomenti della funzione delle funzioni [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileGetStream** .</span><span class="sxs-lookup"><span data-stu-id="af4c1-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="af4c1-112">Per accedere a più di un flusso in un file, usare **AVIFileOpen** una volta seguito da più chiamate a **AVIFileGetStream**.</span><span class="sxs-lookup"><span data-stu-id="af4c1-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="af4c1-113">È possibile incrementare il conteggio dei riferimenti di un flusso usando la funzione [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) per lasciare aperto un flusso quando si usa una funzione che in genere chiude il flusso.</span><span class="sxs-lookup"><span data-stu-id="af4c1-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="af4c1-114">È possibile chiudere un flusso usando la funzione [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="af4c1-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="af4c1-115">Questa funzione decrementa il conteggio dei riferimenti del flusso e lo chiude quando il conteggio dei riferimenti raggiunge zero.</span><span class="sxs-lookup"><span data-stu-id="af4c1-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="af4c1-116">Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata a **AVIStreamRelease** per ogni uso della funzione [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** o **AVIStreamOpenFromFile** .</span><span class="sxs-lookup"><span data-stu-id="af4c1-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="af4c1-117">Quando si rilascia un flusso aperto tramite **AVIStreamOpenFromFile**, avifile chiude il file contenente il flusso.</span><span class="sxs-lookup"><span data-stu-id="af4c1-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="af4c1-118">Se l'applicazione rilascia un file con flussi di dati aperti, AVIFile non chiuderà i flussi finché non verranno rilasciati tutti i flussi.</span><span class="sxs-lookup"><span data-stu-id="af4c1-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 




