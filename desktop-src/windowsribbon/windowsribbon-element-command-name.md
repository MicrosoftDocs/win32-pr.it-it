---
title: Proprietà Command.Name
description: Rappresenta il nome di un comando.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Barra multifunzione di Windows proprietà Command.Name
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048658"
---
# <a name="commandname-property"></a><span data-ttu-id="281a8-104">Proprietà Command.Name</span><span class="sxs-lookup"><span data-stu-id="281a8-104">Command.Name property</span></span>

<span data-ttu-id="281a8-105">Rappresenta il nome di un comando.</span><span class="sxs-lookup"><span data-stu-id="281a8-105">Represents the name of a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="281a8-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="281a8-106">Usage</span></span>

``` syntax
<Command.Name/>
```

## <a name="attributes"></a><span data-ttu-id="281a8-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="281a8-107">Attributes</span></span>

<span data-ttu-id="281a8-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="281a8-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="281a8-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="281a8-109">Child elements</span></span>

<span data-ttu-id="281a8-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="281a8-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="281a8-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="281a8-111">Parent elements</span></span>



| <span data-ttu-id="281a8-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="281a8-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="281a8-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="281a8-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="281a8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="281a8-114">Remarks</span></span>

<span data-ttu-id="281a8-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="281a8-115">Optional.</span></span>

<span data-ttu-id="281a8-116">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="281a8-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="281a8-117">Nel markup viene fatto riferimento a **Command.Name** per associare un comando a un controllo tramite l'attributo *CommandName* del controllo.</span><span class="sxs-lookup"><span data-stu-id="281a8-117">**Command.Name** is referenced in markup to associate a Command with a control through the *CommandName* attribute of the control.</span></span>

<span data-ttu-id="281a8-118">Questo elemento contiene un valore di tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="281a8-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="281a8-119">Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="281a8-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="281a8-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="281a8-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="281a8-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="281a8-121">Examples</span></span>

<span data-ttu-id="281a8-122">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command.Name** .</span><span class="sxs-lookup"><span data-stu-id="281a8-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Name** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="281a8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="281a8-123">Requirements</span></span>



| <span data-ttu-id="281a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="281a8-124">Requirement</span></span> | <span data-ttu-id="281a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="281a8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="281a8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="281a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="281a8-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="281a8-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="281a8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="281a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="281a8-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="281a8-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





