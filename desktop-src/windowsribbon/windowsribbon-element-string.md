---
title: Elemento String
description: Rappresenta una risorsa stringa.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Elemento String Della barra multifunzione di Windows
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443902"
---
# <a name="string-element"></a><span data-ttu-id="43e12-104">Elemento String</span><span class="sxs-lookup"><span data-stu-id="43e12-104">String element</span></span>

<span data-ttu-id="43e12-105">Rappresenta una risorsa stringa.</span><span class="sxs-lookup"><span data-stu-id="43e12-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="43e12-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="43e12-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="43e12-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="43e12-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43e12-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="43e12-108">Attribute</span></span></th>
<th><span data-ttu-id="43e12-109">Type</span><span class="sxs-lookup"><span data-stu-id="43e12-109">Type</span></span></th>
<th><span data-ttu-id="43e12-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="43e12-110">Required</span></span></th>
<th><span data-ttu-id="43e12-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e12-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43e12-112"><strong>Contenuto</strong></span><span class="sxs-lookup"><span data-stu-id="43e12-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="43e12-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="43e12-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="43e12-114">No</span><span class="sxs-lookup"><span data-stu-id="43e12-114">No</span></span><br/></td>
<td><span data-ttu-id="43e12-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="43e12-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="43e12-116">Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.</span><span class="sxs-lookup"><span data-stu-id="43e12-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43e12-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="43e12-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="43e12-118">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="43e12-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="43e12-119">No</span><span class="sxs-lookup"><span data-stu-id="43e12-119">No</span></span><br/></td>
<td><span data-ttu-id="43e12-120">ID risorsa univoco.</span><span class="sxs-lookup"><span data-stu-id="43e12-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="43e12-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="43e12-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="43e12-122">Valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="43e12-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="43e12-123">La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="43e12-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43e12-124"><strong>Simbolo</strong></span><span class="sxs-lookup"><span data-stu-id="43e12-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="43e12-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="43e12-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="43e12-126">No</span><span class="sxs-lookup"><span data-stu-id="43e12-126">No</span></span><br/></td>
<td><span data-ttu-id="43e12-127">Simbolo della risorsa per la stringa.</span><span class="sxs-lookup"><span data-stu-id="43e12-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="43e12-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="43e12-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="43e12-129">Lettera o carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="43e12-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="43e12-130">La lunghezza massima consentita è 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="43e12-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="43e12-131">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="43e12-131">Child elements</span></span>



| <span data-ttu-id="43e12-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="43e12-132">Element</span></span>                                                                   | <span data-ttu-id="43e12-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e12-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="43e12-134">**String.Content**</span><span class="sxs-lookup"><span data-stu-id="43e12-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="43e12-135">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="43e12-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="43e12-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="43e12-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="43e12-137">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="43e12-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="43e12-138">**String.Symbol**</span><span class="sxs-lookup"><span data-stu-id="43e12-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="43e12-139">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="43e12-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="43e12-140">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="43e12-140">Parent elements</span></span>



| <span data-ttu-id="43e12-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="43e12-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43e12-142">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="43e12-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="43e12-143">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="43e12-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="43e12-144">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="43e12-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="43e12-145">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="43e12-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="43e12-146">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="43e12-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="43e12-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="43e12-147">Remarks</span></span>

<span data-ttu-id="43e12-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="43e12-148">Optional.</span></span>

<span data-ttu-id="43e12-149">Può verificarsi al massimo una volta per ogni elemento [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command.TooltipDescription.**](windowsribbon-element-command-tooltipdescription.md)</span><span class="sxs-lookup"><span data-stu-id="43e12-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="43e12-150">La definizione di stringa viene aggiunta al file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="43e12-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="43e12-151">La stringa viene aggiunta a una tabella di stringhe nel file di risorse della barra multifunzione in cui un nome e un ID vengono generati dal framework della barra multifunzione se non ne viene dichiarato nessuno.</span><span class="sxs-lookup"><span data-stu-id="43e12-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="43e12-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="43e12-152">Examples</span></span>

<span data-ttu-id="43e12-153">L'esempio seguente illustra il markup per [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **dichiarazione String.**</span><span class="sxs-lookup"><span data-stu-id="43e12-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="43e12-154">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="43e12-154">Element information</span></span>

- <span data-ttu-id="43e12-155">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="43e12-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="43e12-156">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="43e12-156">**Can be empty**: No</span></span>



 

 





