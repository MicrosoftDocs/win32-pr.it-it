---
title: bindable (attributo)
description: L'attributo \ Bindable \ indica che la proprietà supporta data binding.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- attributo MIDL associabile
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299660"
---
# <a name="bindable-attribute"></a><span data-ttu-id="47e49-104">bindable (attributo)</span><span class="sxs-lookup"><span data-stu-id="47e49-104">bindable attribute</span></span>

<span data-ttu-id="47e49-105">L'attributo **\[ associabile \]** indica che la proprietà supporta data binding.</span><span class="sxs-lookup"><span data-stu-id="47e49-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="47e49-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e49-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="47e49-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-108">Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="47e49-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="47e49-109">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="47e49-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="47e49-110">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="47e49-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-111">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="47e49-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="47e49-112">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="47e49-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-113">Specifica zero o più attributi che si applicano al prototipo di funzione per una proprietà o un metodo in un'interfaccia o in un' [**interfaccia**](interface.md) [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="47e49-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="47e49-114">Gli attributi seguenti sono validi: [**\[ helpstring \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)e [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="47e49-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="47e49-115">Se viene specificato **vararg** , l'ultimo parametro deve essere una matrice sicura di tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="47e49-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="47e49-116">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="47e49-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="47e49-117">*returnType*</span><span class="sxs-lookup"><span data-stu-id="47e49-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-118">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="47e49-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="47e49-119">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="47e49-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-120">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ associabile \]** .</span><span class="sxs-lookup"><span data-stu-id="47e49-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="47e49-121">*params*</span><span class="sxs-lookup"><span data-stu-id="47e49-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="47e49-122">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="47e49-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47e49-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="47e49-123">Remarks</span></span>

<span data-ttu-id="47e49-124">Grazie al supporto di data binding, l'attributo **\[ associabile \]** consente al client di ricevere notifiche ogni volta che una proprietà modifica il valore.</span><span class="sxs-lookup"><span data-stu-id="47e49-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="47e49-125">Se si desidera che il client riceva una notifica di modifiche imminenti a una proprietà, utilizzare l'attributo [**\[ requestedit \]**](requestedit.md) .</span><span class="sxs-lookup"><span data-stu-id="47e49-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="47e49-126">Poiché l'attributo **\[ associabile \]** si riferisce alla proprietà nel suo complesso, è necessario specificare ogni volta che la proprietà è definita.</span><span class="sxs-lookup"><span data-stu-id="47e49-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="47e49-127">Pertanto, è necessario specificare l'attributo sia nella funzione di accesso alla proprietà che nella funzione di impostazione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="47e49-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="47e49-128">Flags</span><span class="sxs-lookup"><span data-stu-id="47e49-128">Flags</span></span>

<span data-ttu-id="47e49-129">FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE</span><span class="sxs-lookup"><span data-stu-id="47e49-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="47e49-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="47e49-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="47e49-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="47e49-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e49-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="47e49-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="47e49-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="47e49-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="47e49-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="47e49-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="47e49-135">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="47e49-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="47e49-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="47e49-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="47e49-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="47e49-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="47e49-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="47e49-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="47e49-139">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="47e49-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="47e49-140">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="47e49-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="47e49-141">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="47e49-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="47e49-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="47e49-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="47e49-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="47e49-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="47e49-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="47e49-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="47e49-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="47e49-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="47e49-146">**string**</span><span class="sxs-lookup"><span data-stu-id="47e49-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="47e49-147">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="47e49-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="47e49-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="47e49-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 