---
title: Proprietà Command. Comment
description: Rappresenta un commento, o annotazione, per un comando.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Barra multifunzione di Windows Command. Comment
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400854"
---
# <a name="commandcomment-property"></a><span data-ttu-id="a8b20-104">Proprietà Command. Comment</span><span class="sxs-lookup"><span data-stu-id="a8b20-104">Command.Comment property</span></span>

<span data-ttu-id="a8b20-105">Rappresenta un commento, o annotazione, per un comando.</span><span class="sxs-lookup"><span data-stu-id="a8b20-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="a8b20-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a8b20-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="a8b20-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a8b20-107">Attributes</span></span>

<span data-ttu-id="a8b20-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a8b20-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8b20-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a8b20-109">Child elements</span></span>

<span data-ttu-id="a8b20-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a8b20-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a8b20-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a8b20-111">Parent elements</span></span>



| <span data-ttu-id="a8b20-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8b20-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="a8b20-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="a8b20-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a8b20-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8b20-114">Remarks</span></span>

<span data-ttu-id="a8b20-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a8b20-115">Optional.</span></span>

<span data-ttu-id="a8b20-116">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="a8b20-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="a8b20-117">Il commento è associato a una definizione di comando nel file di intestazione della barra multifunzione, ad esempio `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="a8b20-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="a8b20-118">Questo elemento contiene un valore di tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="a8b20-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="a8b20-119">La lunghezza massima consentita è di 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a8b20-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="a8b20-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8b20-120">Examples</span></span>

<span data-ttu-id="a8b20-121">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. Comment** .</span><span class="sxs-lookup"><span data-stu-id="a8b20-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a8b20-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b20-122">Requirements</span></span>



| <span data-ttu-id="a8b20-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b20-123">Requirement</span></span> | <span data-ttu-id="a8b20-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b20-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a8b20-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b20-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b20-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8b20-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a8b20-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b20-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b20-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b20-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





