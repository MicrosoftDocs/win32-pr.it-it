---
title: Personalizzazione dei colori della barra multifunzione
description: Il Framework della barra multifunzione di Windows espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Barra multifunzione di Windows, personalizzazione dei colori
- Barra multifunzione, personalizzazione dei colori
- personalizzazione dei colori della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723822"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="984f3-106">Personalizzazione dei colori della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="984f3-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="984f3-107">Il Framework della barra multifunzione di Windows espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di vari elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="984f3-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="984f3-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="984f3-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="984f3-109">Specificare i colori della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="984f3-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="984f3-110">Converti RGB in HSB</span><span class="sxs-lookup"><span data-stu-id="984f3-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="984f3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="984f3-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="984f3-112">Introduzione</span><span class="sxs-lookup"><span data-stu-id="984f3-112">Introduction</span></span>

<span data-ttu-id="984f3-113">Le [chiavi di proprietà del Framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare il colore di diversi elementi dell'interfaccia utente in un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="984f3-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="984f3-114">Queste proprietà consentono al framework della barra multifunzione di supportare la personalizzazione, i requisiti di identità e le specifiche di personalizzazione tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="984f3-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="984f3-115">Colore della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="984f3-115">Ribbon Color</span></span>                     | <span data-ttu-id="984f3-116">Chiave di proprietà del Framework</span><span class="sxs-lookup"><span data-stu-id="984f3-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984f3-117">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="984f3-117">Background color</span></span>                 | [<span data-ttu-id="984f3-118">Interfaccia utente \_ pkey \_ GlobalBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="984f3-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="984f3-119">Colore di evidenziazione (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="984f3-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="984f3-120">[Interfaccia utente \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \* \* \* introdotta in Windows 8 \* \*: \* \* [UI \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) non può essere impostata in modo indipendente dall' [interfaccia utente \_ \_ ](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)pkey GlobalBackgroundColor.</span><span class="sxs-lookup"><span data-stu-id="984f3-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="984f3-121">Colore del testo</span><span class="sxs-lookup"><span data-stu-id="984f3-121">Text color</span></span>                       | <span data-ttu-id="984f3-122">[Interfaccia utente \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* introdotta in Windows 8 **:** le modifiche apportate al valore predefinito di [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 potrebbero richiedere una modifica all' [interfaccia utente pkey \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) nelle app della barra multifunzione progettate per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="984f3-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="984f3-123">Specificare i colori della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="984f3-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="984f3-124">Il Framework della barra multifunzione usa un modello di colore HSB (Hue, Saturation, Brightness), che differisce dagli spazi colori più comuni di Hue, Saturation, luminosità (HSL) o Hue, Saturation, value (HSV).</span><span class="sxs-lookup"><span data-stu-id="984f3-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="984f3-125">In particolare, B rappresenta un livello di luminosità o luminosità generale invece della luminosità di un colore specifico.</span><span class="sxs-lookup"><span data-stu-id="984f3-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="984f3-126">Per specificare il colore degli elementi dell'interfaccia utente nel framework della barra multifunzione, un'applicazione assegna i valori HSB a ognuna delle proprietà dei colori globali.</span><span class="sxs-lookup"><span data-stu-id="984f3-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="984f3-127">Questi valori vengono quindi applicati in modo universale a tutti gli elementi della barra multifunzione come richiesto dall'applicazione Ribbon (il Framework non supporta l'assegnazione di valori HSB a singoli elementi e controlli).</span><span class="sxs-lookup"><span data-stu-id="984f3-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="984f3-128">Introdotta in Windows 8 \* \*: \* \*[UI \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) viene assegnato lo stesso valore di [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="984f3-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="984f3-129">Nella tabella seguente vengono descritti i parametri HSB del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="984f3-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="984f3-130">Componente</span><span class="sxs-lookup"><span data-stu-id="984f3-130">Component</span></span>

<span data-ttu-id="984f3-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984f3-131">Description</span></span>

<span data-ttu-id="984f3-132">Valori regolati\*</span><span class="sxs-lookup"><span data-stu-id="984f3-132">Adjusted Values\*</span></span>

<span data-ttu-id="984f3-133">Tonalità (H)</span><span class="sxs-lookup"><span data-stu-id="984f3-133">Hue (H)</span></span>

<span data-ttu-id="984f3-134">Il colore del pigmento, o effettivo, viene in genere identificato come valore da un intervallo di Circlular compreso tra 0 e 359 gradi.</span><span class="sxs-lookup"><span data-stu-id="984f3-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="984f3-135">da 0 (rosso) a 255 (rosso)</span><span class="sxs-lookup"><span data-stu-id="984f3-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="984f3-136">Saturazione/i</span><span class="sxs-lookup"><span data-stu-id="984f3-136">Saturation (S)</span></span>

