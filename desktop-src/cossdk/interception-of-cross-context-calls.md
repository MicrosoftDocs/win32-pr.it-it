---
description: Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate oltre il limite del contesto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Intercettazione di chiamate tra contesti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342261"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="2f30b-103">Intercettazione di chiamate tra contesti</span><span class="sxs-lookup"><span data-stu-id="2f30b-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="2f30b-104">Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate oltre il limite del contesto.</span><span class="sxs-lookup"><span data-stu-id="2f30b-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="2f30b-105">Le chiamate attraverso il limite del contesto vengono gestite con proxy leggeri.</span><span class="sxs-lookup"><span data-stu-id="2f30b-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="2f30b-106">Questi proxy gestiscono la mediazione necessaria per modificare l'ambiente di runtime da uno che lo inserisce nel chiamante, in modo che sia in grado di ospitare il chiamato.</span><span class="sxs-lookup"><span data-stu-id="2f30b-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="2f30b-107">Questo processo è noto come *intercettazione*.</span><span class="sxs-lookup"><span data-stu-id="2f30b-107">This process is known as *interception*.</span></span>

<span data-ttu-id="2f30b-108">L'intercettazione delle chiamate tra contesti è necessaria perché gli oggetti in contesti diversi hanno requisiti di runtime diversi, questo è esattamente il motivo per i contesti.</span><span class="sxs-lookup"><span data-stu-id="2f30b-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="2f30b-109">COM+ intercetta tutti i riferimenti a oggetti passati come parametri del metodo e li converte automaticamente in proxy in modo che possano essere utilizzati nel nuovo contesto.</span><span class="sxs-lookup"><span data-stu-id="2f30b-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="2f30b-110">Se si condividono i riferimenti agli oggetti tra i limiti del contesto in altri modi, ad esempio in variabili globali, è sempre necessario usare [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="2f30b-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="2f30b-111">Queste funzioni possono convertire un riferimento a un oggetto in un proxy utilizzabile in un contesto diverso.</span><span class="sxs-lookup"><span data-stu-id="2f30b-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="2f30b-112">Non condividere mai un riferimento a un oggetto non elaborato tra i limiti del contesto.</span><span class="sxs-lookup"><span data-stu-id="2f30b-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="2f30b-113">Il comportamento delle chiamate nel contesto può avere conseguenze indesiderate nel caso di oggetti che espongono interfacce che non possono essere sottoposte a marshalling.</span><span class="sxs-lookup"><span data-stu-id="2f30b-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="2f30b-114">In questo caso, è probabile che si voglia insistere sul fatto che l'oggetto di cui non è possibile effettuare il marshalling venga attivato solo nel contesto del chiamante e mai nel suo contesto.</span><span class="sxs-lookup"><span data-stu-id="2f30b-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="2f30b-115">Questa operazione può essere eseguita selezionando l'opzione **deve essere attivata nel contesto del chiamante** nella scheda **attivazione** della pagina **proprietà** componente.</span><span class="sxs-lookup"><span data-stu-id="2f30b-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="2f30b-116">Per istruzioni dettagliate, vedere [applicazione dell'attivazione nel contesto del chiamante](enforcing-activation-in-the-caller-s-context.md) .</span><span class="sxs-lookup"><span data-stu-id="2f30b-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f30b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f30b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f30b-118">Attivazione del contesto</span><span class="sxs-lookup"><span data-stu-id="2f30b-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
