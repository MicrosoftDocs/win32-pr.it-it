---
title: QuickAccessToolbar - elemento
description: Rappresenta la barra di accesso rapido, una piccola barra degli strumenti che visualizza i collegamenti ai comandi della barra multifunzione.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Elemento QuickAccessToolbar Barra multifunzione di Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443302"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="a284e-104">QuickAccessToolbar - elemento</span><span class="sxs-lookup"><span data-stu-id="a284e-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="a284e-105">Rappresenta la [barra di accesso rapido,](windowsribbon-controls-quickaccesstoolbar.md)una piccola barra degli strumenti che visualizza i collegamenti ai comandi della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a284e-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="a284e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a284e-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="a284e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a284e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a284e-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="a284e-108">Attribute</span></span></th>
<th><span data-ttu-id="a284e-109">Type</span><span class="sxs-lookup"><span data-stu-id="a284e-109">Type</span></span></th>
<th><span data-ttu-id="a284e-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a284e-110">Required</span></span></th>
<th><span data-ttu-id="a284e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a284e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a284e-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a284e-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a284e-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="a284e-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a284e-114">No</span><span class="sxs-lookup"><span data-stu-id="a284e-114">No</span></span><br/></td>
<td><span data-ttu-id="a284e-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="a284e-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a284e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="a284e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a284e-117">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="a284e-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a284e-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a284e-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a284e-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a284e-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a284e-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a284e-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a284e-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="a284e-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a284e-122">No</span><span class="sxs-lookup"><span data-stu-id="a284e-122">No</span></span><br/></td>
<td><span data-ttu-id="a284e-123">Inserisce un'ulteriore voce Command nel menu QAT.</span><span class="sxs-lookup"><span data-stu-id="a284e-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="a284e-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="a284e-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="a284e-125">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="a284e-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a284e-126">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a284e-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a284e-127">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a284e-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a284e-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a284e-128">Child elements</span></span>



| <span data-ttu-id="a284e-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="a284e-129">Element</span></span>                                                                                                                   | <span data-ttu-id="a284e-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a284e-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a284e-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="a284e-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="a284e-132">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="a284e-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a284e-133">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a284e-133">Parent elements</span></span>



| <span data-ttu-id="a284e-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="a284e-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a284e-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="a284e-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a284e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="a284e-136">Remarks</span></span>

<span data-ttu-id="a284e-137">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a284e-137">Required.</span></span>

<span data-ttu-id="a284e-138">Deve verificarsi esattamente una volta per [**ogni ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="a284e-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="a284e-139">Gli elementi nella QAT possono essere aggiunti o rimossi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a284e-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="a284e-140">Per coerenza tra le applicazioni della barra multifunzione, è consigliabile che il gestore del comando *CustomizeCommandName* avvii una finestra di dialogo di personalizzazione QAT.</span><span class="sxs-lookup"><span data-stu-id="a284e-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="a284e-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="a284e-141">Examples</span></span>

<span data-ttu-id="a284e-142">L'esempio seguente illustra il markup di base per **QuickAccessToolbar**.</span><span class="sxs-lookup"><span data-stu-id="a284e-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="a284e-143">Questa sezione di codice illustra la **dichiarazione del comando QuickAccessToolbar.**</span><span class="sxs-lookup"><span data-stu-id="a284e-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="a284e-144">Questa sezione di codice illustra la **dichiarazione del controllo QuickAccessToolbar.**</span><span class="sxs-lookup"><span data-stu-id="a284e-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a284e-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a284e-145">Element information</span></span>

* <span data-ttu-id="a284e-146">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="a284e-146">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="a284e-147">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="a284e-147">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="a284e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a284e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a284e-149">Controllo Barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="a284e-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





