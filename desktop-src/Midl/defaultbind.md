---
title: defaultbind (attributo)
description: L'attributo \ defaultbind \ indica la singola proprietà associabile che meglio rappresenta l'oggetto.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- attributo MIDL di defaultbind
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046717"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="639ae-104">defaultbind (attributo)</span><span class="sxs-lookup"><span data-stu-id="639ae-104">defaultbind attribute</span></span>

<span data-ttu-id="639ae-105">L'attributo **\[ defaultbind \]** indica la singola proprietà associabile che meglio rappresenta l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="639ae-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="639ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="639ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639ae-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="639ae-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-108">Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="639ae-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="639ae-109">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="639ae-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="639ae-110">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="639ae-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-111">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="639ae-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="639ae-112">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="639ae-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-113">Specifica un elenco di uno o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="639ae-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="639ae-114">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="639ae-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="639ae-115">*returnType*</span><span class="sxs-lookup"><span data-stu-id="639ae-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-116">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="639ae-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="639ae-117">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="639ae-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-118">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="639ae-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="639ae-119">*params*</span><span class="sxs-lookup"><span data-stu-id="639ae-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="639ae-120">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="639ae-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="639ae-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="639ae-121">Remarks</span></span>

<span data-ttu-id="639ae-122">Anche le proprietà con l'attributo **\[ defaultbind \]** devono avere l' **\[** attributo [**associabile**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="639ae-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="639ae-123">Solo una proprietà in un'interfaccia o in un'interfaccia dispatch può avere l'attributo **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="639ae-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="639ae-124">Questo attributo viene usato dai contenitori che hanno un modello utente che implica l'associazione a un oggetto anziché l'associazione a una proprietà di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="639ae-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="639ae-125">Un oggetto può supportare data binding ma non avere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="639ae-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="639ae-126">Flags</span><span class="sxs-lookup"><span data-stu-id="639ae-126">Flags</span></span>

<span data-ttu-id="639ae-127">FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND</span><span class="sxs-lookup"><span data-stu-id="639ae-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="639ae-128">Esempi</span><span class="sxs-lookup"><span data-stu-id="639ae-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="639ae-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="639ae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639ae-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="639ae-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="639ae-131">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="639ae-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="639ae-132">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="639ae-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="639ae-133">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="639ae-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="639ae-134">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="639ae-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 