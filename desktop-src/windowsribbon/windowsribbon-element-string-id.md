---
title: Proprietà String.Id
description: Rappresenta l'ID univoco di una risorsa di stringa.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Barra multifunzione di Windows proprietà String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121066"
---
# <a name="stringid-property"></a><span data-ttu-id="528b0-104">Proprietà String.Id</span><span class="sxs-lookup"><span data-stu-id="528b0-104">String.Id property</span></span>

<span data-ttu-id="528b0-105">Rappresenta l'ID univoco di una risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="528b0-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="528b0-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="528b0-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="528b0-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="528b0-107">Attributes</span></span>

<span data-ttu-id="528b0-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="528b0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="528b0-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="528b0-109">Child elements</span></span>

<span data-ttu-id="528b0-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="528b0-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="528b0-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="528b0-111">Parent elements</span></span>



| <span data-ttu-id="528b0-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="528b0-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="528b0-113">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="528b0-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="528b0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="528b0-114">Remarks</span></span>

<span data-ttu-id="528b0-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="528b0-115">Optional.</span></span>

<span data-ttu-id="528b0-116">Può verificarsi al massimo una volta per ogni elemento [**stringa**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="528b0-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="528b0-117">Il valore di **String.ID** deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="528b0-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="528b0-118">L'ID è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="528b0-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="528b0-119">Questo elemento contiene un valore dall'Unione dei tipi *xs: positiveInteger* e *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="528b0-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="528b0-120">Il valore è vincolato a un valore intero compreso tra 2 e 59999, inclusivi o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="528b0-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="528b0-121">La lunghezza massima è di 10 caratteri con zeri iniziali facoltativi.</span><span class="sxs-lookup"><span data-stu-id="528b0-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="528b0-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="528b0-122">Examples</span></span>

<span data-ttu-id="528b0-123">Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una Dichiarazione **String.ID** .</span><span class="sxs-lookup"><span data-stu-id="528b0-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="528b0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="528b0-124">Requirements</span></span>



| <span data-ttu-id="528b0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="528b0-125">Requirement</span></span> | <span data-ttu-id="528b0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="528b0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="528b0-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="528b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="528b0-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="528b0-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="528b0-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="528b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="528b0-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="528b0-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





