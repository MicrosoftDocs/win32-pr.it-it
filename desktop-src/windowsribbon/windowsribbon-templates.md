---
title: Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento
description: I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basate su una combinazione di comportamenti predefiniti e modelli di layout (sia definiti dal framework che personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti di layout adattivi del framework della barra multifunzione che influenzano il modo in cui i controlli nella barra dei comandi si adattano alle varie dimensioni della barra multifunzione in fase di esecuzione.
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
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444142"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="0154f-111">Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="0154f-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="0154f-112">I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basate su una combinazione di comportamenti predefiniti e modelli di layout (sia definiti dal framework che personalizzati) come dichiarati nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="0154f-113">Queste regole definiscono i comportamenti di layout adattivi del framework della barra multifunzione che influenzano il modo in cui i controlli nella barra dei comandi si adattano alle varie dimensioni della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="0154f-114">Introduzione</span><span class="sxs-lookup"><span data-stu-id="0154f-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="0154f-115">Modelli sizedefinition della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0154f-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="0154f-116">Modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="0154f-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="0154f-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0154f-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0154f-118">Introduzione</span><span class="sxs-lookup"><span data-stu-id="0154f-118">Introduction</span></span>

<span data-ttu-id="0154f-119">Il layout adattivo, come definito dal framework della barra multifunzione, è la possibilità di tutti i controlli all'interno dell'interfaccia utente della barra multifunzione di modificare dinamicamente l'organizzazione, le dimensioni, il formato e la scala relativa in base alle modifiche apportate alle dimensioni della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="0154f-120">Il framework espone la funzionalità di layout adattivo tramite un set di elementi di markup dedicati alla specifica e alla personalizzazione di vari comportamenti di layout.</span><span class="sxs-lookup"><span data-stu-id="0154f-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="0154f-121">Una raccolta di modelli, denominata [**SizeDefinitions,**](windowsribbon-element-sizedefinition.md)è definita dal framework, ognuno dei quali supporta vari scenari di controllo e layout.</span><span class="sxs-lookup"><span data-stu-id="0154f-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="0154f-122">Tuttavia, il framework supporta anche modelli personalizzati se i modelli predefiniti non forniscono l'esperienza dell'interfaccia utente o i layout richiesti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0154f-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="0154f-123">Per visualizzare i controlli in un layout preferito con una determinata dimensione della barra multifunzione, sia i modelli predefiniti che i modelli personalizzati funzionano in combinazione con [**l'elemento ScalingPolicy.**](windowsribbon-element-scalingpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="0154f-124">Questo elemento contiene un manifesto delle preferenze di dimensioni che il framework usa come guida per il rendering della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="0154f-125">Il framework della barra multifunzione fornisce comportamenti di layout predefiniti basati su un set di euristica predefinita per l'organizzazione e la presentazione dei controlli in fase di esecuzione senza la necessità di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0154f-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="0154f-126">Tuttavia, questa funzionalità è destinata solo a scopo di prototipazione.</span><span class="sxs-lookup"><span data-stu-id="0154f-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="0154f-127">Modelli sizedefinition della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0154f-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="0154f-128">Il framework della barra multifunzione fornisce un set completo di [**modelli SizeDefinition**](windowsribbon-element-sizedefinition.md) che specificano le dimensioni e il comportamento del layout per [un gruppo](windowsribbon-controls-group.md) di controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="0154f-129">Questi modelli riguardano gli scenari più comuni per l'organizzazione dei controlli in un'applicazione barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="0154f-130">Per applicare un'esperienza utente coerente tra le applicazioni della barra multifunzione, ogni modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restrizioni ai controlli o alla famiglia di controlli supportati.</span><span class="sxs-lookup"><span data-stu-id="0154f-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="0154f-131">Ad esempio, la famiglia di controlli button include:</span><span class="sxs-lookup"><span data-stu-id="0154f-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="0154f-132">Button</span><span class="sxs-lookup"><span data-stu-id="0154f-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="0154f-133">Interruttore</span><span class="sxs-lookup"><span data-stu-id="0154f-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="0154f-134">Pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="0154f-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="0154f-135">Pulsante Dividi</span><span class="sxs-lookup"><span data-stu-id="0154f-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="0154f-136">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="0154f-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="0154f-137">Raccolta pulsanti di divisione</span><span class="sxs-lookup"><span data-stu-id="0154f-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="0154f-138">Elenco a discesa Selezione colori</span><span class="sxs-lookup"><span data-stu-id="0154f-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="0154f-139">Mentre la famiglia di controlli di input include:</span><span class="sxs-lookup"><span data-stu-id="0154f-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="0154f-140">ComboBox</span><span class="sxs-lookup"><span data-stu-id="0154f-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="0154f-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="0154f-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="0154f-142">[Check Box](windowsribbon-controls-checkbox.md) e [Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) non appartengono alla famiglia di pulsanti o alla famiglia di input.</span><span class="sxs-lookup"><span data-stu-id="0154f-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="0154f-143">Questi due controlli possono essere usati solo se indicati in modo esplicito in un [**modello SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="0154f-144">Di seguito è riportato un elenco dei [**modelli SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descrizione del layout e dei controlli consentiti da ogni modello.</span><span class="sxs-lookup"><span data-stu-id="0154f-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0154f-145">Se i controlli dichiarati nel markup non vengono mappati esattamente al tipo [](windowsribbon-compilationerrors.md) di controllo, all'ordine e alla quantità definiti nel modello associato, viene registrato un errore di convalida dal compilatore [di markup](windowsribbon-intentcl.md) e la compilazione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="0154f-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="0154f-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="0154f-146">OneButton</span></span>

<span data-ttu-id="0154f-147">Un controllo famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-147">One button-family control.</span></span><br/> <span data-ttu-id="0154f-148">Sono supportate solo le dimensioni del gruppo large.</span><span class="sxs-lookup"><span data-stu-id="0154f-148">Only Large group size is supported.</span></span><br/>

![immagine del modello di definizione delle dimensioni di un pulsante.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="0154f-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-150">TwoButtons</span></span>

<span data-ttu-id="0154f-151">Due controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-151">Two button-family controls.</span></span><br/> <span data-ttu-id="0154f-152">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-152">Only Large and Medium group sizes are supported.</span></span><br/>

![immagine del modello di definizione delle dimensioni di grandi dimensioni a due pulsanti.](images/overviews/sizedefinition-twobuttons-large.png)

![Immagine del modello twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="0154f-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-155">ThreeButtons</span></span>

<span data-ttu-id="0154f-156">Tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-156">Three button-family controls.</span></span><br/> <span data-ttu-id="0154f-157">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-157">Only Large and Medium group sizes are supported.</span></span><br/>

![Immagine di un modello di definizione di dimensioni di grandi dimensioni a tre pulsanti.](images/overviews/sizedefinition-threebuttons-large.png)

![Immagine del modello di definizione a tre pulsanti di dimensioni medie.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="0154f-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="0154f-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="0154f-161">Tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-161">Three button-family controls.</span></span><br/> <span data-ttu-id="0154f-162">Il primo pulsante viene presentato in modo evidente in tutte e tre le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0154f-162">The first button is presented prominently in all three sizes.</span></span><br/>

![immagine del modello threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![immagine del modello threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![immagine del modello threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="0154f-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="0154f-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="0154f-167">Tre controlli della famiglia di pulsanti accompagnati da un singolo controllo CheckBox.</span><span class="sxs-lookup"><span data-stu-id="0154f-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="0154f-168">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-168">Only Large and Medium group sizes are supported.</span></span><br/>

![immagine del modello threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![immagine del modello threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="0154f-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-171">FourButtons</span></span>

<span data-ttu-id="0154f-172">Quattro controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-172">Four button-family controls.</span></span><br/>

![immagine del modello di definizione delle dimensioni di grandi dimensioni a quattro pulsanti.](images/overviews/sizedefinition-fourbuttons-large.png)

![Immagine del modello fourbuttons medium sizedefinition.](images/overviews/sizedefinition-fourbuttons-medium.png)

![Immagine del modello small sizedefinition a quattro pulsanti.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="0154f-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-176">FiveButtons</span></span>

<span data-ttu-id="0154f-177">Cinque controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-177">Five button-family controls.</span></span><br/>

![Immagine di un modello di definizione di dimensioni di grandi dimensioni a cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-large.png)

![Immagine del modello di definizione di dimensioni medie dei cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Immagine di un modello di definizione di dimensioni ridotte a cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="0154f-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-181">FiveOrSixButtons</span></span>

<span data-ttu-id="0154f-182">Cinque controlli della famiglia di pulsanti e un sesto pulsante facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0154f-182">Five button-family controls and an optional sixth button.</span></span><br/>

![immagine di fiveorsixbuttons large sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![immagine di fiveorsixbuttons medium sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![immagine di fiveorsixbuttons small sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="0154f-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-186">SixButtons</span></span>

<span data-ttu-id="0154f-187">Sei controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-187">Six button-family controls.</span></span><br/>

![immagine del modello di definizione di dimensioni di grandi dimensioni a sei pulsanti.](images/overviews/sizedefinition-sixbuttons-large.png)

![immagine del modello sixbuttons medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Immagine del modello small sizedefinition a sei pulsanti.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="0154f-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="0154f-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="0154f-192">Sei controlli della famiglia di pulsanti (presentazione alternativa).</span><span class="sxs-lookup"><span data-stu-id="0154f-192">Six button-family controls (alternate presentation).</span></span><br/>

![immagine del modello di definizione delle dimensioni large sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![modello sixbuttons-twocolumns medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Immagine del modello small sizedefinition a sei pulsanti a due colonne.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="0154f-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-196">SevenButtons</span></span>

<span data-ttu-id="0154f-197">Sette controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-197">Seven button-family controls.</span></span><br/>

![immagine del modello di definizione delle dimensioni di dimensioni di sette pulsanti.](images/overviews/sizedefinition-sevenbuttons-large.png)

![immagine del modello sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![immagine del modello di definizione di dimensioni ridotte di sette pulsanti.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="0154f-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-201">EightButtons</span></span>

<span data-ttu-id="0154f-202">Otto controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-202">Eight button-family controls.</span></span><br/>

![immagine di eightbuttons-lastthreesmall large sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![immagine di eightbuttons-lastthreesmall medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![immagine di eightbuttons-lastthreesmall small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="0154f-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="0154f-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="0154f-207">Otto controlli della famiglia di pulsanti (presentazione alternativa).</span><span class="sxs-lookup"><span data-stu-id="0154f-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="0154f-208">Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in due elementi [**ControlGroup:**](windowsribbon-element-controlgroup.md) uno per i primi cinque elementi e uno per gli ultimi tre elementi.</span><span class="sxs-lookup"><span data-stu-id="0154f-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="0154f-209">Nell'esempio seguente viene illustrato il markup necessario per questo modello.</span><span class="sxs-lookup"><span data-stu-id="0154f-209">The following example demonstrates the markup required for this template.</span></span><br/>

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



![Immagine di un modello di definizione delle dimensioni di grandi dimensioni a otto pulsanti.](images/overviews/sizedefinition-eightbuttons-large.png)

![Immagine del modello di definizione delle dimensioni medie degli otto pulsanti.](images/overviews/sizedefinition-eightbuttons-medium.png)

![immagine di otto pulsanti small sizedefinition modello.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="0154f-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-213">NineButtons</span></span>

<span data-ttu-id="0154f-214">Nove controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-214">Nine button-family controls.</span></span>

![Immagine del modello ninebuttons large sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![Immagine del modello ninebuttons medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Immagine del modello ninebuttons small sizedefinition.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="0154f-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-218">TenButtons</span></span>

<span data-ttu-id="0154f-219">Dieci controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-219">Ten button-family controls.</span></span>

![Immagine del modello tenbuttons large sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![Immagine del modello tenbuttons medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![Immagine del modello tenbuttons small sizedefinition.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="0154f-223">ElevenButtons</span><span class="sxs-lookup"><span data-stu-id="0154f-223">ElevenButtons</span></span>

<span data-ttu-id="0154f-224">Undicesimo controllo della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-224">Eleven button-family controls.</span></span>

![Immagine di undicesimo modello sizedefinition di pulsanti di grandi dimensioni.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Immagine di undicesimo modello di definizione delle dimensioni medie dei pulsanti.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![immagine di undicesimobuttons small sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="0154f-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="0154f-228">OneFontControl</span></span>

<span data-ttu-id="0154f-229">Un [**oggetto FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="0154f-230">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0154f-231">L'inclusione [**di un oggetto FontControl**](windowsribbon-element-fontcontrol.md) all'interno di una definizione di modello personalizzata non è supportata dal framework.</span><span class="sxs-lookup"><span data-stu-id="0154f-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![immagine di un modello large sizedefinition di onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![immagine di un modello di definizione delle dimensioni medie di unfontcontrol.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="0154f-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="0154f-234">OneInRibbonGallery</span></span>

<span data-ttu-id="0154f-235">Un [**controllo InRibbonGallery.**](windowsribbon-element-inribbongallery.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="0154f-236">Sono supportate solo le dimensioni dei gruppi Large e Small.</span><span class="sxs-lookup"><span data-stu-id="0154f-236">Only Large and Small group sizes are supported.</span></span>

![immagine di un modello oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![immagine di un modello oneinribbongallery small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="0154f-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="0154f-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="0154f-240">Un [**controllo InRibbonGallery**](windowsribbon-element-inribbongallery.md) e un controllo famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="0154f-241">Sono supportate solo le dimensioni dei gruppi Large e Small.</span><span class="sxs-lookup"><span data-stu-id="0154f-241">Only Large and Small group sizes are supported.</span></span>

![immagine del modello inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![immagine del modello inribbongalleryandbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="0154f-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="0154f-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="0154f-245">Un [controllo Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) e due o tre controlli della famiglia di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="0154f-246">La raccolta viene compressa nella rappresentazione Popup nelle dimensioni dei gruppi Medio e Piccolo.</span><span class="sxs-lookup"><span data-stu-id="0154f-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![immagine di inribbongalleryandbuttons-galleryscalesfirst large sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="0154f-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="0154f-250">ButtonGroups</span></span>

<span data-ttu-id="0154f-251">Una disposizione complessa di 32 controlli della famiglia di pulsanti (la maggior parte dei quali sono facoltativi).</span><span class="sxs-lookup"><span data-stu-id="0154f-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="0154f-252">A parte il pulsante facoltativo a dimensione intera del modello ButtonGroups di grandi dimensioni, tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli [**elementi ControlGroup.**](windowsribbon-element-controlgroup.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="0154f-253">L'esempio seguente illustra il markup necessario per visualizzare tutti e 32 gli elementi di controllo (obbligatori e facoltativi) con questo modello.</span><span class="sxs-lookup"><span data-stu-id="0154f-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


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



![immagine del modello buttongroups large sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![Immagine del modello buttongroups medium sizedefinition.](images/overviews/sizedefinition-buttongroups-medium.png)

![immagine del modello buttongroups small sizedefinition.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="0154f-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="0154f-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="0154f-258">Due controlli della famiglia di input (il secondo è facoltativo) seguiti da una disposizione complessa di 29 controlli della famiglia di pulsanti (la maggior parte dei quali è facoltativa).</span><span class="sxs-lookup"><span data-stu-id="0154f-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="0154f-259">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="0154f-260">Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli [**elementi ControlGroup.**](windowsribbon-element-controlgroup.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="0154f-261">Nell'esempio seguente viene illustrato il markup necessario per visualizzare tutti gli elementi del controllo (obbligatori e facoltativi) con questo modello.</span><span class="sxs-lookup"><span data-stu-id="0154f-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


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



![immagine di buttongroupsandinputs large sizedefinition template.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![immagine del modello buttongroupsandinputs medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="0154f-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="0154f-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="0154f-265">Due controlli della famiglia di pulsanti (entrambi facoltativi) seguiti da due o tre pulsanti o controlli della famiglia di input.</span><span class="sxs-lookup"><span data-stu-id="0154f-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="0154f-266">Sono supportate solo le dimensioni dei gruppi Large e Medium.</span><span class="sxs-lookup"><span data-stu-id="0154f-266">Only Large and Medium group sizes are supported.</span></span>

![immagine di bigbuttonsandsmallbuttonsorinputs large sizedefinition template.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![immagine del modello bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="0154f-269">Esempio di SizeDefinition di base</span><span class="sxs-lookup"><span data-stu-id="0154f-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="0154f-270">L'esempio di codice seguente fornisce una dimostrazione di base di come dichiarare un [**modello SizeDefinition**](windowsribbon-element-sizedefinition.md) nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="0154f-271">*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) viene usato per questo particolare esempio, ma tutti i modelli di framework vengono specificati in modo simile.</span><span class="sxs-lookup"><span data-stu-id="0154f-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="0154f-272">Esempio di SizeDefinition complesso con criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="0154f-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="0154f-273">Il comportamento di compressione dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) può essere controllato tramite l'uso di criteri di ridimensionamento nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="0154f-274">[**L'elemento ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifesto delle dichiarazioni [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e [**Scale**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattivo per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="0154f-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="0154f-275">È consigliabile che i dettagli dei criteri di ridimensionamento adeguati siano specificati in modo che la maggior parte degli elementi [**Group,**](windowsribbon-element-group.md) se non tutti, siano associati a un elemento [**Scale**](windowsribbon-element-scale.md) in cui l'attributo *Size* è uguale a `Popup` .</span><span class="sxs-lookup"><span data-stu-id="0154f-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="0154f-276">In questo modo il framework può eseguire il rendering della barra multifunzione con le dimensioni più piccole possibili e supportare la più ampia gamma di dispositivi di visualizzazione, prima di introdurre automaticamente un meccanismo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="0154f-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="0154f-277">L'esempio di codice seguente illustra un manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) che specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda Home.** Inoltre, gli [**elementi Scale**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di dimensione decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="0154f-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



### <a name="custom-templates"></a><span data-ttu-id="0154f-278">Modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="0154f-278">Custom Templates</span></span>

<span data-ttu-id="0154f-279">Se i comportamenti di layout predefiniti e i modelli Predefiniti di [**SizeDefinition**](windowsribbon-element-sizedefinition.md) non offrono la flessibilità o il supporto per uno scenario di layout specifico, i modelli personalizzati sono supportati dal framework della barra multifunzione tramite l'elemento [**Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="0154f-280">I modelli personalizzati possono essere dichiarati in due modi: un metodo autonomo che usa l'elemento [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) per dichiarare modelli riutilizzabili, denominati o un metodo inline specifico di [**Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="0154f-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="0154f-281">Modello autonomo</span><span class="sxs-lookup"><span data-stu-id="0154f-281">Standalone Template</span></span>

<span data-ttu-id="0154f-282">L'esempio di codice seguente illustra un modello personalizzato di base riutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="0154f-282">The following code example illustrates a basic, reusable custom template.</span></span>


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



### <a name="inline-template"></a><span data-ttu-id="0154f-283">Modello inline</span><span class="sxs-lookup"><span data-stu-id="0154f-283">Inline Template</span></span>

<span data-ttu-id="0154f-284">Gli esempi di codice seguenti illustrano un modello personalizzato inline di base per un gruppo di quattro pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="0154f-285">Questa sezione di codice illustra le dichiarazioni command per un gruppo di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0154f-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="0154f-286">Qui vengono specificate anche risorse di immagini di grandi e piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0154f-286">Large and small image resources are also specified here.</span></span>


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



<span data-ttu-id="0154f-287">Questa sezione di codice illustra come definire modelli [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) di grandi, medie e piccole dimensioni per visualizzare i quattro pulsanti di varie dimensioni e layout.</span><span class="sxs-lookup"><span data-stu-id="0154f-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="0154f-288">La [**dichiarazione ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per la scheda definisce quale modello viene usato per un gruppo di controlli in base alle dimensioni e allo spazio della barra multifunzione richiesti dalla scheda attiva.</span><span class="sxs-lookup"><span data-stu-id="0154f-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


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



<span data-ttu-id="0154f-289">Le immagini seguenti illustrano come vengono applicati i modelli dell'esempio precedente all'interfaccia utente della barra multifunzione per ridurre le dimensioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0154f-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|  <span data-ttu-id="0154f-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="0154f-290">Type</span></span>  |      <span data-ttu-id="0154f-291">Immagine</span><span class="sxs-lookup"><span data-stu-id="0154f-291">Image</span></span>                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0154f-292">Grande</span><span class="sxs-lookup"><span data-stu-id="0154f-292">Large</span></span>  | ![immagine di un modello personalizzato di grandi dimensioni inline.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="0154f-294">Medio</span><span class="sxs-lookup"><span data-stu-id="0154f-294">Medium</span></span> | ![Immagine di un modello personalizzato medio inline.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="0154f-296">Small</span><span class="sxs-lookup"><span data-stu-id="0154f-296">Small</span></span>  | ![immagine di un modello personalizzato di piccole dimensioni inline.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="0154f-298">Popup</span><span class="sxs-lookup"><span data-stu-id="0154f-298">Popup</span></span>  | ![immagine di un modello personalizzato popup inline.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="0154f-300">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0154f-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0154f-301">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="0154f-301">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="0154f-302">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="0154f-302">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="0154f-303">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="0154f-303">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





