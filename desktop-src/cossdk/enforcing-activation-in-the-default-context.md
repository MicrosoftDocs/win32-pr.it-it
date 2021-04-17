---
description: Un componente COM configurato viene in genere attivato nel relativo contesto; COM+ fa riferimento alle informazioni del catalogo dei componenti per fornire i servizi configurati.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Applicazione dell'attivazione nel contesto predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524362"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="f4286-103">Applicazione dell'attivazione nel contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="f4286-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="f4286-104">Un componente COM configurato viene in genere attivato nel relativo contesto; COM+ fa riferimento alle informazioni del catalogo del componente per fornire i servizi configurati.</span><span class="sxs-lookup"><span data-stu-id="f4286-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="f4286-105">Tuttavia, è possibile scegliere di attivare un componente configurato nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4286-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="f4286-106">Un componente COM di base, ovvero un componente registrato senza informazioni sul catalogo COM+, viene in genere attivato nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4286-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="f4286-107">L'attivazione di un componente COM nel contesto predefinito offre tre vantaggi principali in termini di prestazioni, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f4286-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="f4286-108">È possibile salvare le risorse di sistema limitando il numero di contesti creati.</span><span class="sxs-lookup"><span data-stu-id="f4286-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="f4286-109">Si aumentano le prestazioni limitando il numero di chiamate tra più contesti.</span><span class="sxs-lookup"><span data-stu-id="f4286-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="f4286-110">Poiché le chiamate tra contesti richiedono il marshalling, è molto più veloce per un oggetto COM attivato nel contesto predefinito per effettuare chiamate ad altri oggetti nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4286-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="f4286-111">Le prestazioni in questo caso (di chiamate all'interno dello stesso contesto) sono simili a quelle della chiamata a una subroutine.</span><span class="sxs-lookup"><span data-stu-id="f4286-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="f4286-112">È possibile importare le applicazioni COM meno recenti in COM+ ed eseguirle senza problemi.</span><span class="sxs-lookup"><span data-stu-id="f4286-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="f4286-113">È possibile, ad esempio, che si disponga di più applicazioni COM meno recenti implementate in base al presupposto che sia possibile passare riferimenti a oggetti all'interno di un Apartment senza effettuare il marshalling dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="f4286-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="f4286-114">Queste applicazioni COM non funzionano quando vengono importate in COM+ perché i riferimenti agli oggetti vengono passati tra i limiti del contesto.</span><span class="sxs-lookup"><span data-stu-id="f4286-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="f4286-115">Tuttavia, è possibile eseguire questo tipo di applicazione COM quando viene importato se si utilizza lo strumento di amministrazione Servizi componenti per contrassegnare tutte le classi nell'applicazione come **deve essere attivato nel contesto predefinito**.</span><span class="sxs-lookup"><span data-stu-id="f4286-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="f4286-116">Lo svantaggio principale dell'attivazione di un componente configurato nel contesto predefinito è che COM+ non fornisce alcun servizio configurato per il componente.</span><span class="sxs-lookup"><span data-stu-id="f4286-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="f4286-117">Si verifica un compromesso tra prestazioni migliorate e la possibilità di utilizzare i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="f4286-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="f4286-118">Si supponga, ad esempio, che un componente COM non richieda alcun servizio COM+, ad esempio [transazioni](com--transactions.md), [attivazione JIT](com--just-in-time-activation.md), [eventi](com--events.md), componenti in [coda](com--queued-components.md), [sincronizzazione](com--synchronization.md)o pool di [oggetti](com--object-pooling.md), e che il componente effettua un certo numero di chiamate ad altri componenti com che possono essere attivati nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4286-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="f4286-119">In questo caso, è consigliabile attivare il componente chiamante nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4286-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="f4286-120">Se il componente COM richiede servizi COM+, non può essere contrassegnato come **deve essere attivato nel contesto predefinito**.</span><span class="sxs-lookup"><span data-stu-id="f4286-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="f4286-121">Inoltre, non esiste un miglioramento delle prestazioni reale se un oggetto COM attivato nel contesto predefinito esegue una serie di chiamate a oggetti in altri contesti.</span><span class="sxs-lookup"><span data-stu-id="f4286-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="f4286-122">Per informazioni dettagliate, vedere [contesti](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="f4286-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="f4286-123">**Per applicare l'attivazione nel contesto predefinito**</span><span class="sxs-lookup"><span data-stu-id="f4286-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="f4286-124">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova all'interno della cartella **componenti** di qualsiasi applicazione COM+ selezionata) che si desidera attivare nel contesto predefinito, quindi fare clic su **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="f4286-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="f4286-125">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="f4286-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="f4286-126">Selezionare la casella **di controllo deve essere attivato nel contesto predefinito**.</span><span class="sxs-lookup"><span data-stu-id="f4286-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="f4286-127">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4286-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="f4286-128">Quando si esegue un componente configurato nel contesto predefinito, COM+ non attiva alcuno dei servizi configurati per tale componente.</span><span class="sxs-lookup"><span data-stu-id="f4286-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="f4286-129">Questi servizi sono nuovamente disponibili quando si deseleziona la casella **di controllo deve essere attivato nel contesto predefinito** ed eseguire successivamente il componente configurato nel relativo contesto.</span><span class="sxs-lookup"><span data-stu-id="f4286-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f4286-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4286-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4286-131">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="f4286-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="f4286-132">Applicazione dell'attivazione nel contesto del chiamante</span><span class="sxs-lookup"><span data-stu-id="f4286-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



