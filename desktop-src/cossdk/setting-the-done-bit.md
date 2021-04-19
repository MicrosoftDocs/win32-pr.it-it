---
description: Impostazione del bit completato
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Impostazione del bit completato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305131"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="7d6d1-103">Impostazione del bit completato</span><span class="sxs-lookup"><span data-stu-id="7d6d1-103">Setting the Done Bit</span></span>

<span data-ttu-id="7d6d1-104">COM+ attiverà un oggetto attivato tramite JIT in base allo stato di una proprietà di contesto, ovvero il bit done, come segue:</span><span class="sxs-lookup"><span data-stu-id="7d6d1-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="7d6d1-105">Quando il bit done è impostato su true, COM+ disattiva l'oggetto quando viene restituita la chiamata al metodo corrente.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="7d6d1-106">Quando il bit done è impostato su false, l'oggetto rimane attivo quando viene restituita la chiamata al metodo corrente.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="7d6d1-107">Per impostazione predefinita, il bit done viene impostato su false quando viene creato un oggetto e il relativo contesto viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="7d6d1-108">(Qualsiasi oggetto attivato tramite JIT viene creato nel relativo contesto, in modo da impostare il proprio bit done). Tuttavia, è possibile modificare questa impostazione predefinita in base al metodo usando la proprietà auto-done.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="7d6d1-109">È possibile impostare il bit done nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d6d1-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="7d6d1-110">Uso di [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="7d6d1-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="7d6d1-111">Uso di [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="7d6d1-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="7d6d1-112">Uso della proprietà auto-done</span><span class="sxs-lookup"><span data-stu-id="7d6d1-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="7d6d1-113">Uso di IContextState</span><span class="sxs-lookup"><span data-stu-id="7d6d1-113">Using IContextState</span></span>

<span data-ttu-id="7d6d1-114">È possibile usare [**IContextState:: setDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) per impostare il bit done su true o false.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="7d6d1-115">È possibile usare [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) per ottenere lo stato corrente del bit fatto dal contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="7d6d1-116">Uso di IObjectContext</span><span class="sxs-lookup"><span data-stu-id="7d6d1-116">Using IObjectContext</span></span>

<span data-ttu-id="7d6d1-117">È possibile usare i metodi seguenti in [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) per impostare il bit fatto durante l'impostazione simultanea del bit coerente usato per il voto nelle transazioni:</span><span class="sxs-lookup"><span data-stu-id="7d6d1-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="7d6d1-118">Il [**Secomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) indica che l'operazione è stata completata e che si vota per eseguire il commit della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="7d6d1-119">Imposta sia il bit done sia il bit coerente su true.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="7d6d1-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) segnala che l'utente ha terminato la transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="7d6d1-121">Imposta il bit done su true e il bit coerente su false.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="7d6d1-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) segnala che non è stato fatto, ma che si vota per eseguire il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="7d6d1-123">Imposta il bit done su false e il bit coerente su true.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="7d6d1-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) segnala che l'operazione non è stata eseguita e che si vota di non eseguire il commit della transazione in questo momento, in genere perché lo stato è incoerente.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="7d6d1-125">Imposta sia il bit done sia il bit coerente su false.</span><span class="sxs-lookup"><span data-stu-id="7d6d1-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d6d1-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d6d1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d6d1-127">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="7d6d1-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="7d6d1-128">Abilitazione dell'attivazione JIT per un componente</span><span class="sxs-lookup"><span data-stu-id="7d6d1-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="7d6d1-129">Pool di oggetti e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="7d6d1-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="7d6d1-130">Transazioni e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="7d6d1-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



