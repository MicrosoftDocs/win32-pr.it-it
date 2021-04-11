---
title: entry (attributo)
description: L'attributo \ entry \ specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- attributo voce MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336951"
---
# <a name="entry-attribute"></a><span data-ttu-id="154a4-104">entry (attributo)</span><span class="sxs-lookup"><span data-stu-id="154a4-104">entry attribute</span></span>

<span data-ttu-id="154a4-105">L'attributo **\[ entry \]** specifica una funzione o una costante esportata in un modulo identificando il punto di ingresso nella dll.</span><span class="sxs-lookup"><span data-stu-id="154a4-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="154a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="154a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="154a4-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="154a4-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="154a4-108">Specifica un numero di identificazione univoco universale per il [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="154a4-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="154a4-109">*ID di ingresso*</span><span class="sxs-lookup"><span data-stu-id="154a4-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="154a4-110">Specifica il nome della funzione del punto di ingresso del modulo o il numero di identificazione intero.</span><span class="sxs-lookup"><span data-stu-id="154a4-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="154a4-111">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="154a4-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="154a4-112">Specifica zero o più attributi per il compilatore MIDL da applicare al [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="154a4-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="154a4-113">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="154a4-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="154a4-114">Specifica il nome usato da altri componenti software per indicare il [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="154a4-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="154a4-115">*elemento element*</span><span class="sxs-lookup"><span data-stu-id="154a4-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="154a4-116">Specifica una o più istruzioni di definizione degli elementi del modulo.</span><span class="sxs-lookup"><span data-stu-id="154a4-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="154a4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="154a4-117">Remarks</span></span>

<span data-ttu-id="154a4-118">Se la variabile *EntryID* dell'attributo **\[ entry \]** è una stringa, si tratta di un punto di ingresso denominato.</span><span class="sxs-lookup"><span data-stu-id="154a4-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="154a4-119">Se *EntryID* è un numero, il punto di ingresso viene definito da un ordinale.</span><span class="sxs-lookup"><span data-stu-id="154a4-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="154a4-120">Questo attributo fornisce un modo per ottenere l'indirizzo di una funzione in un modulo.</span><span class="sxs-lookup"><span data-stu-id="154a4-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="154a4-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="154a4-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="154a4-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="154a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154a4-123">**DllName**</span><span class="sxs-lookup"><span data-stu-id="154a4-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="154a4-124">**modulo**</span><span class="sxs-lookup"><span data-stu-id="154a4-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="154a4-125">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="154a4-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="154a4-126">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="154a4-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="154a4-127">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="154a4-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 