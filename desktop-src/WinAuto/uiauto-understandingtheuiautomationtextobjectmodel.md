---
title: Informazioni sul modello a oggetti testo di automazione interfaccia utente
description: Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft accedono al contenuto testuale di un controllo basato su testo.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- client, informazioni sul modello a oggetti testo di automazione interfaccia utente
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo Text
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709340"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="b97f1-108">Informazioni sul modello a oggetti testo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b97f1-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="b97f1-109">Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft accedono al contenuto testuale di un controllo basato su testo.</span><span class="sxs-lookup"><span data-stu-id="b97f1-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="b97f1-110">Modello a oggetti specifico del controllo</span><span class="sxs-lookup"><span data-stu-id="b97f1-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="b97f1-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b97f1-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="b97f1-112">I controlli basati su testo espongono contenuto testuale per le applicazioni client di automazione interfaccia utente tramite un modello a oggetti testo semplice.</span><span class="sxs-lookup"><span data-stu-id="b97f1-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="b97f1-113">Le applicazioni client possono accedere al modello a oggetti testo tramite le interfacce del pattern [di controllo Text e TextRange](uiauto-about-text-and-textrange-patterns.md) , inclusi [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="b97f1-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="b97f1-114">Le applicazioni client possono usare queste interfacce per recuperare contenuto testuale, attributi di testo e oggetti incorporati, ad esempio tabelle e collegamenti ipertestuali, da controlli basati su testo.</span><span class="sxs-lookup"><span data-stu-id="b97f1-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="b97f1-115">I tipi di controllo che supportano il modello a oggetti testo di automazione interfaccia utente includono i tipi di controllo [modifica](uiauto-supporteditcontroltype.md) e [documento](uiauto-supportdocumentcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="b97f1-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="b97f1-116">Altri tipi di controllo, ad esempio [Descrizione comando](uiauto-supporttooltipcontroltype.md) e [testo](uiauto-supporttextcontroltype.md) , potrebbero supportare anche il modello a oggetti testo, ma non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="b97f1-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="b97f1-117">Il modello a oggetti testo di automazione interfaccia utente non fornisce un mezzo per inserire o modificare il testo.</span><span class="sxs-lookup"><span data-stu-id="b97f1-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="b97f1-118">Tuttavia, alcuni controlli consentono di inserire o modificare il testo tramite l'interfaccia [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o tramite input diretto da tastiera.</span><span class="sxs-lookup"><span data-stu-id="b97f1-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="b97f1-119">Modello a oggetti specifico del controllo</span><span class="sxs-lookup"><span data-stu-id="b97f1-119">Control-specific Object Model</span></span>

<span data-ttu-id="b97f1-120">Un controllo basato su testo che implementa il proprio Document Object Model (DOM) può esporre il DOM implementando il pattern di controllo [ObjectModel](uiauto-implementingobjectmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="b97f1-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="b97f1-121">L'esposizione del DOM può consentire alle applicazioni client di accedere e controllare ulteriormente il contenuto di un controllo basato su testo.</span><span class="sxs-lookup"><span data-stu-id="b97f1-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="b97f1-122">Un'applicazione client può individuare se un particolare controllo basato su testo implementa un DOM recuperando l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del controllo.</span><span class="sxs-lookup"><span data-stu-id="b97f1-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="b97f1-123">Chiamare quindi il metodo [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , specificando l'identificatore della proprietà [**\_ IsObjectModelPatternAvailablePropertyId di UIA**](uiauto-control-pattern-availability-propids.md) e una variante che riceve true se il controllo implementa un Dom.</span><span class="sxs-lookup"><span data-stu-id="b97f1-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="b97f1-124">Per accedere al DOM, chiamare il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , specificando l'identificatore del pattern di controllo [**\_ ObjectModelPatternId di UIA**](uiauto-controlpattern-ids.md) e una variabile che riceve l'interfaccia [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) .</span><span class="sxs-lookup"><span data-stu-id="b97f1-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="b97f1-125">Chiamare il metodo [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) per recuperare l'interfaccia Dom.</span><span class="sxs-lookup"><span data-stu-id="b97f1-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b97f1-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b97f1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97f1-127">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="b97f1-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="b97f1-128">Supporto di automazione interfaccia utente per contenuto testuale</span><span class="sxs-lookup"><span data-stu-id="b97f1-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="b97f1-129">Utilizzo di controlli basati su testo</span><span class="sxs-lookup"><span data-stu-id="b97f1-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




