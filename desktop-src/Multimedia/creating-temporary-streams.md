---
title: Creazione di flussi temporanei
description: Creazione di flussi temporanei
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate (funzione)
- AVIStreamRelease (funzione)
- AVIMakeCompressedStream (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471195"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="e163f-106">Creazione di flussi temporanei</span><span class="sxs-lookup"><span data-stu-id="e163f-106">Creating Temporary Streams</span></span>

<span data-ttu-id="e163f-107">I flussi temporanei possono essere utili in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="e163f-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="e163f-108">È possibile usare un flusso temporaneo come flusso di lavoro, ad esempio quando si modifica il formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="e163f-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="e163f-109">In alternativa, è possibile creare un flusso temporaneo per contenere parti di altri flussi che sono stati copiati.</span><span class="sxs-lookup"><span data-stu-id="e163f-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="e163f-110">È possibile creare un flusso in memoria non associato ad alcun file tramite la funzione [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) .</span><span class="sxs-lookup"><span data-stu-id="e163f-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="e163f-111">Questa funzione restituisce l'indirizzo dell'interfaccia al nuovo flusso in una posizione specificata e viene usato internamente da altre funzioni che creano flussi temporanei.</span><span class="sxs-lookup"><span data-stu-id="e163f-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="e163f-112">È possibile creare un flusso compresso da un flusso non compresso usando la funzione [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) .</span><span class="sxs-lookup"><span data-stu-id="e163f-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="e163f-113">Si identifica il flusso da comprimere, il metodo di compressione e le opzioni di compressione e il gestore per il nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="e163f-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="e163f-114">Al termine dell'uso di un flusso creato con **AVIStreamCreate** o **AVIMakeCompressedStream**, chiudere il flusso usando la funzione [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="e163f-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="e163f-115">**AVIStreamRelease** libera le risorse usate dal flusso temporaneo.</span><span class="sxs-lookup"><span data-stu-id="e163f-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




