---
title: Elemento spinner
description: Rappresenta un controllo Spinner.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Barra multifunzione di Windows per l'elemento spinner
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444812"
---
# <a name="spinner-element"></a><span data-ttu-id="cd75c-104">Elemento spinner</span><span class="sxs-lookup"><span data-stu-id="cd75c-104">Spinner element</span></span>

<span data-ttu-id="cd75c-105">Rappresenta un [controllo Spinner.](windowsribbon-controls-spinner.md)</span><span class="sxs-lookup"><span data-stu-id="cd75c-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="cd75c-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cd75c-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="cd75c-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="cd75c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd75c-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="cd75c-108">Attribute</span></span></th>
<th><span data-ttu-id="cd75c-109">Type</span><span class="sxs-lookup"><span data-stu-id="cd75c-109">Type</span></span></th>
<th><span data-ttu-id="cd75c-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="cd75c-110">Required</span></span></th>
<th><span data-ttu-id="cd75c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd75c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd75c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="cd75c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="cd75c-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="cd75c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="cd75c-114">No</span><span class="sxs-lookup"><span data-stu-id="cd75c-114">No</span></span><br/></td>
<td><span data-ttu-id="cd75c-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cd75c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="cd75c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="cd75c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="cd75c-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="cd75c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="cd75c-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="cd75c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="cd75c-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="cd75c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="cd75c-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cd75c-120">Child elements</span></span>

<span data-ttu-id="cd75c-121">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="cd75c-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cd75c-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="cd75c-122">Parent elements</span></span>



| <span data-ttu-id="cd75c-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="cd75c-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="cd75c-124">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="cd75c-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="cd75c-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="cd75c-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="cd75c-126">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="cd75c-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="cd75c-127">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="cd75c-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="cd75c-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="cd75c-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cd75c-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd75c-129">Remarks</span></span>

<span data-ttu-id="cd75c-130">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="cd75c-130">Optional.</span></span>

<span data-ttu-id="cd75c-131">Può verificarsi una o più volte per ogni [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="cd75c-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="cd75c-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="cd75c-132">Examples</span></span>

<span data-ttu-id="cd75c-133">Nell'esempio seguente viene illustrato il markup di base per [spinner](windowsribbon-controls-spinner.md).</span><span class="sxs-lookup"><span data-stu-id="cd75c-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="cd75c-134">Questa sezione di codice illustra le dichiarazioni del comando **Spinner,** con un [**elemento Group**](windowsribbon-element-group.md) che funziona come contenitore padre per l'elemento **Spinner.**</span><span class="sxs-lookup"><span data-stu-id="cd75c-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="cd75c-135">Questa sezione di codice illustra le **dichiarazioni del controllo Spinner.**</span><span class="sxs-lookup"><span data-stu-id="cd75c-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="cd75c-136">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cd75c-136">Element information</span></span>

- <span data-ttu-id="cd75c-137">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd75c-137">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="cd75c-138">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="cd75c-138">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="cd75c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd75c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd75c-140">Controllo spinner</span><span class="sxs-lookup"><span data-stu-id="cd75c-140">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





