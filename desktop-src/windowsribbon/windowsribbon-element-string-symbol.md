---
title: Proprietà String. Symbol
description: Rappresenta il nome di una risorsa di stringa.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Proprietà String. Symbol (barra multifunzione di Windows)
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873401"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="a943e-104">Proprietà String. Symbol</span><span class="sxs-lookup"><span data-stu-id="a943e-104">String.Symbol property</span></span>

<span data-ttu-id="a943e-105">Rappresenta il nome di una risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="a943e-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="a943e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a943e-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="a943e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a943e-107">Attributes</span></span>

<span data-ttu-id="a943e-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a943e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a943e-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a943e-109">Child elements</span></span>

<span data-ttu-id="a943e-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a943e-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a943e-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a943e-111">Parent elements</span></span>



| <span data-ttu-id="a943e-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="a943e-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="a943e-113">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="a943e-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a943e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a943e-114">Remarks</span></span>

<span data-ttu-id="a943e-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a943e-115">Optional.</span></span>

<span data-ttu-id="a943e-116">Può verificarsi al massimo una volta per ogni elemento [**stringa**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="a943e-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="a943e-117">Il simbolo è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="a943e-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="a943e-118">Questo elemento contiene un valore di tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="a943e-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="a943e-119">Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="a943e-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="a943e-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a943e-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="a943e-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="a943e-121">Examples</span></span>

<span data-ttu-id="a943e-122">Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una Dichiarazione **String. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="a943e-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="a943e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a943e-123">Requirements</span></span>



| <span data-ttu-id="a943e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a943e-124">Requirement</span></span> | <span data-ttu-id="a943e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a943e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a943e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a943e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a943e-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a943e-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a943e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a943e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a943e-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a943e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





