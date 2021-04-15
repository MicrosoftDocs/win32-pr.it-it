---
title: opzione/align
description: L'opzione/align è funzionalmente identica all'opzione MIDL/ZP ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align switch MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516336"
---
# <a name="align-switch"></a><span data-ttu-id="b6c5c-104">opzione/align</span><span class="sxs-lookup"><span data-stu-id="b6c5c-104">/align switch</span></span>

<span data-ttu-id="b6c5c-105">L'opzione **/align** è funzionalmente identica all'opzione MIDL [**/ZP**](-zp.md) ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di mktyplib.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="b6c5c-106">Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="b6c5c-107">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="b6c5c-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="b6c5c-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b6c5c-109">*allineamento*</span><span class="sxs-lookup"><span data-stu-id="b6c5c-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="b6c5c-110">Specifica l'allineamento per i tipi nella libreria.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="b6c5c-111">Il valore di *allineamento* può essere 1, 2, 4 o 8.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="b6c5c-112">Il valore 1 indica l'allineamento naturale; *n* indica l'allineamento sul byte *n*.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="b6c5c-113">Quando non si specifica l'opzione **/align** , il valore predefinito è 8.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6c5c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6c5c-114">Remarks</span></span>

<span data-ttu-id="b6c5c-115">Se si sta generando un nuovo Makefile, usare l'opzione [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c5c-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="b6c5c-116">Il valore di allineamento corrisponde al valore dell'opzione [**/ZP**](-zp.md) usato dal compilatore Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="b6c5c-117">Assicurarsi di specificare lo stesso allineamento quando si richiama il compilatore C come quando si richiama il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="b6c5c-118">Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="b6c5c-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="b6c5c-119">Per una descrizione dei potenziali rischi correlati all'uso di livelli di compressione non standard, vedere l'argomento della Guida di [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c5c-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="b6c5c-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6c5c-120">Examples</span></span>

<span data-ttu-id="b6c5c-121">**MIDL/align: 4 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="b6c5c-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b6c5c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6c5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c5c-123">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="b6c5c-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b6c5c-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="b6c5c-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




