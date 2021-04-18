---
title: Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità
description: I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Barra multifunzione di Windows, personalizzazione
- Barra multifunzione, personalizzazione
- Barra multifunzione di Windows, modelli SizeDefinition
- Barra multifunzione, modelli SizeDefinition
- Barra multifunzione di Windows, modelli personalizzati
- Barra multifunzione, modelli personalizzati
- personalizzazione della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "104554664"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="6b342-111">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="6b342-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="6b342-112">I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="6b342-113">Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="6b342-114">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6b342-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="6b342-115">Modelli SizeDefinition della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="6b342-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="6b342-116">Modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="6b342-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="6b342-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b342-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="6b342-118">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6b342-118">Introduction</span></span>

<span data-ttu-id="6b342-119">Il layout adattivo, come definito dal framework della barra multifunzione, è la capacità di tutti i controlli all'interno dell'interfaccia utente della barra multifunzione di regolare dinamicamente l'organizzazione, le dimensioni, il formato e la scala relativa in base alle modifiche apportate alle dimensioni della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="6b342-120">Il Framework espone la funzionalità di layout adattivo tramite un set di elementi di markup dedicati per specificare e personalizzare diversi comportamenti di layout.</span><span class="sxs-lookup"><span data-stu-id="6b342-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="6b342-121">Un insieme di modelli, denominato [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), viene definito dal Framework, ognuno dei quali supporta vari scenari di controllo e layout.</span><span class="sxs-lookup"><span data-stu-id="6b342-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="6b342-122">Tuttavia, il Framework supporta anche modelli personalizzati se i modelli predefiniti non forniscono l'esperienza dell'interfaccia utente o i layout richiesti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6b342-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="6b342-123">Per visualizzare i controlli in un layout preferito a una determinata dimensione della barra multifunzione, sia i modelli predefiniti che i modelli personalizzati funzionano insieme all'elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="6b342-124">Questo elemento contiene un manifesto di preferenze di dimensione utilizzato dal Framework come guida durante il rendering della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="6b342-125">Il Framework Ribbon fornisce comportamenti di layout predefiniti basati su un set di regole euristiche predefinite per l'organizzazione e la presentazione di controlli in fase di esecuzione senza la necessità di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6b342-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="6b342-126">Questa funzionalità, tuttavia, è destinata solo ai prototipi.</span><span class="sxs-lookup"><span data-stu-id="6b342-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="6b342-127">Modelli SizeDefinition della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="6b342-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="6b342-128">Il Framework della barra multifunzione fornisce un set completo di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) che specificano il comportamento delle dimensioni e del layout per un [gruppo](windowsribbon-controls-group.md) di controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="6b342-129">Questi modelli riguardano scenari più comuni per organizzare i controlli in un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="6b342-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="6b342-130">Per applicare un'esperienza utente coerente tra le applicazioni della barra multifunzione, ogni modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restrizioni sui controlli o sulla famiglia di controlli supportati.</span><span class="sxs-lookup"><span data-stu-id="6b342-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="6b342-131">Ad esempio, la famiglia di controlli Button include:</span><span class="sxs-lookup"><span data-stu-id="6b342-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="6b342-132">Button</span><span class="sxs-lookup"><span data-stu-id="6b342-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="6b342-133">Interruttore</span><span class="sxs-lookup"><span data-stu-id="6b342-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="6b342-134">Pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="6b342-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="6b342-135">Pulsante di divisione</span><span class="sxs-lookup"><span data-stu-id="6b342-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="6b342-136">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="6b342-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="6b342-137">Raccolta di pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="6b342-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="6b342-138">Selezione colori a discesa</span><span class="sxs-lookup"><span data-stu-id="6b342-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="6b342-139">Sebbene la famiglia di controlli di input includa:</span><span class="sxs-lookup"><span data-stu-id="6b342-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="6b342-140">ComboBox</span><span class="sxs-lookup"><span data-stu-id="6b342-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="6b342-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="6b342-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="6b342-142">La [casella di controllo](windowsribbon-controls-checkbox.md) e la [raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) non appartengono al gruppo di pulsanti o alla famiglia di input.</span><span class="sxs-lookup"><span data-stu-id="6b342-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="6b342-143">Questi due controlli possono essere usati solo laddove indicato in modo esplicito in un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="6b342-144">Di seguito è riportato un elenco dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descrizione del layout e dei controlli consentiti da ogni modello.</span><span class="sxs-lookup"><span data-stu-id="6b342-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b342-145">Se i controlli dichiarati nel markup non eseguono esattamente il mapping al tipo di controllo, all'ordine e alla quantità definiti nel modello associato, viene registrato un [errore di convalida](windowsribbon-compilationerrors.md) da parte del [compilatore di markup](windowsribbon-intentcl.md) e la compilazione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="6b342-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="6b342-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="6b342-146">OneButton</span></span>

