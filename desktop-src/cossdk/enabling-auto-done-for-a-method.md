---
description: È possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+. Se l'attivazione JIT è disabilitata, l'operazione di completamento automatico non è disponibile.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Abilitazione dell'operazione automatica per un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305142"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="744dd-104">Abilitazione dell'operazione automatica per un metodo</span><span class="sxs-lookup"><span data-stu-id="744dd-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="744dd-105">È possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+.</span><span class="sxs-lookup"><span data-stu-id="744dd-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="744dd-106">Se l'attivazione JIT è disabilitata, l'operazione di completamento automatico non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="744dd-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="744dd-107">È necessario abilitare il completamento automatico solo per un metodo che è stato scritto intenzionalmente per sfruttarlo perché questa funzionalità può modificare il comportamento previsto del metodo.</span><span class="sxs-lookup"><span data-stu-id="744dd-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="744dd-108">Quando si Abilita l'operazione automatica, si modifica il comportamento predefinito dell'attivazione JIT e delle transazioni automatiche per il metodo.</span><span class="sxs-lookup"><span data-stu-id="744dd-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="744dd-109">Questa funzionalità può essere utile perché può rimuovere la necessità di dichiarare in modo esplicito la coerenza e la fine.</span><span class="sxs-lookup"><span data-stu-id="744dd-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="744dd-110">Questa operazione può essere eseguita semplicemente restituendo un HRESULT quando l'operazione di completamento automatico è abilitata.</span><span class="sxs-lookup"><span data-stu-id="744dd-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="744dd-111">In pratica, quando si Abilita l'operazione automatica, si indica a COM+ di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="744dd-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="744dd-112">Impostare il bit done su true per impostazione predefinita nel contesto in cui viene eseguito l'oggetto ogni volta che viene chiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="744dd-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="744dd-113">Controllare HRESULT restituito dal metodo; Se viene indicato l'ESITo positivo o negativo, impostare di conseguenza il bit di coerenza.</span><span class="sxs-lookup"><span data-stu-id="744dd-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="744dd-114">Ciò può comportare una chiamata automatica a [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), a seconda di ciò che il metodo esegue internamente.</span><span class="sxs-lookup"><span data-stu-id="744dd-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="744dd-115">**Per abilitare l'operazione automatica per un metodo**</span><span class="sxs-lookup"><span data-stu-id="744dd-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="744dd-116">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul metodo che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="744dd-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="744dd-117">Nella finestra di dialogo Proprietà metodo fare clic sulla scheda **generale** .</span><span class="sxs-lookup"><span data-stu-id="744dd-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="744dd-118">Per abilitare il completamento automatico, selezionare la casella di controllo **Disattiva automaticamente questo oggetto quando il metodo restituisce** un risultato.</span><span class="sxs-lookup"><span data-stu-id="744dd-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="744dd-119">Se la casella di controllo non è disponibile, è necessario abilitare prima l'attivazione JIT per il componente.</span><span class="sxs-lookup"><span data-stu-id="744dd-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="744dd-120">Per istruzioni dettagliate, vedere[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md) .</span><span class="sxs-lookup"><span data-stu-id="744dd-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="744dd-121">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="744dd-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="744dd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="744dd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="744dd-123">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="744dd-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="744dd-124">Abilitazione dell'attivazione JIT per un componente</span><span class="sxs-lookup"><span data-stu-id="744dd-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="744dd-125">Impostazione del bit completato</span><span class="sxs-lookup"><span data-stu-id="744dd-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



