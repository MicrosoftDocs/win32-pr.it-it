---
title: Proprietà Command. TooltipTitle
description: Rappresenta il titolo di una descrizione comandi.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Barra multifunzione di Windows Command. TooltipTitle
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478617"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="b8e7e-104">Proprietà Command. TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="b8e7e-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="b8e7e-105">Rappresenta il titolo di una descrizione comandi.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="b8e7e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b8e7e-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="b8e7e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="b8e7e-107">Attributes</span></span>

<span data-ttu-id="b8e7e-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b8e7e-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b8e7e-109">Child elements</span></span>



| <span data-ttu-id="b8e7e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8e7e-110">Element</span></span>                                                   | <span data-ttu-id="b8e7e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8e7e-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b8e7e-112">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="b8e7e-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="b8e7e-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="b8e7e-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b8e7e-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b8e7e-114">Parent elements</span></span>



| <span data-ttu-id="b8e7e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8e7e-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="b8e7e-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="b8e7e-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b8e7e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8e7e-117">Remarks</span></span>

<span data-ttu-id="b8e7e-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-118">Optional.</span></span>

<span data-ttu-id="b8e7e-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="b8e7e-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="b8e7e-120">**Command. TooltipTitle** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="b8e7e-121">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="b8e7e-122">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="b8e7e-123">Se non viene specificato alcun valore per **Command. TooltipTitle**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="b8e7e-124">Se **Command. TooltipTitle** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="b8e7e-125">**Command. TooltipTitle** supporta solo l'allineamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="b8e7e-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="b8e7e-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8e7e-126">Examples</span></span>

<span data-ttu-id="b8e7e-127">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. TooltipTitle** .</span><span class="sxs-lookup"><span data-stu-id="b8e7e-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b8e7e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8e7e-128">Requirements</span></span>



| <span data-ttu-id="b8e7e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e7e-129">Requirement</span></span> | <span data-ttu-id="b8e7e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e7e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b8e7e-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8e7e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e7e-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b8e7e-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b8e7e-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8e7e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e7e-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8e7e-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8e7e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e7e-136">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="b8e7e-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