<span data-ttu-id="6b342-147">Un controllo della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-147">One button-family control.</span></span><br/> <span data-ttu-id="6b342-148">Sono supportate solo le dimensioni di gruppo grandi.</span><span class="sxs-lookup"><span data-stu-id="6b342-148">Only Large group size is supported.</span></span><br/>

![immagine del modello sizedefinition di OneButton.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="6b342-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-150">TwoButtons</span></span>

<span data-ttu-id="6b342-151">Due controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-151">Two button-family controls.</span></span><br/> <span data-ttu-id="6b342-152">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-152">Only Large and Medium group sizes are supported.</span></span><br/>

![immagine del modello sizedefinition di twobuttons di grandi dimensioni.](images/overviews/sizedefinition-twobuttons-large.png)

![immagine del modello sizedefinition twobuttons medium.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="6b342-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-155">ThreeButtons</span></span>

<span data-ttu-id="6b342-156">Tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-156">Three button-family controls.</span></span><br/> <span data-ttu-id="6b342-157">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-157">Only Large and Medium group sizes are supported.</span></span><br/>

![immagine del modello sizedefinition di threebuttons di grandi dimensioni.](images/overviews/sizedefinition-threebuttons-large.png)

![immagine del modello sizedefinition threebuttons medium.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="6b342-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="6b342-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="6b342-161">Tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-161">Three button-family controls.</span></span><br/> <span data-ttu-id="6b342-162">Il primo pulsante è riportato in evidenza in tutte e tre le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6b342-162">The first button is presented prominently in all three sizes.</span></span><br/>

![immagine di threebuttons-onebigandtwosmall modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![immagine del modello threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![immagine di threebuttons-onebigandtwosmall Small sizedefinition template.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="6b342-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="6b342-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="6b342-167">Tre controlli della famiglia di pulsanti accompagnati da un singolo controllo CheckBox.</span><span class="sxs-lookup"><span data-stu-id="6b342-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="6b342-168">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-168">Only Large and Medium group sizes are supported.</span></span><br/>

![immagine del modello sizedefinition di threebuttonsandonecheckbox di grandi dimensioni.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![immagine del modello sizedefinition threebuttonsandonecheckbox medium.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="6b342-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-171">FourButtons</span></span>

<span data-ttu-id="6b342-172">Quattro controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-172">Four button-family controls.</span></span><br/>

![immagine del modello sizedefinition di fourbuttons di grandi dimensioni.](images/overviews/sizedefinition-fourbuttons-large.png)

![immagine del modello sizedefinition fourbuttons medium.](images/overviews/sizedefinition-fourbuttons-medium.png)

![immagine di fourbuttons Small sizedefinition template.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="6b342-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-176">FiveButtons</span></span>

<span data-ttu-id="6b342-177">Cinque controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-177">Five button-family controls.</span></span><br/>

![immagine del modello sizedefinition di fivebuttons di grandi dimensioni.](images/overviews/sizedefinition-fivebuttons-large.png)

![immagine del modello sizedefinition fivebuttons medium.](images/overviews/sizedefinition-fivebuttons-medium.png)

![immagine di fivebuttons Small sizedefinition template.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="6b342-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-181">FiveOrSixButtons</span></span>

<span data-ttu-id="6b342-182">Cinque controlli della famiglia Button e un sesto pulsante facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6b342-182">Five button-family controls and an optional sixth button.</span></span><br/>

![immagine del modello sizedefinition di fiveorsixbuttons di grandi dimensioni.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![immagine del modello sizedefinition fiveorsixbuttons medium.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![immagine di fiveorsixbuttons Small sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="6b342-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-186">SixButtons</span></span>

<span data-ttu-id="6b342-187">Sei controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-187">Six button-family controls.</span></span><br/>

![immagine del modello sizedefinition di sixbuttons di grandi dimensioni.](images/overviews/sizedefinition-sixbuttons-large.png)

![immagine del modello sizedefinition sixbuttons medium.](images/overviews/sizedefinition-sixbuttons-medium.png)

![immagine di sixbuttons Small sizedefinition template.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="6b342-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="6b342-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="6b342-192">Sei controlli della famiglia di pulsanti (presentazione alternativa).</span><span class="sxs-lookup"><span data-stu-id="6b342-192">Six button-family controls (alternate presentation).</span></span><br/>

![immagine di sixbuttons-twocolumns modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns modello di sizedefinition medio.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![immagine di sixbuttons-twocolumns Small sizedefinition template.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="6b342-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-196">SevenButtons</span></span>

<span data-ttu-id="6b342-197">Sette controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-197">Seven button-family controls.</span></span><br/>

![immagine del modello sizedefinition di sevenbuttons di grandi dimensioni.](images/overviews/sizedefinition-sevenbuttons-large.png)

![immagine del modello mediumsizedefinition di sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![immagine di sevenbuttons Small sizedefinition template.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="6b342-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-201">EightButtons</span></span>

<span data-ttu-id="6b342-202">Otto controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-202">Eight button-family controls.</span></span><br/>

![immagine di eightbuttons-lastthreesmall modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![immagine del modello eightbuttons-lastthreesmall medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![immagine di eightbuttons-lastthreesmall Small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="6b342-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="6b342-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="6b342-207">Otto controlli della famiglia di pulsanti (presentazione alternativa).</span><span class="sxs-lookup"><span data-stu-id="6b342-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="6b342-208">Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in due elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) : uno per i primi cinque elementi e uno per gli ultimi tre elementi.</span><span class="sxs-lookup"><span data-stu-id="6b342-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="6b342-209">Nell'esempio seguente viene illustrato il markup necessario per questo modello.</span><span class="sxs-lookup"><span data-stu-id="6b342-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![immagine del modello sizedefinition di eightbuttons di grandi dimensioni.](images/overviews/sizedefinition-eightbuttons-large.png)

![immagine del modello sizedefinition eightbuttons medium.](images/overviews/sizedefinition-eightbuttons-medium.png)

![immagine di eightbuttons Small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="6b342-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-213">NineButtons</span></span>

<span data-ttu-id="6b342-214">Nove controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-214">Nine button-family controls.</span></span>

![immagine del modello sizedefinition di ninebuttons di grandi dimensioni.](images/overviews/sizedefinition-ninebuttons-large.png)

![immagine del modello sizedefinition ninebuttons medium.](images/overviews/sizedefinition-ninebuttons-medium.png)

![immagine di ninebuttons Small sizedefinition template.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="6b342-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-218">TenButtons</span></span>

<span data-ttu-id="6b342-219">Dieci controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-219">Ten button-family controls.</span></span>

![immagine del modello sizedefinition di tenbuttons di grandi dimensioni.](images/overviews/sizedefinition-tenbuttons-large.png)

![immagine del modello sizedefinition tenbuttons medium.](images/overviews/sizedefinition-tenbuttons-medium.png)

![immagine di tenbuttons Small sizedefinition template.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="6b342-223">ElevenButtons</span><span class="sxs-lookup"><span data-stu-id="6b342-223">ElevenButtons</span></span>

<span data-ttu-id="6b342-224">Undici controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-224">Eleven button-family controls.</span></span>

![immagine del modello sizedefinition di elevenbuttons di grandi dimensioni.](images/overviews/sizedefinition-elevenbuttons-large.png)

![immagine del modello sizedefinition elevenbuttons medium.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![immagine di elevenbuttons Small sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="6b342-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="6b342-228">OneFontControl</span></span>

<span data-ttu-id="6b342-229">Un [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6b342-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="6b342-230">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b342-231">L'inclusione di un [**FontControl**](windowsribbon-element-fontcontrol.md) all'interno di una definizione di modello personalizzata non è supportata dal Framework.</span><span class="sxs-lookup"><span data-stu-id="6b342-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![immagine del modello sizedefinition di onefontcontrol di grandi dimensioni.](images/overviews/sizedefinition-onefontcontrol-large.png)

![immagine del modello sizedefinition onefontcontrol medium.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="6b342-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="6b342-234">OneInRibbonGallery</span></span>

<span data-ttu-id="6b342-235">Un controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="6b342-236">Sono supportate solo dimensioni di gruppi di grandi dimensioni e di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="6b342-236">Only Large and Small group sizes are supported.</span></span>

![immagine del modello sizedefinition di oneinribbongallery di grandi dimensioni.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![immagine di oneinribbongallery Small sizedefinition template.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="6b342-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="6b342-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="6b342-240">Un controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) e un controllo della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="6b342-241">Sono supportate solo dimensioni di gruppi di grandi dimensioni e di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="6b342-241">Only Large and Small group sizes are supported.</span></span>

![immagine del modello sizedefinition di inribbongalleryandbigbutton di grandi dimensioni.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![immagine di inribbongalleryandbigbutton Small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="6b342-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="6b342-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="6b342-245">Un controllo [della raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) e due o tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="6b342-246">La raccolta comprime la rappresentazione popup in dimensioni medie e piccole del gruppo.</span><span class="sxs-lookup"><span data-stu-id="6b342-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![immagine di inribbongalleryandbuttons-galleryscalesfirst modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![immagine del modello inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="6b342-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="6b342-250">ButtonGroups</span></span>

<span data-ttu-id="6b342-251">Una disposizione complessa di controlli della famiglia di pulsanti 32 (la maggior parte dei quali è facoltativa).</span><span class="sxs-lookup"><span data-stu-id="6b342-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="6b342-252">Oltre al pulsante di ridimensionamento completo facoltativo del modello ButtonGroups di grandi dimensioni, tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="6b342-253">Nell'esempio seguente viene illustrato il markup necessario per visualizzare tutti gli elementi del controllo 32 (obbligatorio e facoltativo) con questo modello.</span><span class="sxs-lookup"><span data-stu-id="6b342-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![immagine del modello sizedefinition di buttongroups di grandi dimensioni.](images/overviews/sizedefinition-buttongroups-large.png)

![immagine del modello sizedefinition buttongroups medium.](images/overviews/sizedefinition-buttongroups-medium.png)

![immagine di buttongroups Small sizedefinition template.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="6b342-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="6b342-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="6b342-258">Due controlli della famiglia di input (il secondo è facoltativo) seguiti da una disposizione complessa di 29 controlli della famiglia di pulsanti (la maggior parte dei quali è facoltativa).</span><span class="sxs-lookup"><span data-stu-id="6b342-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="6b342-259">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="6b342-260">Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="6b342-261">Nell'esempio seguente viene illustrato il markup necessario per visualizzare tutti gli elementi del controllo (obbligatorio e facoltativo) con questo modello.</span><span class="sxs-lookup"><span data-stu-id="6b342-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![immagine del modello sizedefinition di buttongroupsandinputs di grandi dimensioni.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![immagine del modello sizedefinition buttongroupsandinputs medium.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="6b342-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="6b342-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="6b342-265">Due controlli della famiglia di pulsanti (entrambi facoltativi) seguiti da due o tre pulsanti o controlli della famiglia di input.</span><span class="sxs-lookup"><span data-stu-id="6b342-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="6b342-266">Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.</span><span class="sxs-lookup"><span data-stu-id="6b342-266">Only Large and Medium group sizes are supported.</span></span>

![immagine del modello sizedefinition di bigbuttonsandsmallbuttonsorinputs di grandi dimensioni.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![immagine del modello sizedefinition bigbuttonsandsmallbuttonsorinputs medium.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="6b342-269">Esempio di SizeDefinition di base</span><span class="sxs-lookup"><span data-stu-id="6b342-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="6b342-270">L'esempio di codice seguente fornisce una dimostrazione di base di come dichiarare un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="6b342-271">Per questo particolare esempio viene usato *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) , ma tutti i modelli di Framework sono specificati in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="6b342-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="6b342-272">Esempio SizeDefinition complesso con criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="6b342-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="6b342-273">Il comportamento di compressione dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) può essere controllato tramite l'uso di criteri di ridimensionamento nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="6b342-274">L'elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifesto di [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e le dichiarazioni di [**scala**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattivo per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="6b342-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="6b342-275">È consigliabile specificare i dettagli dei criteri di scalabilità adeguati in modo che la maggior parte degli elementi di [**gruppo**](windowsribbon-element-group.md) , se non tutti, siano associati a un elemento [**scale**](windowsribbon-element-scale.md) in cui l'attributo *size* è uguale a `Popup` .</span><span class="sxs-lookup"><span data-stu-id="6b342-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="6b342-276">Questa operazione consente al Framework di eseguire il rendering della barra multifunzione con le dimensioni minime possibili e di supportare la più ampia gamma di dispositivi di visualizzazione, prima di introdurre automaticamente un meccanismo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6b342-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="6b342-277">Nell'esempio di codice seguente viene illustrato un manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) che specifica una preferenza [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="6b342-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="6b342-278">Modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="6b342-278">Custom Templates</span></span>

<span data-ttu-id="6b342-279">Se i comportamenti di layout predefiniti e i modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti non offrono la flessibilità o il supporto per uno scenario di layout specifico, i modelli personalizzati sono supportati dal framework della barra multifunzione tramite l'elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="6b342-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="6b342-280">I modelli personalizzati possono essere dichiarati in due modi: un metodo autonomo che usa l'elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) per dichiarare i modelli riutilizzabili, denominati o un metodo inline specifico del [**gruppo**](windowsribbon-element-group.md).</span><span class="sxs-lookup"><span data-stu-id="6b342-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="6b342-281">Modello autonomo</span><span class="sxs-lookup"><span data-stu-id="6b342-281">Standalone Template</span></span>

<span data-ttu-id="6b342-282">Nell'esempio di codice riportato di seguito viene illustrato un modello personalizzato di base riutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="6b342-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="6b342-283">Modello inline</span><span class="sxs-lookup"><span data-stu-id="6b342-283">Inline Template</span></span>

<span data-ttu-id="6b342-284">Negli esempi di codice seguenti viene illustrato un modello personalizzato inline di base per un gruppo di quattro pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="6b342-285">In questa sezione del codice vengono illustrate le dichiarazioni di comando per un gruppo di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6b342-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="6b342-286">Qui sono specificate anche le risorse per immagini di grandi dimensioni e di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="6b342-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="6b342-287">Questa sezione di codice illustra come definire modelli [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) di grandi dimensioni, medi e piccoli per visualizzare i quattro pulsanti in diverse dimensioni e layout.</span><span class="sxs-lookup"><span data-stu-id="6b342-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="6b342-288">La Dichiarazione [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per la scheda definisce il modello usato per un gruppo di controlli in base alla dimensione della barra multifunzione e allo spazio richiesto dalla scheda attiva.</span><span class="sxs-lookup"><span data-stu-id="6b342-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="6b342-289">Le immagini seguenti mostrano come vengono applicati i modelli dell'esempio precedente all'interfaccia utente della barra multifunzione per ridurre le dimensioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6b342-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b342-290">Grande</span><span class="sxs-lookup"><span data-stu-id="6b342-290">Large</span></span>  | ![immagine di un modello personalizzato di grandi dimensioni in linea.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="6b342-292">Medio</span><span class="sxs-lookup"><span data-stu-id="6b342-292">Medium</span></span> | ![immagine di un modello personalizzato medio in linea.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="6b342-294">Piccola</span><span class="sxs-lookup"><span data-stu-id="6b342-294">Small</span></span>  | ![immagine di un modello personalizzato piccolo inline.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="6b342-296">Popup</span><span class="sxs-lookup"><span data-stu-id="6b342-296">Popup</span></span>  | ![immagine di un modello personalizzato popup in linea.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="6b342-298">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b342-298">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b342-299">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="6b342-299">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="6b342-300">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="6b342-300">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="6b342-301">**Group**</span><span class="sxs-lookup"><span data-stu-id="6b342-301">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





