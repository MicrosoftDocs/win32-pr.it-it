---
title: Proprietà String. Content
description: Rappresenta il contenuto di una risorsa di stringa.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Barra multifunzione di Windows String. Content
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301401"
---
# <a name="stringcontent-property"></a><span data-ttu-id="b36a0-104">Proprietà String. Content</span><span class="sxs-lookup"><span data-stu-id="b36a0-104">String.Content property</span></span>

<span data-ttu-id="b36a0-105">Rappresenta il contenuto di una risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="b36a0-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="b36a0-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b36a0-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="b36a0-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="b36a0-107">Attributes</span></span>

<span data-ttu-id="b36a0-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="b36a0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b36a0-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b36a0-109">Child elements</span></span>

<span data-ttu-id="b36a0-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b36a0-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b36a0-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b36a0-111">Parent elements</span></span>



| <span data-ttu-id="b36a0-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="b36a0-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="b36a0-113">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="b36a0-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b36a0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b36a0-114">Remarks</span></span>

<span data-ttu-id="b36a0-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b36a0-115">Optional.</span></span>

<span data-ttu-id="b36a0-116">Può verificarsi al massimo una volta per ogni elemento [**stringa**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="b36a0-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="b36a0-117">Questo elemento contiene un valore di tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="b36a0-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="b36a0-118">Il valore è vincolato a una stringa composta da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="b36a0-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="b36a0-119">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="b36a0-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="b36a0-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b36a0-120">Examples</span></span>

<span data-ttu-id="b36a0-121">Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una Dichiarazione **String. Content** .</span><span class="sxs-lookup"><span data-stu-id="b36a0-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="b36a0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b36a0-122">Requirements</span></span>



| <span data-ttu-id="b36a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b36a0-123">Requirement</span></span> | <span data-ttu-id="b36a0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b36a0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b36a0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b36a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b36a0-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b36a0-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b36a0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b36a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b36a0-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b36a0-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





