---
title: Elemento Tab
description: Rappresenta una scheda principale o contestuale.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Elemento Scheda Barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443882"
---
# <a name="tab-element"></a><span data-ttu-id="2ff48-104">Elemento Tab</span><span class="sxs-lookup"><span data-stu-id="2ff48-104">Tab element</span></span>

<span data-ttu-id="2ff48-105">Rappresenta una scheda [principale](windowsribbon-controls-tab.md) o [contestuale.](windowsribbon-controls-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="2ff48-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="2ff48-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2ff48-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="2ff48-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="2ff48-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ff48-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="2ff48-108">Attribute</span></span></th>
<th><span data-ttu-id="2ff48-109">Type</span><span class="sxs-lookup"><span data-stu-id="2ff48-109">Type</span></span></th>
<th><span data-ttu-id="2ff48-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="2ff48-110">Required</span></span></th>
<th><span data-ttu-id="2ff48-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ff48-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ff48-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="2ff48-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="2ff48-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="2ff48-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="2ff48-114">No</span><span class="sxs-lookup"><span data-stu-id="2ff48-114">No</span></span><br/></td>
<td><span data-ttu-id="2ff48-115">Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="2ff48-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="2ff48-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="2ff48-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2ff48-117">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="2ff48-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="2ff48-118">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="2ff48-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="2ff48-119">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2ff48-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ff48-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2ff48-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2ff48-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="2ff48-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2ff48-122">No</span><span class="sxs-lookup"><span data-stu-id="2ff48-122">No</span></span><br/></td>
<td><span data-ttu-id="2ff48-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="2ff48-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2ff48-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="2ff48-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2ff48-125">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="2ff48-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2ff48-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2ff48-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2ff48-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2ff48-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2ff48-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2ff48-128">Child elements</span></span>



| <span data-ttu-id="2ff48-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ff48-129">Element</span></span>                                                                         | <span data-ttu-id="2ff48-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ff48-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2ff48-131">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="2ff48-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="2ff48-132">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="2ff48-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2ff48-133">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="2ff48-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="2ff48-134">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="2ff48-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="2ff48-135">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2ff48-135">Parent elements</span></span>



| <span data-ttu-id="2ff48-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ff48-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="2ff48-137">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="2ff48-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="2ff48-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="2ff48-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="2ff48-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ff48-139">Remarks</span></span>

<span data-ttu-id="2ff48-140">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ff48-140">Required.</span></span>

<span data-ttu-id="2ff48-141">Deve verificarsi almeno una volta per [**ogni elemento Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) [**o TabGroup.**](windowsribbon-element-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="2ff48-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="2ff48-142">**Tab** supporta le [modalità dell'applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="2ff48-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="2ff48-143">Se [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) è presente per l'elemento **Tab,** è necessaria una voce per ogni elemento [**Group**](windowsribbon-element-group.md) e le relative dimensioni ideali in **ScalingPolicy.IdealSizes.**</span><span class="sxs-lookup"><span data-stu-id="2ff48-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="2ff48-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="2ff48-144">Examples</span></span>

<span data-ttu-id="2ff48-145">L'esempio seguente illustra il markup di base per **l'elemento Tab.**</span><span class="sxs-lookup"><span data-stu-id="2ff48-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="2ff48-146">Questa sezione di codice illustra le **dichiarazioni di comando** tab per una **scheda** Home.</span><span class="sxs-lookup"><span data-stu-id="2ff48-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="2ff48-147">Questa sezione di codice illustra le **dichiarazioni del** controllo Tab.</span><span class="sxs-lookup"><span data-stu-id="2ff48-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="2ff48-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2ff48-148">Element information</span></span>

- <span data-ttu-id="2ff48-149">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ff48-149">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="2ff48-150">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="2ff48-150">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="2ff48-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ff48-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff48-152">Controllo Tab</span><span class="sxs-lookup"><span data-stu-id="2ff48-152">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="2ff48-153">Controllo Gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="2ff48-153">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="2ff48-154">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="2ff48-154">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

