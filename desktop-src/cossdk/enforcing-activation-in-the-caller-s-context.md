---
description: Applicazione dell'attivazione nel contesto dei chiamanti
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Applicazione dell'attivazione nel contesto dei chiamanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304618"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="db274-103">Applicazione dell'attivazione nel contesto del chiamante</span><span class="sxs-lookup"><span data-stu-id="db274-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="db274-104">È possibile controllare se un oggetto viene attivato in un contesto.</span><span class="sxs-lookup"><span data-stu-id="db274-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="db274-105">Quando si utilizza lo strumento di amministrazione Servizi componenti per richiedere l'attivazione del componente nel contesto del chiamante, si verifica quanto segue quando COM+ attiva un'istanza del componente in un contesto:</span><span class="sxs-lookup"><span data-stu-id="db274-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="db274-106">Se possibile, l'oggetto viene attivato nel contesto del creatore.</span><span class="sxs-lookup"><span data-stu-id="db274-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="db274-107">L'attivazione dell'oggetto ha esito negativo se richiede il proprio contesto; \_ \_ \_ Viene restituito il tentativo di \_ creare il \_ \_ contesto client esterno \_ .</span><span class="sxs-lookup"><span data-stu-id="db274-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="db274-108">Il fatto che l'oggetto richieda il proprio contesto dipende dalla configurazione relativa allo stato corrente delle proprietà di contesto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="db274-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="db274-109">Per informazioni dettagliate, vedere [contesti com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="db274-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="db274-110">È possibile controllare l'attivazione a tale livello se un aspetto dell'oggetto non funziona correttamente se dispone di un contesto.</span><span class="sxs-lookup"><span data-stu-id="db274-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="db274-111">Se, ad esempio, il componente non supporta il marshalling e ha il proprio contesto, le chiamate a tale componente avranno esito negativo perché le chiamate tra i contesti vengono intercettate e viene eseguito un marshalling leggero.</span><span class="sxs-lookup"><span data-stu-id="db274-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="db274-112">**Per applicare l'attivazione nel contesto del chiamante**</span><span class="sxs-lookup"><span data-stu-id="db274-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="db274-113">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova nella cartella **componenti** di qualsiasi applicazione COM+ selezionata) per la quale si stanno impostando le proprietà di attivazione e quindi fare clic su **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="db274-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="db274-114">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="db274-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="db274-115">Selezionare la casella **di controllo deve essere attivato nel contesto dei chiamanti** .</span><span class="sxs-lookup"><span data-stu-id="db274-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="db274-116">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="db274-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db274-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db274-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db274-118">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="db274-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="db274-119">Applicazione dell'attivazione nel contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="db274-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



