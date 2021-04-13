---
title: Elemento Command
description: Rappresenta una definizione di comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Barra multifunzione Windows elemento di comando
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338814"
---
# <a name="command-element"></a><span data-ttu-id="d0d8a-104">Elemento Command</span><span class="sxs-lookup"><span data-stu-id="d0d8a-104">Command element</span></span>

<span data-ttu-id="d0d8a-105">Rappresenta una definizione di comando.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="d0d8a-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d0d8a-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="d0d8a-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d0d8a-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d8a-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="d0d8a-108">Attribute</span></span></th>
<th><span data-ttu-id="d0d8a-109">Type</span><span class="sxs-lookup"><span data-stu-id="d0d8a-109">Type</span></span></th>
<th><span data-ttu-id="d0d8a-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d0d8a-110">Required</span></span></th>
<th><span data-ttu-id="d0d8a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0d8a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0d8a-112"><strong>Commento</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-114">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-114">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-115">Utilizzato per annotare l'elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-117">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="d0d8a-118">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d8a-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-120">XS: positiveInteger Union XS: String</span><span class="sxs-lookup"><span data-stu-id="d0d8a-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-121">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-121">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-122">ID di risorsa univoco.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="d0d8a-123">
<dt><span></span><span></span><strong></strong> (Unione di XS: positiveInteger e xs: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-124">Valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="d0d8a-125">La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d8a-126"><strong>Suggerimento tasto</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-128">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-128">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-129">Stringa che rappresenta il tasto di scelta rapida di un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-130">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-131">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d8a-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-134">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-134">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-135">Stringa che rappresenta il testo visualizzato su un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-136">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-137">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d8a-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-140">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-140">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-141">Stringa che rappresenta il testo visualizzato su un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-142">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-143">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d8a-144"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-146">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-146">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-147"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-148">Stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di cifre, lettere o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="d0d8a-149">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d8a-150"><strong>Simbolo</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-152">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-152">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-153"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-154">Stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di cifre, lettere o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="d0d8a-155">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d8a-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-158">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-158">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-159">Stringa che rappresenta il testo visualizzato su un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-160">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-161">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d8a-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="d0d8a-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="d0d8a-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d8a-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="d0d8a-164">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-164">No</span></span><br/></td>
<td><span data-ttu-id="d0d8a-165">Stringa che rappresenta il testo visualizzato su un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="d0d8a-166">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="d0d8a-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d0d8a-167">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d0d8a-168">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d0d8a-168">Child elements</span></span>



| <span data-ttu-id="d0d8a-169">Elemento</span><span class="sxs-lookup"><span data-stu-id="d0d8a-169">Element</span></span>                                                                                                     | <span data-ttu-id="d0d8a-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0d8a-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="d0d8a-171">**Comando. Comment**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="d0d8a-172">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="d0d8a-174">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-175">**Command. suggerimento**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="d0d8a-176">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-177">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="d0d8a-178">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-179">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="d0d8a-180">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-181">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="d0d8a-182">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-183">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="d0d8a-184">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="d0d8a-186">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-187">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="d0d8a-188">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-189">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="d0d8a-190">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-191">**Command. Symbol**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="d0d8a-192">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-193">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="d0d8a-194">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="d0d8a-195">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="d0d8a-196">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="d0d8a-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d0d8a-197">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d0d8a-197">Parent elements</span></span>



| <span data-ttu-id="d0d8a-198">Elemento</span><span class="sxs-lookup"><span data-stu-id="d0d8a-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0d8a-199">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="d0d8a-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d0d8a-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0d8a-200">Remarks</span></span>

<span data-ttu-id="d0d8a-201">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-201">Required.</span></span>

<span data-ttu-id="d0d8a-202">Può essere presente una o più volte per ogni elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8a-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="d0d8a-203">Gli elementi figlio dell'elemento **Command** possono verificarsi in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="d0d8a-204">In genere, le risorse dei comandi sono dichiarate nel markup della barra multifunzione, ma possono anche essere impostate in fase di esecuzione con una chiamata a [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="d0d8a-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="d0d8a-205">È ad esempio possibile impostare la proprietà pkey del [ \_ \_ Suggerimento utente](windowsribbon-reference-properties-uipkey-keytip.md) per un comando anziché dichiarare un valore nel markup con l'elemento [**Command. suggerimento**](windowsribbon-element-command-keytip.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8a-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="d0d8a-206">Nei casi in cui le proprietà del comando, ad esempio etichette e immagini, non possono essere impostate con [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , possono essere invalidate con una chiamata a [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="d0d8a-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="d0d8a-207">Dopo l'invalidamento, il Framework esegue una query sull'applicazione host per ottenere i dettagli della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="d0d8a-208">Una risorsa non può essere ripristinata dalla tabella delle risorse di markup dopo che è stata invalidata.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="d0d8a-209">Una definizione di comando viene aggiunta al file di intestazione di markup della barra multifunzione per ogni **comando** dichiarato nel markup.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="d0d8a-210">Il valore di *Suggerimento* tasto di scelta funge da tasto di scelta rapida per un comando, a meno che il comando non venga esposto tramite una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="d0d8a-211">In questo caso, il Framework ignora il valore del tasto di *Suggerimento* e usa invece un carattere preceduto da una e commerciale come specificato da *LabelTitle* o dall' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="d0d8a-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="d0d8a-212">Se nessuna e commerciale è specificata da *LabelTitle* o dall'etichetta pkey dell'interfaccia utente \_ \_ , non viene esposto alcun tasto di scelta rapida o tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d0d8a-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="d0d8a-213">Esempio</span><span class="sxs-lookup"><span data-stu-id="d0d8a-213">Examples</span></span>

<span data-ttu-id="d0d8a-214">Nell'esempio seguente viene illustrato un manifesto di elementi **Command** per una scheda **Home** .</span><span class="sxs-lookup"><span data-stu-id="d0d8a-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




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




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="d0d8a-215">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d0d8a-215">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d0d8a-216">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0d8a-216">Minimum supported system</span></span><br/> | <span data-ttu-id="d0d8a-217">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0d8a-217">Windows 7</span></span> |
| <span data-ttu-id="d0d8a-218">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="d0d8a-218">Can be empty</span></span>                        | <span data-ttu-id="d0d8a-219">No</span><span class="sxs-lookup"><span data-stu-id="d0d8a-219">No</span></span>        |



 

