---
title: Proprietà Command. TooltipDescription
description: Rappresenta una descrizione della descrizione comando.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Barra multifunzione di Windows Command. TooltipDescription
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 288578e74420912b7454be5037c4b2651918ac6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302310"
---
# <a name="commandtooltipdescription-property"></a><span data-ttu-id="83827-104">Proprietà Command. TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="83827-104">Command.TooltipDescription property</span></span>

<span data-ttu-id="83827-105">Rappresenta una descrizione della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="83827-105">Represents a tooltip description.</span></span>

## <a name="usage"></a><span data-ttu-id="83827-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="83827-106">Usage</span></span>

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a><span data-ttu-id="83827-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="83827-107">Attributes</span></span>

<span data-ttu-id="83827-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="83827-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="83827-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="83827-109">Child elements</span></span>



| <span data-ttu-id="83827-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="83827-110">Element</span></span>                                                   | <span data-ttu-id="83827-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83827-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="83827-112">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="83827-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="83827-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="83827-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="83827-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="83827-114">Parent elements</span></span>



| <span data-ttu-id="83827-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="83827-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="83827-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="83827-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="83827-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="83827-117">Remarks</span></span>

<span data-ttu-id="83827-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="83827-118">Optional.</span></span>

<span data-ttu-id="83827-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="83827-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="83827-120">**Command. TooltipDescription** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="83827-120">**Command.TooltipDescription** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters .</span></span>

> [!Note]  
> <span data-ttu-id="83827-121">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="83827-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="83827-122">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="83827-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="83827-123">Se non viene specificato alcun valore per **Command. TooltipDescription**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="83827-123">If no value is supplied for **Command.TooltipDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="83827-124">Se **Command. TooltipDescription** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="83827-124">If **Command.TooltipDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="83827-125">**Command. TooltipDescription** supporta solo l'allineamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="83827-125">**Command.TooltipDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="83827-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="83827-126">Examples</span></span>

<span data-ttu-id="83827-127">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. TooltipDescription** .</span><span class="sxs-lookup"><span data-stu-id="83827-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipDescription** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="83827-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83827-128">Requirements</span></span>



| <span data-ttu-id="83827-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="83827-129">Requirement</span></span> | <span data-ttu-id="83827-130">Valore</span><span class="sxs-lookup"><span data-stu-id="83827-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="83827-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83827-131">Minimum supported client</span></span><br/> | <span data-ttu-id="83827-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83827-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="83827-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83827-133">Minimum supported server</span></span><br/> | <span data-ttu-id="83827-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="83827-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83827-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83827-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83827-136">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="83827-136">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





