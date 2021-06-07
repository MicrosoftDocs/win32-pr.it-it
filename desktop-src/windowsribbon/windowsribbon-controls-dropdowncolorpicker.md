---
title: Drop-Down Selezione colori
description: Il framework della barra multifunzione di Windows fornisce un controllo Drop-Down Selezione colori controllo che espone un'ampia gamma di impostazioni di colore tramite un pulsante di menu suddiviso e un selettore di colore a discesa personalizzabile.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443662"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="de8ca-103">Drop-Down Selezione colori</span><span class="sxs-lookup"><span data-stu-id="de8ca-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="de8ca-104">Il framework della barra multifunzione di Windows fornisce un controllo Drop-Down Selezione colori controllo che espone un'ampia gamma di impostazioni di colore tramite un pulsante di menu suddiviso e un selettore di colore a discesa personalizzabile.</span><span class="sxs-lookup"><span data-stu-id="de8ca-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="de8ca-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="de8ca-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="de8ca-106">markup</span><span class="sxs-lookup"><span data-stu-id="de8ca-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="de8ca-107">Codice</span><span class="sxs-lookup"><span data-stu-id="de8ca-107">Code</span></span>](#code)
    -   [<span data-ttu-id="de8ca-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="de8ca-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="de8ca-109">Gestori di comandi</span><span class="sxs-lookup"><span data-stu-id="de8ca-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="de8ca-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de8ca-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="de8ca-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="de8ca-111">Introduction</span></span>

<span data-ttu-id="de8ca-112">Grazie all'emulazione dell'aspetto e delle funzionalità della selezione colori di Microsoft Office, il framework della barra multifunzione è in grado di trarre vantaggio da e contribuire alla coerenza e alla familiarità in un'ampia gamma di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="de8ca-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="de8ca-113">markup</span><span class="sxs-lookup"><span data-stu-id="de8ca-113">Markup</span></span>

<span data-ttu-id="de8ca-114">Come tutti i controlli della barra multifunzione, Drop-Down Selezione colori è facilmente implementato e personalizzato tramite markup.</span><span class="sxs-lookup"><span data-stu-id="de8ca-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="de8ca-115">Il framework fornisce una serie di attributi dell'elemento per Drop-Down Selezione colori esporre vari livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="de8ca-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="de8ca-116">Nella tabella seguente sono elencati Drop-Down Selezione colori attributi.</span><span class="sxs-lookup"><span data-stu-id="de8ca-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de8ca-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="de8ca-117">Attribute</span></span></th>
<th><span data-ttu-id="de8ca-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de8ca-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de8ca-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="de8ca-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="de8ca-120">Modelli di layout che specificano il tipo di Drop-Down Selezione colori.</span><span class="sxs-lookup"><span data-stu-id="de8ca-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="de8ca-121">Sono disponibili tre modelli, ognuno dei quali specifica un layout di controllo e i valori predefiniti per gli attributi associati e le chiavi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="de8ca-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="de8ca-122">ChipSize</span></span></td>
<td><span data-ttu-id="de8ca-123">Dimensioni di ogni chip di colore (o campione).</span><span class="sxs-lookup"><span data-stu-id="de8ca-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="de8ca-124">Columns</span></span></td>
<td><span data-ttu-id="de8ca-125">Numero di colonne chip (o campione) di colore.</span><span class="sxs-lookup"><span data-stu-id="de8ca-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="de8ca-126">CommandName</span></span></td>
<td><span data-ttu-id="de8ca-127">Nome della dichiarazione Command associata.</span><span class="sxs-lookup"><span data-stu-id="de8ca-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="de8ca-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="de8ca-129">Visualizza o nasconde il <strong>pulsante</strong> Automatico.</span><span class="sxs-lookup"><span data-stu-id="de8ca-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="de8ca-130">Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="de8ca-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="de8ca-132">Visualizza (o nasconde) il <strong>pulsante Nessun</strong> colore.</span><span class="sxs-lookup"><span data-stu-id="de8ca-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="de8ca-133">Valido per tutti <em>i valori ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="de8ca-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="de8ca-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="de8ca-135">Numero di righe di chip di colori (o campione) nell'area <strong>Colori</strong> recenti.</span><span class="sxs-lookup"><span data-stu-id="de8ca-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="de8ca-136">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="de8ca-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="de8ca-138">Numero di righe chip di colori (o campione) nell'area <strong>Colori</strong> standard.</span><span class="sxs-lookup"><span data-stu-id="de8ca-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="de8ca-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="de8ca-140">Numero di righe chip di colori (o campione) nell'area <strong>Colori tema.</strong></span><span class="sxs-lookup"><span data-stu-id="de8ca-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="de8ca-141">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="de8ca-142">Le schermate seguenti illustrano i layout Drop-Down Selezione colori predefiniti per i tre modelli di colore.</span><span class="sxs-lookup"><span data-stu-id="de8ca-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8ca-143">`ThemeColors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su 'themecolors'. ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="de8ca-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="de8ca-144">`standardcolors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su 'standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="de8ca-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="de8ca-145">`highlightcolors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su "highlightcolors".](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="de8ca-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="de8ca-146">Il markup di base necessario per Drop-Down Selezione colori tipo di dati è illustrato negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="de8ca-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="de8ca-147">Il Drop-Down Selezione colori è un controllo [Button](windowsribbon-controls-button.md) valido in un [**modello SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="de8ca-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="de8ca-148">Codice</span><span class="sxs-lookup"><span data-stu-id="de8ca-148">Code</span></span>

<span data-ttu-id="de8ca-149">In quanto controllo specializzato che supporta la personalizzazione, qualsiasi implementazione del Drop-Down Selezione colori che sfrutta queste funzionalità richiede codice dell'applicazione specializzato per gestire le proprietà e gli eventuali comandi emessi dal controllo.</span><span class="sxs-lookup"><span data-stu-id="de8ca-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="de8ca-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="de8ca-150">Properties</span></span>

<span data-ttu-id="de8ca-151">Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il Drop-Down Selezione colori controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="de8ca-152">In genere, una Drop-Down Selezione colori viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)</span><span class="sxs-lookup"><span data-stu-id="de8ca-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="de8ca-153">L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)</span><span class="sxs-lookup"><span data-stu-id="de8ca-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="de8ca-154">Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework.</span><span class="sxs-lookup"><span data-stu-id="de8ca-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="de8ca-155">Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="de8ca-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="de8ca-156">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)</span><span class="sxs-lookup"><span data-stu-id="de8ca-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="de8ca-157">Nella tabella seguente sono elencate le chiavi di proprietà associate al Drop-Down Selezione colori controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de8ca-158">Chiave di proprietà</span><span class="sxs-lookup"><span data-stu-id="de8ca-158">Property Key</span></span></th>
<th><span data-ttu-id="de8ca-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de8ca-159">Description</span></span></th>
<th><span data-ttu-id="de8ca-160">Note</span><span class="sxs-lookup"><span data-stu-id="de8ca-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de8ca-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-162">Definisce l'etichetta per il <strong>pulsante Colore</strong> automatico.</span><span class="sxs-lookup"><span data-stu-id="de8ca-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="de8ca-163">Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="de8ca-164">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="de8ca-166">Definisce il valore del colore selezionato come <a href="/windows/win32/gdi/colorref">COLORREF.</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="de8ca-167">Valido solo quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> ha un valore pari a <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="de8ca-168">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="de8ca-170">Definisce il tipo di colore selezionato.</span><span class="sxs-lookup"><span data-stu-id="de8ca-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="de8ca-171">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="de8ca-173">Definisce la possibilità per un controllo di rispondere all'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="de8ca-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="de8ca-174">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="de8ca-176">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="de8ca-178">Definisce la stringa di caratteri per un'etichetta di controllo.</span><span class="sxs-lookup"><span data-stu-id="de8ca-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="de8ca-179">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="de8ca-181">Definisce l'immagine a contrasto elevato di grandi dimensioni da visualizzare per un controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="de8ca-182">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="de8ca-183">Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="de8ca-185">Definisce l'immagine grande da visualizzare per un controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="de8ca-186">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="de8ca-187">Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-189">Definisce l'etichetta per il <strong>pulsante Altri</strong> colori.</span><span class="sxs-lookup"><span data-stu-id="de8ca-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="de8ca-190">Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="de8ca-191">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-193">Definisce l'etichetta per il <strong>pulsante Nessun</strong> colore.</span><span class="sxs-lookup"><span data-stu-id="de8ca-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="de8ca-194">Valido per tutti <em>i valori ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="de8ca-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="de8ca-195">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-197">Definisce l'etichetta per la <strong>categoria Colori</strong> recenti.</span><span class="sxs-lookup"><span data-stu-id="de8ca-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="de8ca-198">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="de8ca-199">Questo è l'unico modello che contiene categorie etichettate.</span><span class="sxs-lookup"><span data-stu-id="de8ca-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="de8ca-200">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="de8ca-202">Definisce la piccola immagine a contrasto elevato da visualizzare per un controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="de8ca-203">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="de8ca-204">Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="de8ca-206">Definisce l'immagine piccola da visualizzare per un controllo .</span><span class="sxs-lookup"><span data-stu-id="de8ca-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="de8ca-207">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="de8ca-208">Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="de8ca-210">Definisce una matrice di <a href="/windows/win32/gdi/colorref">valori COLORREF</a> per i campioni di un Drop-Down Selezione colori.</span><span class="sxs-lookup"><span data-stu-id="de8ca-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="de8ca-211">Ogni Drop-Down Selezione colori <em>ColorTemplate contiene</em> una <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de8ca-212">Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> dell'oggetto <em>StandardColorGridRows</em> x <em>Columns</em> iniziale della matrice.</span><span class="sxs-lookup"><span data-stu-id="de8ca-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="de8ca-213">Se la matrice definisce un numero di colori inferiore al numero di campioni dichiarati nel markup, vengono visualizzati spazi vuoti <code>StandardColors</code> per i chip mancanti.</span><span class="sxs-lookup"><span data-stu-id="de8ca-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="de8ca-214">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-216">Definisce l'etichetta per la <strong>categoria Colori</strong> standard.</span><span class="sxs-lookup"><span data-stu-id="de8ca-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="de8ca-217">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="de8ca-218">Questo è l'unico modello che contiene categorie etichettate.</span><span class="sxs-lookup"><span data-stu-id="de8ca-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="de8ca-219">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="de8ca-221">Definisce una matrice di stringhe di descrizioni comando del controllo colore per la <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="de8ca-222">Ogni Drop-Down Selezione colori <em>ColorTemplate contiene</em> una <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de8ca-223">Vengono usate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati <code>StandardColors</code> nella griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="de8ca-224">Se vengono fornite meno etichette rispetto al numero di campioni nella griglia, viene fornito un valore predefinito per i campioni di <code>StandardColors</code> resto.</span><span class="sxs-lookup"><span data-stu-id="de8ca-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="de8ca-225">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="de8ca-227">Definisce una matrice di <a href="/windows/win32/gdi/colorref">valori COLORREF</a> per i campioni di un Drop-Down Selezione colori.</span><span class="sxs-lookup"><span data-stu-id="de8ca-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="de8ca-228">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de8ca-229">Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> <em>dell'oggetto ThemeColorGridRows</em> x <em>Columns</em> iniziale della matrice.</span><span class="sxs-lookup"><span data-stu-id="de8ca-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="de8ca-230">Se la matrice definisce un numero di colori inferiore al numero di campioni dichiarati nel markup, vengono visualizzati spazi vuoti <code>ThemeColors</code> per i chip mancanti.</span><span class="sxs-lookup"><span data-stu-id="de8ca-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="de8ca-231">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="de8ca-233">Definisce la matrice di stringhe di descrizioni comando del controllo colore per la <code>ThemeColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="de8ca-234">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de8ca-235">Vengono usate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati <code>ThemeColors</code> nella griglia.</span><span class="sxs-lookup"><span data-stu-id="de8ca-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="de8ca-236">Se vengono fornite meno etichette rispetto al numero di campioni nella griglia, viene fornito un valore predefinito per i campioni di <code>ThemeColors</code> resto.</span><span class="sxs-lookup"><span data-stu-id="de8ca-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="de8ca-237">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="de8ca-239">Definisce l'etichetta per la <strong>categoria Colori</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="de8ca-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="de8ca-240">Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="de8ca-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="de8ca-241">Questo è l'unico modello che contiene categorie etichettate.</span><span class="sxs-lookup"><span data-stu-id="de8ca-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="de8ca-242">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de8ca-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="de8ca-244">Definisce la stringa di caratteri per una descrizione comando associata a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="de8ca-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="de8ca-245">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de8ca-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="de8ca-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="de8ca-247">Definisce la stringa di caratteri per una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="de8ca-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="de8ca-248">Può essere aggiornato solo tramite invalidamento.</span><span class="sxs-lookup"><span data-stu-id="de8ca-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="de8ca-249">Gestori di comandi</span><span class="sxs-lookup"><span data-stu-id="de8ca-249">Command handlers</span></span>

<span data-ttu-id="de8ca-250">Il [**metodo IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) viene usato per personalizzare un Drop-Down Selezione colori tramite le chiavi di proprietà elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="de8ca-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="de8ca-251">L'esempio seguente illustra come impostare i campioni di colore di un Drop-Down Selezione colori, in base a una preferenza di stile personalizzata o a una griglia di controllo personalizzata dichiarata nel markup.</span><span class="sxs-lookup"><span data-stu-id="de8ca-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="de8ca-252">L'esempio seguente illustra un'implementazione del metodo [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) che espone i colori Drop-Down Selezione colori campione all'applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="de8ca-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="de8ca-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de8ca-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de8ca-254">Libreria di controlli del framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="de8ca-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="de8ca-255">**Elemento di markup DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="de8ca-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="de8ca-256">Selezione colori proprietà</span><span class="sxs-lookup"><span data-stu-id="de8ca-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="de8ca-257">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="de8ca-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="de8ca-258">Esempio di DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="de8ca-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

