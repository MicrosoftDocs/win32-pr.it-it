---
title: displaybind (attributo)
description: L'attributo \ displaybind \ indica una proprietà che deve essere visualizzata all'utente come associabile.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- attributo MIDL di displaybind
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725434"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="5f70f-104">displaybind (attributo)</span><span class="sxs-lookup"><span data-stu-id="5f70f-104">displaybind attribute</span></span>

<span data-ttu-id="5f70f-105">L'attributo **\[ displaybind \]** indica una proprietà che deve essere visualizzata all'utente come associabile.</span><span class="sxs-lookup"><span data-stu-id="5f70f-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="5f70f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f70f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f70f-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5f70f-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-108">Specifica un elenco facoltativo di attributi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5f70f-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5f70f-109">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="5f70f-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-110">Nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5f70f-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="5f70f-111">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="5f70f-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-112">Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo restituito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="5f70f-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="5f70f-113">*returnType*</span><span class="sxs-lookup"><span data-stu-id="5f70f-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-114">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="5f70f-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="5f70f-115">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="5f70f-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-116">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ displaybind \]** .</span><span class="sxs-lookup"><span data-stu-id="5f70f-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="5f70f-117">*params*</span><span class="sxs-lookup"><span data-stu-id="5f70f-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="5f70f-118">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="5f70f-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f70f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f70f-119">Remarks</span></span>

<span data-ttu-id="5f70f-120">Anche le proprietà con l'attributo **\[ displaybind \]** devono avere l' **\[** attributo [**associabile**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5f70f-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="5f70f-121">Un oggetto può supportare data binding ma non avere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="5f70f-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="5f70f-122">Flags</span><span class="sxs-lookup"><span data-stu-id="5f70f-122">Flags</span></span>

<span data-ttu-id="5f70f-123">FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND</span><span class="sxs-lookup"><span data-stu-id="5f70f-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="5f70f-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="5f70f-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="5f70f-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5f70f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f70f-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="5f70f-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="5f70f-127">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="5f70f-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="5f70f-128">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="5f70f-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5f70f-129">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="5f70f-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5f70f-130">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="5f70f-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 