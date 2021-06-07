---
title: Elemento HelpButton
description: Rappresenta il controllo Pulsante ? .
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Elemento HelpButton nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442842"
---
# <a name="helpbutton-element"></a><span data-ttu-id="d5069-104">Elemento HelpButton</span><span class="sxs-lookup"><span data-stu-id="d5069-104">HelpButton element</span></span>

<span data-ttu-id="d5069-105">Rappresenta il [controllo Pulsante ?](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="d5069-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="d5069-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d5069-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="d5069-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d5069-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5069-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="d5069-108">Attribute</span></span></th>
<th><span data-ttu-id="d5069-109">Type</span><span class="sxs-lookup"><span data-stu-id="d5069-109">Type</span></span></th>
<th><span data-ttu-id="d5069-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d5069-110">Required</span></span></th>
<th><span data-ttu-id="d5069-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5069-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5069-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d5069-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d5069-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="d5069-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d5069-114">No</span><span class="sxs-lookup"><span data-stu-id="d5069-114">No</span></span><br/></td>
<td><span data-ttu-id="d5069-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5069-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d5069-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="d5069-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d5069-117">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="d5069-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d5069-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5069-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d5069-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d5069-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d5069-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d5069-120">Child elements</span></span>

<span data-ttu-id="d5069-121">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="d5069-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d5069-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d5069-122">Parent elements</span></span>



| <span data-ttu-id="d5069-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="d5069-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d5069-124">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="d5069-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d5069-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5069-125">Remarks</span></span>

<span data-ttu-id="d5069-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d5069-126">Optional.</span></span>

<span data-ttu-id="d5069-127">Può verificarsi al massimo una volta per [**ogni ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="d5069-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="d5069-128">Avvia una finestra di dialogo della Guida dell'applicazione quando si fa clic su .</span><span class="sxs-lookup"><span data-stu-id="d5069-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="d5069-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="d5069-129">Examples</span></span>

<span data-ttu-id="d5069-130">L'esempio seguente illustra il markup di base necessario per implementare un controllo Pulsante [? della barra](windowsribbon-controls-helpbutton.md) multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d5069-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="d5069-131">Questa sezione di codice illustra la **dichiarazione del comando HelpButton.**</span><span class="sxs-lookup"><span data-stu-id="d5069-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="d5069-132">Questa sezione di codice mostra la dichiarazione **del controllo HelpButton.**</span><span class="sxs-lookup"><span data-stu-id="d5069-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="d5069-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d5069-133">Element information</span></span>

* <span data-ttu-id="d5069-134">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5069-134">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d5069-135">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="d5069-135">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="d5069-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5069-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5069-137">Controllo Pulsante ?</span><span class="sxs-lookup"><span data-stu-id="d5069-137">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





