---
title: Supporto di esempio allocato dall'utente
description: Supporto di esempio allocato dall'utente
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK, supporto di esempio allocato dall'utente
- ASF (Advanced Systems Format), supporto di esempio allocato dall'utente
- ASF (Advanced Systems Format), supporto di esempio allocato dall'utente
- supporto di esempio allocato dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044473"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="aaed2-107">Supporto di esempio allocato dall'utente</span><span class="sxs-lookup"><span data-stu-id="aaed2-107">User Allocated Sample Support</span></span>

<span data-ttu-id="aaed2-108">In circostanze normali, sia l'oggetto Reader che l'oggetto Reader sincrono creano un nuovo oggetto buffer per ogni esempio recapitato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aaed2-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="aaed2-109">Questo è dovuto al fatto che l'oggetto di lettura non è in grado di conoscere il funzionamento dell'applicazione con gli esempi dopo averlo ottenuto.</span><span class="sxs-lookup"><span data-stu-id="aaed2-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="aaed2-110">Sebbene molte applicazioni leggano esempi solo per eseguirne il rendering immediatamente, è possibile che alcune applicazioni debbano gestire i campioni per un lungo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="aaed2-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="aaed2-111">L'oggetto di lettura non può, pertanto, riutilizzare i buffer allocati; li recapita all'applicazione, che quindi ne ha il controllo.</span><span class="sxs-lookup"><span data-stu-id="aaed2-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="aaed2-112">Il problema di questo approccio è che un file può contenere un numero immenso di esempi.</span><span class="sxs-lookup"><span data-stu-id="aaed2-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="aaed2-113">Se ognuno di essi richiede la creazione di un nuovo oggetto buffer, l'allocazione e il rilascio della memoria di una quantità eccessiva di tempo del processore.</span><span class="sxs-lookup"><span data-stu-id="aaed2-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="aaed2-114">In applicazioni sensibili al tempo, ad esempio lettori multimediali, questo overhead può essere molto dannoso per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="aaed2-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="aaed2-115">Per attenuare i problemi di prestazioni degli esempi allocati dal lettore, sia il Reader che il lettore sincrono supportano gli esempi allocati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aaed2-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="aaed2-116">Per usare gli esempi allocati dall'applicazione, l'oggetto di lettura effettua chiamate a un metodo di callback di allocazione di esempio che viene implementato.</span><span class="sxs-lookup"><span data-stu-id="aaed2-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="aaed2-117">La logica utilizzata dal callback per recapitare i buffer all'oggetto di lettura dipende interamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aaed2-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="aaed2-118">È possibile utilizzare un pool di buffer per l'intero file o utilizzare più pool di buffer, uno per ogni output o flusso o qualsiasi altro schema che funziona per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aaed2-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaed2-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaed2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaed2-120">**Allocazione di buffer per la lettura di file**</span><span class="sxs-lookup"><span data-stu-id="aaed2-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="aaed2-121">**Funzionalità di lettura file**</span><span class="sxs-lookup"><span data-stu-id="aaed2-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




