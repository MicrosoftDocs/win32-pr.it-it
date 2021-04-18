---
title: Differenze tra i modelli a oggetti
description: Differenze tra i modelli a oggetti
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, differenze di versione
- modello a oggetti, differenze di versione
- Controllo ActiveX di Windows Media Player, differenze di versione
- Controllo ActiveX, differenze di versione
- Controllo ActiveX Windows Media Player Mobile, differenze di versione
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, differenze di versione
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298569"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="4cd2b-112">Differenze tra i modelli a oggetti</span><span class="sxs-lookup"><span data-stu-id="4cd2b-112">Differences Between the Object Models</span></span>

<span data-ttu-id="4cd2b-113">Esistono due differenze principali tra il modello a oggetti di Windows Media Player 6,4 e il modello a oggetti di Windows Media Player 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="4cd2b-114">**CLSID** Il modello a oggetti di Windows Media Player 7 o versione successiva è una partenza completa del modello a oggetti della versione 6,4.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="4cd2b-115">Per la specifica Component Object Model (COM) è necessario che tutte le interfacce esistenti continuino a funzionare nelle nuove versioni di un componente COM.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="4cd2b-116">Ciò significa che è possibile aggiungere nuove interfacce a un componente COM, ma le interfacce esistenti non devono mai essere modificate, garantendo che il codice client precedente funzioni sempre con il componente specifico che è stato progettato per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="4cd2b-117">Pertanto, il controllo ActiveX Windows Media Player 7 o versione successiva ha un nuovo ID classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="4cd2b-118">Se si desidera sfruttare le nuove funzionalità del controllo per questa versione, è necessario modificare il CLSID.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="4cd2b-119">**Modello a oggetti gerarchico** Se si usa il controllo ActiveX di Windows Media Player 6,4, si è notato che è possibile accedere a tutte le proprietà, i metodi e gli eventi tramite lo stesso oggetto, ovvero l'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="4cd2b-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="4cd2b-120">Al contrario, il modello a oggetti di Windows Media Player 7 o versione successiva è organizzato come una gerarchia di oggetti.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="4cd2b-121">L'oggetto **Player** è ancora l'oggetto radice, ma a questo punto è possibile accedere alle funzioni tramite una varietà di oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="4cd2b-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cd2b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cd2b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd2b-123">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="4cd2b-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




