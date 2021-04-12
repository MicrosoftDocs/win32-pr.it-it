---
title: immediatebind (attributo)
description: L'attributo \ immediatebind \ indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- attributo MIDL di immediatebind
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223494"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="50bd2-104">immediatebind (attributo)</span><span class="sxs-lookup"><span data-stu-id="50bd2-104">immediatebind attribute</span></span>

<span data-ttu-id="50bd2-105">L'attributo **\[ immediatebind \]** indica che il database riceverà immediatamente una notifica di tutte le modifiche apportate a una proprietà di un oggetto associato a dati.</span><span class="sxs-lookup"><span data-stu-id="50bd2-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="50bd2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50bd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50bd2-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="50bd2-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-108">Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="50bd2-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="50bd2-109">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="50bd2-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-110">Specifica il nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="50bd2-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="50bd2-111">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="50bd2-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-112">Zero o più attributi di funzione.</span><span class="sxs-lookup"><span data-stu-id="50bd2-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="50bd2-113">*returnType*</span><span class="sxs-lookup"><span data-stu-id="50bd2-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-114">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="50bd2-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="50bd2-115">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="50bd2-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-116">Specifica il nome della funzione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="50bd2-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="50bd2-117">*params*</span><span class="sxs-lookup"><span data-stu-id="50bd2-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="50bd2-118">Zero o più parametri di funzione.</span><span class="sxs-lookup"><span data-stu-id="50bd2-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50bd2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="50bd2-119">Remarks</span></span>

<span data-ttu-id="50bd2-120">L'attributo **\[ immediatebind \]** consente ai controlli di distinguere tra le proprietà che devono notificare al database ogni modifica e quelle che non lo fanno.</span><span class="sxs-lookup"><span data-stu-id="50bd2-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="50bd2-121">Ogni modifica apportata a un controllo CheckBox, ad esempio, deve essere inviata immediatamente al database sottostante, anche se il controllo non ha perso lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="50bd2-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="50bd2-122">Tuttavia, per un controllo ListBox, viene apportata una modifica ogni volta che viene evidenziata un'altra selezione.</span><span class="sxs-lookup"><span data-stu-id="50bd2-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="50bd2-123">La notifica al database di una modifica prima che il controllo perda lo stato attivo non è efficiente e non è necessario.</span><span class="sxs-lookup"><span data-stu-id="50bd2-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="50bd2-124">L'attributo **\[ immediatebind \]** consente di specificare, impostando il bit immediatebind, singole proprietà in un form le cui modifiche devono essere segnalate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="50bd2-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="50bd2-125">Anche le proprietà con l'attributo **\[ immediatebind \]** devono avere l' **\[** attributo [**associabile**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="50bd2-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="50bd2-126">Flags</span><span class="sxs-lookup"><span data-stu-id="50bd2-126">Flags</span></span>

<span data-ttu-id="50bd2-127">FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND</span><span class="sxs-lookup"><span data-stu-id="50bd2-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="50bd2-128">Esempi</span><span class="sxs-lookup"><span data-stu-id="50bd2-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="50bd2-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50bd2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bd2-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="50bd2-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="50bd2-131">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="50bd2-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="50bd2-132">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="50bd2-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="50bd2-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="50bd2-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="50bd2-134">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="50bd2-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="50bd2-135">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="50bd2-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="50bd2-136">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="50bd2-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 