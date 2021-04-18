---
title: Elemento HelpButton
description: Rappresenta il controllo pulsante della guida.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Barra multifunzione Windows elemento HelpButton
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299361"
---
# <a name="helpbutton-element"></a><span data-ttu-id="f3ddb-104">Elemento HelpButton</span><span class="sxs-lookup"><span data-stu-id="f3ddb-104">HelpButton element</span></span>

<span data-ttu-id="f3ddb-105">Rappresenta il controllo [pulsante della Guida](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ddb-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="f3ddb-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f3ddb-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="f3ddb-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="f3ddb-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3ddb-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="f3ddb-108">Attribute</span></span></th>
<th><span data-ttu-id="f3ddb-109">Type</span><span class="sxs-lookup"><span data-stu-id="f3ddb-109">Type</span></span></th>
<th><span data-ttu-id="f3ddb-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f3ddb-110">Required</span></span></th>
<th><span data-ttu-id="f3ddb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3ddb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3ddb-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f3ddb-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f3ddb-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="f3ddb-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f3ddb-114">No</span><span class="sxs-lookup"><span data-stu-id="f3ddb-114">No</span></span><br/></td>
<td><span data-ttu-id="f3ddb-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f3ddb-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="f3ddb-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f3ddb-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f3ddb-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f3ddb-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f3ddb-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f3ddb-120">Child elements</span></span>

<span data-ttu-id="f3ddb-121">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f3ddb-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f3ddb-122">Parent elements</span></span>



| <span data-ttu-id="f3ddb-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3ddb-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f3ddb-124">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="f3ddb-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f3ddb-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3ddb-125">Remarks</span></span>

<span data-ttu-id="f3ddb-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-126">Optional.</span></span>

<span data-ttu-id="f3ddb-127">Può essere presente al massimo una volta per ogni [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="f3ddb-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="f3ddb-128">Viene avviata una finestra di dialogo della Guida dell'applicazione quando si fa clic su.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="f3ddb-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="f3ddb-129">Examples</span></span>

<span data-ttu-id="f3ddb-130">Nell'esempio seguente viene illustrato il markup di base necessario per implementare un controllo [pulsante della Guida](windowsribbon-controls-helpbutton.md) della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f3ddb-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="f3ddb-131">Questa sezione di codice mostra la dichiarazione del comando **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="f3ddb-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="f3ddb-132">Questa sezione di codice mostra la dichiarazione del controllo **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="f3ddb-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="f3ddb-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3ddb-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f3ddb-134">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3ddb-134">Minimum supported system</span></span><br/> | <span data-ttu-id="f3ddb-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3ddb-135">Windows 7</span></span> |
| <span data-ttu-id="f3ddb-136">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f3ddb-136">Can be empty</span></span>                        | <span data-ttu-id="f3ddb-137">Sì</span><span class="sxs-lookup"><span data-stu-id="f3ddb-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="f3ddb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3ddb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ddb-139">Controllo pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="f3ddb-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