<span data-ttu-id="984f3-137">La purezza, o saturazione, del colore misurato come percentuale da 0 a 100%.</span><span class="sxs-lookup"><span data-stu-id="984f3-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="984f3-138">0 (grigio) a 255 (completamente saturo)</span><span class="sxs-lookup"><span data-stu-id="984f3-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="984f3-139">Luminosità (B)</span><span class="sxs-lookup"><span data-stu-id="984f3-139">Brightness (B)</span></span>

<span data-ttu-id="984f3-140">La luminosità complessiva o l'oscurità del colore misurato come percentuale da 0 a 100%.</span><span class="sxs-lookup"><span data-stu-id="984f3-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="984f3-141">da 0 (scuro) a 255 (chiaro)</span><span class="sxs-lookup"><span data-stu-id="984f3-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="984f3-142">\* L'intervallo originale per ogni valore di parametro viene convertito in un intervallo compreso tra 0 e 255 per il Framework.</span><span class="sxs-lookup"><span data-stu-id="984f3-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="984f3-143">I valori HSB non identificano colori specifici.</span><span class="sxs-lookup"><span data-stu-id="984f3-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="984f3-144">Al contrario, la combinazione di valori di proprietà HSB influenza il modo in cui le sfumature di colore nell'intera interfaccia utente vengono regolate in relazione.</span><span class="sxs-lookup"><span data-stu-id="984f3-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="984f3-145">Quando si assegnano valori HSB personalizzati all' [interfaccia utente \_ pkey \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) e [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), è consigliabile che questi valori siano di un contrasto sufficientemente elevato per garantire la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="984f3-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="984f3-146">In particolare, il colore del testo deve essere più scuro della sfumatura più chiara dell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="984f3-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="984f3-147">Se necessario, il framework regola automaticamente il \_ valore HSB pkey GlobalTextColor dell'interfaccia utente \_ per fornire un contrasto sufficiente rispetto a qualsiasi sfumatura o sfumatura di sfondo derivata dall'interfaccia utente \_ pkey \_ GlobalBackgroundColor.</span><span class="sxs-lookup"><span data-stu-id="984f3-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="984f3-148">In Windows 7, l' [interfaccia utente \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) può essere impostata indipendentemente dall' [interfaccia utente \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="984f3-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="984f3-149">Nell'esempio seguente viene illustrato come specificare un colore personalizzato per l' [interfaccia utente \_ pkey \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)e l' [interfaccia utente \_ pkey \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) proprietà.</span><span class="sxs-lookup"><span data-stu-id="984f3-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="984f3-150">Converti RGB in HSB</span><span class="sxs-lookup"><span data-stu-id="984f3-150">Convert RGB to HSB</span></span>

<span data-ttu-id="984f3-151">In questa sezione viene descritta la formula necessaria per la corrispondenza dinamica di un valore HSB del Framework della barra multifunzione, l' [interfaccia utente \_ pkey \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in questo esempio a un colore RGB specifico in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="984f3-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="984f3-152">Lo sfondo della riga di tabulazione viene usato come punto di riferimento perché viene sottoposto a rendering come superficie di colore Flat rispetto alla sfumatura di luminosità dello sfondo della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="984f3-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="984f3-153">È necessaria una conversione preliminare per ottenere un valore HSL intermedio.</span><span class="sxs-lookup"><span data-stu-id="984f3-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="984f3-154">Questo valore HSL può quindi essere convertito in un valore HSB.</span><span class="sxs-lookup"><span data-stu-id="984f3-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="984f3-155">La conversione da RGB a HSL viene eseguita facilmente con la maggior parte del software per la modifica di foto.</span><span class="sxs-lookup"><span data-stu-id="984f3-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="984f3-156">La conversione di HSL (con ogni componente nell'intervallo compreso tra 0,0 e 1,0) in un'impostazione HSB della barra multifunzione viene eseguita tramite le formule seguenti:</span><span class="sxs-lookup"><span data-stu-id="984f3-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="984f3-157"><sub>Sfondo</sub> H = Round (255.0 h)</span><span class="sxs-lookup"><span data-stu-id="984f3-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="984f3-158"><sub>Background</sub> S = Round (255.0 s)</span><span class="sxs-lookup"><span data-stu-id="984f3-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="984f3-159">B<sub>background</sub> = Round (257.7 + 149,9 ln (L)) se 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="984f3-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="984f3-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="984f3-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="984f3-161">Linee guida sui colori</span><span class="sxs-lookup"><span data-stu-id="984f3-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="984f3-162">Proprietà del Framework</span><span class="sxs-lookup"><span data-stu-id="984f3-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





