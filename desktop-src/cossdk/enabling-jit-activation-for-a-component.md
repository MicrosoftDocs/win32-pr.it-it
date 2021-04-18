---
description: Abilitazione dell'attivazione JIT per un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Abilitazione dell'attivazione JIT per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304951"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="8ea1b-103">Abilitazione dell'attivazione JIT per un componente</span><span class="sxs-lookup"><span data-stu-id="8ea1b-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="8ea1b-104">È necessario configurare un componente per l'attivazione JIT solo quando viene scritto correttamente per supportare il servizio di attivazione JIT (just-in-Time) COM+.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="8ea1b-105">Se un componente viene disattivato tra le chiamate al metodo, perderà qualsiasi stato associato.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="8ea1b-106">Dato il comportamento predefinito dell'attivazione JIT, questo errore si verifica quando non è previsto, ma è necessario conoscere i requisiti di un componente prima di modificarne la configurazione e le aspettative dei client che chiameranno il componente.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="8ea1b-107">Se un componente è configurato per richiedere transazioni, il servizio di attivazione JIT COM+ viene abilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="8ea1b-108">In questo caso, non è possibile disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-108">You cannot disable it in this case.</span></span> <span data-ttu-id="8ea1b-109">Per informazioni dettagliate, vedere [configurazione di transazioni](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8ea1b-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="8ea1b-110">Quando si Abilita l'attivazione JIT per un componente, il relativo attributo di sincronizzazione viene impostato su Required per quel componente.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="8ea1b-111">In questo caso, non è possibile modificare l'impostazione di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="8ea1b-112">Per informazioni dettagliate, vedere [dipendenze di sincronizzazione](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="8ea1b-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="8ea1b-113">**Per abilitare l'attivazione JIT**</span><span class="sxs-lookup"><span data-stu-id="8ea1b-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="8ea1b-114">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="8ea1b-115">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="8ea1b-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="8ea1b-116">Per abilitare l'attivazione JIT per il componente, selezionare la casella di controllo **Abilita attivazione Just-in-Time** .</span><span class="sxs-lookup"><span data-stu-id="8ea1b-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="8ea1b-117">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-117">Click **OK**.</span></span>

<span data-ttu-id="8ea1b-118">Quando è stata abilitata l'attivazione JIT per un componente, è possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da tale componente.</span><span class="sxs-lookup"><span data-stu-id="8ea1b-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="8ea1b-119">Per ulteriori informazioni, vedere [Abilitazione dell'operazione automatica per un metodo](enabling-auto-done-for-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea1b-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ea1b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ea1b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea1b-121">Abilitazione dell'operazione automatica per un metodo</span><span class="sxs-lookup"><span data-stu-id="8ea1b-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="8ea1b-122">Impostazione del bit completato</span><span class="sxs-lookup"><span data-stu-id="8ea1b-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



