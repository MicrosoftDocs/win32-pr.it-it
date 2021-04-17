---
title: Elemento QuickAccessToolbar
description: Rappresenta la barra di accesso rapido (QAT), una piccola barra degli strumenti che Visualizza i collegamenti ai comandi della barra multifunzione.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Barra multifunzione Windows elemento QuickAccessToolbar
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398508"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="a476c-104">Elemento QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="a476c-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="a476c-105">Rappresenta la [barra di accesso rapido (QAT)](windowsribbon-controls-quickaccesstoolbar.md), una piccola barra degli strumenti che Visualizza i collegamenti ai comandi della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a476c-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="a476c-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a476c-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="a476c-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a476c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a476c-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="a476c-108">Attribute</span></span></th>
<th><span data-ttu-id="a476c-109">Type</span><span class="sxs-lookup"><span data-stu-id="a476c-109">Type</span></span></th>
<th><span data-ttu-id="a476c-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a476c-110">Required</span></span></th>
<th><span data-ttu-id="a476c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a476c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a476c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a476c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a476c-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="a476c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a476c-114">No</span><span class="sxs-lookup"><span data-stu-id="a476c-114">No</span></span><br/></td>
<td><span data-ttu-id="a476c-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a476c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a476c-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="a476c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a476c-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="a476c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a476c-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a476c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a476c-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a476c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a476c-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a476c-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a476c-121">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="a476c-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a476c-122">No</span><span class="sxs-lookup"><span data-stu-id="a476c-122">No</span></span><br/></td>
<td><span data-ttu-id="a476c-123">Inserisce un elemento del comando aggiuntivo nel menu QAT.</span><span class="sxs-lookup"><span data-stu-id="a476c-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="a476c-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="a476c-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="a476c-125">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="a476c-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a476c-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a476c-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a476c-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a476c-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a476c-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a476c-128">Child elements</span></span>



| <span data-ttu-id="a476c-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="a476c-129">Element</span></span>                                                                                                                   | <span data-ttu-id="a476c-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a476c-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a476c-131">**QuickAccessToolbar. ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="a476c-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="a476c-132">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a476c-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a476c-133">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a476c-133">Parent elements</span></span>



| <span data-ttu-id="a476c-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="a476c-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a476c-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="a476c-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a476c-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="a476c-136">Remarks</span></span>

<span data-ttu-id="a476c-137">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a476c-137">Required.</span></span>

<span data-ttu-id="a476c-138">Deve essere eseguita esattamente una volta per ogni [**Ribbon. QuickAccessToolBar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="a476c-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="a476c-139">Gli elementi in QAT possono essere aggiunti o rimossi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a476c-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="a476c-140">Per coerenza tra le applicazioni della barra multifunzione, è consigliabile che il gestore di comandi *CustomizeCommandName* avvii una finestra di dialogo di personalizzazione di qat.</span><span class="sxs-lookup"><span data-stu-id="a476c-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="a476c-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="a476c-141">Examples</span></span>

<span data-ttu-id="a476c-142">Nell'esempio seguente viene illustrato il markup di base per **QuickAccessToolBar**.</span><span class="sxs-lookup"><span data-stu-id="a476c-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="a476c-143">Questa sezione di codice mostra la dichiarazione del comando **QuickAccessToolBar** .</span><span class="sxs-lookup"><span data-stu-id="a476c-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="a476c-144">Questa sezione di codice mostra la dichiarazione del controllo **QuickAccessToolBar** .</span><span class="sxs-lookup"><span data-stu-id="a476c-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a476c-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a476c-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a476c-146">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a476c-146">Minimum supported system</span></span><br/> | <span data-ttu-id="a476c-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a476c-147">Windows 7</span></span> |
| <span data-ttu-id="a476c-148">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="a476c-148">Can be empty</span></span>                        | <span data-ttu-id="a476c-149">No</span><span class="sxs-lookup"><span data-stu-id="a476c-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="a476c-150">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a476c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a476c-151">Controllo della barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="a476c-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





