---
title: Proprietà Command.Id
description: Rappresenta un ID univoco per un comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Barra multifunzione di Windows proprietà Command.Id
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478640"
---
# <a name="commandid-property"></a><span data-ttu-id="e8910-104">Proprietà Command.Id</span><span class="sxs-lookup"><span data-stu-id="e8910-104">Command.Id property</span></span>

<span data-ttu-id="e8910-105">Rappresenta un ID univoco per un comando.</span><span class="sxs-lookup"><span data-stu-id="e8910-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="e8910-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e8910-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="e8910-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="e8910-107">Attributes</span></span>

<span data-ttu-id="e8910-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="e8910-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e8910-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e8910-109">Child elements</span></span>

<span data-ttu-id="e8910-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="e8910-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e8910-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e8910-111">Parent elements</span></span>



| <span data-ttu-id="e8910-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8910-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="e8910-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="e8910-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e8910-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8910-114">Remarks</span></span>

<span data-ttu-id="e8910-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e8910-115">Optional.</span></span>

<span data-ttu-id="e8910-116">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="e8910-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="e8910-117">L'ID è associato a una definizione di comando nel file di intestazione della barra multifunzione, ad esempio `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="e8910-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="e8910-118">Questo elemento contiene un valore dall'Unione dei tipi *xs: positiveInteger* e *xs: String* vincolato a un valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="e8910-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="e8910-119">La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="e8910-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="e8910-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8910-120">Examples</span></span>

<span data-ttu-id="e8910-121">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command.ID** .</span><span class="sxs-lookup"><span data-stu-id="e8910-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e8910-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8910-122">Requirements</span></span>



| <span data-ttu-id="e8910-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8910-123">Requirement</span></span> | <span data-ttu-id="e8910-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e8910-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e8910-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8910-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8910-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8910-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e8910-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8910-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8910-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8910-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





