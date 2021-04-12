---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330239"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="ebffb-103">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="ebffb-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="ebffb-104">Testo</span><span class="sxs-lookup"><span data-stu-id="ebffb-104">Text</span></span>

<span data-ttu-id="ebffb-105">L'elemento con un ControlType di {0} deve supportare almeno uno di questi modelli: {1} ma questo elemento non</span><span class="sxs-lookup"><span data-stu-id="ebffb-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="ebffb-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebffb-106">Type</span></span>

<span data-ttu-id="ebffb-107">Errore</span><span class="sxs-lookup"><span data-stu-id="ebffb-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ebffb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebffb-108">Description</span></span>

<span data-ttu-id="ebffb-109">Il supporto per l'automazione interfaccia utente dell'elemento non è conforme alla specifica di automazione interfaccia utente, perché l'elemento deve supportare almeno uno dei pattern di controllo forniti.</span><span class="sxs-lookup"><span data-stu-id="ebffb-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="ebffb-110">Di conseguenza, questo elemento potrebbe non essere esposto correttamente alle tecnologie assistive, che potrebbero avere un notevole effetto sull'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="ebffb-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ebffb-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ebffb-111">Possible causes</span></span>

-   <span data-ttu-id="ebffb-112">Implementazione di automazione interfaccia utente incompleta.</span><span class="sxs-lookup"><span data-stu-id="ebffb-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="ebffb-113">La proprietà ControlType non è impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ebffb-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebffb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebffb-114">Remarks</span></span>

<span data-ttu-id="ebffb-115">AccChecker registra questo messaggio di errore per un indicatore di stato indeterminato.</span><span class="sxs-lookup"><span data-stu-id="ebffb-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="ebffb-116">È possibile ignorare questo messaggio e/o aggiungerlo all'elenco delle eliminazioni.</span><span class="sxs-lookup"><span data-stu-id="ebffb-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebffb-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebffb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebffb-118">**\_CONTROLTYPEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="ebffb-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="ebffb-119">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ebffb-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ebffb-120">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ebffb-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




