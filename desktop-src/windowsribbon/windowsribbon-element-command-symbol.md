---
title: Proprietà Command. Symbol
description: Rappresenta il nome di un comando a cui è possibile fare riferimento esternamente.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Barra multifunzione di Windows Command. Symbol
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302311"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="52c1d-104">Proprietà Command. Symbol</span><span class="sxs-lookup"><span data-stu-id="52c1d-104">Command.Symbol property</span></span>

<span data-ttu-id="52c1d-105">Rappresenta il nome di un [**comando**](windowsribbon-element-command.md) a cui è possibile fare riferimento esternamente.</span><span class="sxs-lookup"><span data-stu-id="52c1d-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="52c1d-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="52c1d-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="52c1d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="52c1d-107">Attributes</span></span>

<span data-ttu-id="52c1d-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="52c1d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="52c1d-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="52c1d-109">Child elements</span></span>

<span data-ttu-id="52c1d-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="52c1d-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="52c1d-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="52c1d-111">Parent elements</span></span>



| <span data-ttu-id="52c1d-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="52c1d-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="52c1d-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="52c1d-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="52c1d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c1d-114">Remarks</span></span>

<span data-ttu-id="52c1d-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="52c1d-115">Optional.</span></span>

<span data-ttu-id="52c1d-116">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="52c1d-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="52c1d-117">Il simbolo è associato a una definizione di comando nel file di intestazione della barra multifunzione, ad esempio `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="52c1d-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="52c1d-118">Questo elemento contiene un valore di tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="52c1d-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="52c1d-119">Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="52c1d-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="52c1d-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="52c1d-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="52c1d-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="52c1d-121">Examples</span></span>

<span data-ttu-id="52c1d-122">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="52c1d-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="52c1d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c1d-123">Requirements</span></span>



| <span data-ttu-id="52c1d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c1d-124">Requirement</span></span> | <span data-ttu-id="52c1d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="52c1d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="52c1d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c1d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52c1d-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52c1d-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="52c1d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c1d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52c1d-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="52c1d-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





