---
title: Elemento ToggleButton
description: Rappresenta il controllo di un interruttore.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Barra multifunzione Windows elemento ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104336145"
---
# <a name="togglebutton-element"></a><span data-ttu-id="2c023-104">Elemento ToggleButton</span><span class="sxs-lookup"><span data-stu-id="2c023-104">ToggleButton element</span></span>

<span data-ttu-id="2c023-105">Rappresenta il controllo di un [interruttore](windowsribbon-controls-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="2c023-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2c023-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2c023-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="2c023-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="2c023-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c023-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="2c023-108">Attribute</span></span></th>
<th><span data-ttu-id="2c023-109">Type</span><span class="sxs-lookup"><span data-stu-id="2c023-109">Type</span></span></th>
<th><span data-ttu-id="2c023-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="2c023-110">Required</span></span></th>
<th><span data-ttu-id="2c023-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c023-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c023-112"><strong>ApplicationDefaults. checkin</strong></span><span class="sxs-lookup"><span data-stu-id="2c023-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="2c023-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="2c023-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="2c023-114">No</span><span class="sxs-lookup"><span data-stu-id="2c023-114">No</span></span><br/></td>
<td><span data-ttu-id="2c023-115">Questo attributo è valido solo quando l'elemento <strong>ToggleButton</strong> è un elemento figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolBar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2c023-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="2c023-116">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c023-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2c023-117">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="2c023-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2c023-118">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c023-118">Default.</span></span> <br/> </dd> <span data-ttu-id="2c023-119"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="2c023-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c023-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2c023-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2c023-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="2c023-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2c023-122">No</span><span class="sxs-lookup"><span data-stu-id="2c023-122">No</span></span><br/></td>
<td><span data-ttu-id="2c023-123">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2c023-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2c023-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="2c023-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2c023-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="2c023-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2c023-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2c023-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2c023-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2c023-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2c023-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2c023-128">Child elements</span></span>

<span data-ttu-id="2c023-129">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="2c023-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2c023-130">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2c023-130">Parent elements</span></span>



| <span data-ttu-id="2c023-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c023-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c023-132">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="2c023-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="2c023-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="2c023-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="2c023-134">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2c023-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="2c023-135">**Group**</span><span class="sxs-lookup"><span data-stu-id="2c023-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="2c023-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="2c023-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="2c023-137">**QuickAccessToolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="2c023-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="2c023-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2c023-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="2c023-139">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="2c023-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="2c023-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2c023-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="2c023-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c023-141">Remarks</span></span>

<span data-ttu-id="2c023-142">Facoltativo o obbligatorio, a seconda dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="2c023-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="2c023-143">Può verificarsi al massimo una volta per ogni elemento [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2c023-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="2c023-144">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolBar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="2c023-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2c023-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c023-145">Examples</span></span>

<span data-ttu-id="2c023-146">Nell'esempio seguente viene illustrato il markup di base per l'elemento **ToggleButton** .</span><span class="sxs-lookup"><span data-stu-id="2c023-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="2c023-147">In questa sezione del codice viene illustrata una dichiarazione di elemento **ToggleButton** all'interno dell'elemento [**QuickAccessToolBar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .</span><span class="sxs-lookup"><span data-stu-id="2c023-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="2c023-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2c023-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2c023-149">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c023-149">Minimum supported system</span></span><br/> | <span data-ttu-id="2c023-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c023-150">Windows 7</span></span> |
| <span data-ttu-id="2c023-151">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="2c023-151">Can be empty</span></span>                        | <span data-ttu-id="2c023-152">Sì</span><span class="sxs-lookup"><span data-stu-id="2c023-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="2c023-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c023-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c023-154">Controllo interruttore</span><span class="sxs-lookup"><span data-stu-id="2c023-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





