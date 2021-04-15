---
title: Selezione colori Drop-Down
description: Il Framework della barra multifunzione di Windows fornisce un controllo di selezione colori Drop-Down specializzato che espone diverse impostazioni dei colori tramite un pulsante di suddivisione e un selettore di colori personalizzabile.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399825"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="7b1b6-103">Selezione colori Drop-Down</span><span class="sxs-lookup"><span data-stu-id="7b1b6-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="7b1b6-104">Il Framework della barra multifunzione di Windows fornisce un controllo di selezione colori Drop-Down specializzato che espone diverse impostazioni dei colori tramite un pulsante di suddivisione e un selettore di colori personalizzabile.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="7b1b6-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="7b1b6-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="7b1b6-106">markup</span><span class="sxs-lookup"><span data-stu-id="7b1b6-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="7b1b6-107">Codice</span><span class="sxs-lookup"><span data-stu-id="7b1b6-107">Code</span></span>](#code)
    -   [<span data-ttu-id="7b1b6-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b1b6-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="7b1b6-109">Gestori di comandi</span><span class="sxs-lookup"><span data-stu-id="7b1b6-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="7b1b6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b1b6-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="7b1b6-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="7b1b6-111">Introduction</span></span>

<span data-ttu-id="7b1b6-112">Emulando l'aspetto e la funzionalità della selezione colori Microsoft Office, il Framework della barra multifunzione è in grado di trarre vantaggio da e contribuire a coerenza e familiarità in un'ampia gamma di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="7b1b6-113">markup</span><span class="sxs-lookup"><span data-stu-id="7b1b6-113">Markup</span></span>

<span data-ttu-id="7b1b6-114">Come tutti i controlli della barra multifunzione, il Drop-Down selezione colori viene facilmente implementato e personalizzato tramite markup.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="7b1b6-115">Il Framework fornisce un numero di attributi degli elementi per la selezione colori Drop-Down per esporre diversi livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="7b1b6-116">Nella tabella seguente sono elencati gli attributi di selezione colori Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b1b6-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="7b1b6-117">Attribute</span></span></th>
<th><span data-ttu-id="7b1b6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b1b6-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b1b6-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="7b1b6-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="7b1b6-120">Modelli di layout che specificano il tipo di selezione colori Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="7b1b6-121">Sono disponibili tre modelli, ognuno dei quali specifica un layout di controllo e i valori predefiniti per gli attributi e le chiavi di proprietà associati.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="7b1b6-122">ChipSize</span></span></td>
<td><span data-ttu-id="7b1b6-123">Dimensioni di ogni chip di colore (o campione).</span><span class="sxs-lookup"><span data-stu-id="7b1b6-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="7b1b6-124">Columns</span></span></td>
<td><span data-ttu-id="7b1b6-125">Numero di colonne del chip di colore (o campione).</span><span class="sxs-lookup"><span data-stu-id="7b1b6-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="7b1b6-126">CommandName</span></span></td>
<td><span data-ttu-id="7b1b6-127">Nome della dichiarazione del comando associato.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="7b1b6-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="7b1b6-129">Consente di visualizzare o nascondere il pulsante <strong>automatico</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="7b1b6-130">Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="7b1b6-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="7b1b6-132">Consente di visualizzare o nascondere il pulsante <strong>nessun colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="7b1b6-133">Valido per tutti i valori <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="7b1b6-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="7b1b6-135">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori recenti</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="7b1b6-136">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="7b1b6-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="7b1b6-138">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="7b1b6-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="7b1b6-140">Numero di righe del chip di colore (o campione) nell'area dei <strong>colori del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="7b1b6-141">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7b1b6-142">Le schermate seguenti illustrano i layout di selezione colori predefiniti Drop-Down per i tre modelli di colore.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1b6-143">`ThemeColors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' ThemeColors '. ](images/markup/colortemplate.themedcolors.1.png) \[ NewLine\]</span><span class="sxs-lookup"><span data-stu-id="7b1b6-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="7b1b6-144">`standardcolors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' standardcolors '. ](images/markup/colortemplate.standardcolors.3.png) \[ NewLine\]</span><span class="sxs-lookup"><span data-stu-id="7b1b6-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="7b1b6-145">`highlightcolors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' highlightcolors '.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="7b1b6-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="7b1b6-146">Il markup di base necessario per ogni tipo di selezione dei colori Drop-Down è illustrato negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b1b6-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="7b1b6-147">La selezione colori Drop-Down è un controllo [Button](windowsribbon-controls-button.md) valido in un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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





## <a name="code"></a><span data-ttu-id="7b1b6-148">Codice</span><span class="sxs-lookup"><span data-stu-id="7b1b6-148">Code</span></span>

<span data-ttu-id="7b1b6-149">Come controllo specializzato che supporta la personalizzazione, qualsiasi implementazione della selezione colori Drop-Down che sfrutta tali funzionalità richiede un codice dell'applicazione specializzato per gestire le proprietà e gestire qualsiasi comando emesso dal controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="7b1b6-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b1b6-150">Properties</span></span>

<span data-ttu-id="7b1b6-151">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Drop-Down selezione colori.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="7b1b6-152">In genere, una proprietà della selezione colori Drop-Down viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="7b1b6-153">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="7b1b6-154">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="7b1b6-155">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="7b1b6-156">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="7b1b6-157">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Drop-Down selezione colori.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b1b6-158">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="7b1b6-158">Property Key</span></span></th>
<th><span data-ttu-id="7b1b6-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b1b6-159">Description</span></span></th>
<th><span data-ttu-id="7b1b6-160">Note</span><span class="sxs-lookup"><span data-stu-id="7b1b6-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b1b6-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-162">Definisce l'etichetta per il pulsante colore <strong>automatico</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="7b1b6-163">Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-164">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="7b1b6-166">Definisce il valore di colore selezionato come <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="7b1b6-167">Valido solo quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> ha un valore <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-168">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="7b1b6-170">Definisce il tipo di colore selezionato.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-171">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="7b1b6-173">Definisce la possibilità per un controllo di rispondere all'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-174">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="7b1b6-176">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="7b1b6-178">Definisce la stringa di caratteri per un'etichetta del controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-179">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="7b1b6-181">Definisce l'immagine a contrasto elevato grande da visualizzare per un controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-182">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="7b1b6-183">Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="7b1b6-185">Definisce l'immagine di grandi dimensioni da visualizzare per un controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-186">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="7b1b6-187">Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-189">Definisce l'etichetta per il pulsante <strong>altri colori...</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="7b1b6-190">Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-191">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-193">Definisce l'etichetta per il pulsante <strong>nessun colore</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="7b1b6-194">Valido per tutti i valori <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-195">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-197">Definisce l'etichetta per la categoria dei <strong>colori recenti</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="7b1b6-198">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="7b1b6-199">Si tratta dell'unico modello che contiene le categorie con etichetta.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-200">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="7b1b6-202">Definisce la piccola immagine a contrasto elevato da visualizzare per un controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-203">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="7b1b6-204">Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="7b1b6-206">Definisce l'immagine piccola da visualizzare per un controllo.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-207">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="7b1b6-208">Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="7b1b6-210">Definisce una matrice di valori <a href="/windows/win32/gdi/colorref">COLORREF</a> per i campioni di una selezione colori Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="7b1b6-211">Ogni <em>ColorTemplate</em> di selezione colori Drop-Down contiene una <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7b1b6-212">Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> delle <em>colonne</em> <em>StandardColorGridRows</em> x iniziali della matrice.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="7b1b6-213">Se la matrice definisce un numero inferiore di colori rispetto al numero di <code>StandardColors</code> campioni dichiarati nel markup, vengono visualizzati spazi vuoti per i chip mancanti.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7b1b6-214">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-216">Definisce l'etichetta per la categoria dei <strong>colori standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="7b1b6-217">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="7b1b6-218">Si tratta dell'unico modello che contiene le categorie con etichetta.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-219">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="7b1b6-221">Definisce una matrice di stringhe di descrizioni comandi dei campioni di colore per la <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="7b1b6-222">Ogni <em>ColorTemplate</em> di selezione colori Drop-Down contiene una <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7b1b6-223">Vengono utilizzate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati nella <code>StandardColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="7b1b6-224">Se viene fornito un minor numero di etichette rispetto al numero di campioni nella <code>StandardColors</code> griglia, viene fornito un valore predefinito per i campioni remainining.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7b1b6-225">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="7b1b6-227">Definisce una matrice di valori <a href="/windows/win32/gdi/colorref">COLORREF</a> per i campioni di una selezione colori Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="7b1b6-228">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7b1b6-229">Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> delle <em>colonne</em> <em>ThemeColorGridRows</em> x iniziali della matrice.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="7b1b6-230">Se la matrice definisce un numero inferiore di colori rispetto al numero di <code>ThemeColors</code> campioni dichiarati nel markup, vengono visualizzati spazi vuoti per i chip mancanti.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7b1b6-231">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="7b1b6-233">Definisce la matrice di stringhe di descrizioni comandi dei campioni di colore per la <code>ThemeColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="7b1b6-234">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7b1b6-235">Vengono utilizzate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati nella <code>ThemeColors</code> griglia.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="7b1b6-236">Se viene fornito un minor numero di etichette rispetto al numero di campioni nella <code>ThemeColors</code> griglia, viene fornito un valore predefinito per i campioni remainining.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="7b1b6-237">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="7b1b6-239">Definisce l'etichetta per la categoria dei <strong>colori del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="7b1b6-240">Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="7b1b6-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="7b1b6-241">Si tratta dell'unico modello che contiene le categorie con etichetta.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-242">Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b1b6-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="7b1b6-244">Definisce la stringa di caratteri per una descrizione della descrizione comando associata a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-245">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b1b6-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="7b1b6-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="7b1b6-247">Definisce la stringa di caratteri per una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="7b1b6-248">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="7b1b6-249">Gestori di comandi</span><span class="sxs-lookup"><span data-stu-id="7b1b6-249">Command handlers</span></span>

<span data-ttu-id="7b1b6-250">Il metodo [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) viene usato per personalizzare una selezione dei colori Drop-Down tramite le chiavi di proprietà elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="7b1b6-251">Nell'esempio seguente viene illustrato come impostare i campioni di colore di un selettore di colore Drop-Down, in base a una preferenza di stile personalizzata o a una griglia di campioni personalizzata dichiarata nel markup.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


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



<span data-ttu-id="7b1b6-252">Nell'esempio seguente viene illustrata un'implementazione del metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) che espone i colori del campione di selezione colori Drop-Down all'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="7b1b6-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7b1b6-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b1b6-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b1b6-254">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="7b1b6-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="7b1b6-255">**Elemento di markup DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="7b1b6-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="7b1b6-256">Proprietà selezione colori</span><span class="sxs-lookup"><span data-stu-id="7b1b6-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="7b1b6-257">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="7b1b6-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="7b1b6-258">Esempio DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="7b1b6-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

