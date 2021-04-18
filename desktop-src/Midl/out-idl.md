---
title: out (attributo)
description: L'attributo \ out \ identifica i parametri del puntatore restituiti dalla routine chiamata alla procedura chiamante (dal server al client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- attributo out MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299737"
---
# <a name="out-attribute"></a><span data-ttu-id="e22a0-104">out (attributo)</span><span class="sxs-lookup"><span data-stu-id="e22a0-104">out attribute</span></span>

<span data-ttu-id="e22a0-105">L' \[ attributo **out** \] identifica i parametri del puntatore restituiti dalla routine chiamata alla procedura chiamante (dal server al client).</span><span class="sxs-lookup"><span data-stu-id="e22a0-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="e22a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e22a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22a0-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e22a0-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-108">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="e22a0-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e22a0-109">Gli attributi di funzione validi sono \[ [**callback**](callback.md) \] , \[ [**local**](local.md), \] l'attributo Pointer \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] e gli attributi Usage \[ [**String**](string.md) \] , \[ [**Ignore**](ignore.md) \] e \[ [**Context \_ handle**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="e22a0-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="e22a0-110">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="e22a0-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-111">Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="e22a0-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="e22a0-112">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e22a0-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e22a0-113">*puntatore-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="e22a0-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-114">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="e22a0-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="e22a0-115">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="e22a0-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e22a0-116">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="e22a0-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-117">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e22a0-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e22a0-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e22a0-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-119">Specifica zero o più attributi appropriati per un tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="e22a0-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="e22a0-120">Gli attributi di parametro con l' \[ attributo **out** \] possono anche prendere l'attributo Directional \[ **out** \] . gli attributi di campo \[ [**First \_ sono**](first-is.md) \] , \[ [**Last \_ is**](last-is.md) \] , \[ [**length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**size \_ is**](size-is.md) \] e \[ [**Switch \_ Type**](switch-type.md), \] l'attributo Pointer \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] e l' \[ [**\_ handle**](context-handle.md) \] e la \[ [**stringa**](string.md)del contesto degli attributi Usage \] .</span><span class="sxs-lookup"><span data-stu-id="e22a0-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="e22a0-121">L'attributo Usage \[ [**Ignore**](ignore.md) \] non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="e22a0-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="e22a0-122">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e22a0-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e22a0-123">*dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="e22a0-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e22a0-124">Specifica i dichiaratori standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="e22a0-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e22a0-125">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e22a0-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e22a0-126">Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e22a0-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e22a0-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e22a0-127">Remarks</span></span>

<span data-ttu-id="e22a0-128">L' \[ attributo **out** \] indica che un parametro che funge da puntatore e i dati associati in memoria devono essere passati di nuovo dalla procedura chiamata alla procedura chiamante.</span><span class="sxs-lookup"><span data-stu-id="e22a0-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="e22a0-129">L' \[ attributo **out** \] deve essere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="e22a0-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="e22a0-130">I compilatori IDL DCE richiedono la presenza di un \* dichiaratore esplicito come puntatore nella dichiarazione di parametro.</span><span class="sxs-lookup"><span data-stu-id="e22a0-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="e22a0-131">Microsoft IDL offre un'estensione che elimina questo requisito e consente una matrice o un tipo di puntatore definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e22a0-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="e22a0-132">Un attributo correlato, \[ [**in**](in.md) \] , indica che il parametro viene passato dalla routine chiamante alla routine chiamata.</span><span class="sxs-lookup"><span data-stu-id="e22a0-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="e22a0-133">Gli \[  \] attributi in e \[ **out** \] specificano la direzione in cui vengono passati i parametri.</span><span class="sxs-lookup"><span data-stu-id="e22a0-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="e22a0-134">Un parametro può essere definito solo \[ **in**, solo in uscita o in uscita \] \[  \] \[   \] .</span><span class="sxs-lookup"><span data-stu-id="e22a0-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="e22a0-135">\[  \] Si presuppone che un parametro out-only non sia definito quando viene chiamata la procedura remota e che la memoria per l'oggetto venga allocata dal server.</span><span class="sxs-lookup"><span data-stu-id="e22a0-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="e22a0-136">Poiché il puntatore/parametri di primo livello deve sempre puntare a una risorsa di archiviazione valida e pertanto non può essere **null**, \[ **out** \] non può essere applicato ai \[ puntatori [**univoci**](unique.md) \] o \[ [**ptr**](ptr.md) di primo livello \] .</span><span class="sxs-lookup"><span data-stu-id="e22a0-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="e22a0-137">I parametri che corrispondono \[  \] a puntatori univoci o \[ **ptr** \] devono essere \[ [**in**](in.md) \] o \[ **in**, **out** \] Parameters.</span><span class="sxs-lookup"><span data-stu-id="e22a0-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="e22a0-138">Esempi</span><span class="sxs-lookup"><span data-stu-id="e22a0-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="e22a0-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e22a0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22a0-140">**matrici**</span><span class="sxs-lookup"><span data-stu-id="e22a0-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e22a0-141">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="e22a0-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e22a0-142">**callback**</span><span class="sxs-lookup"><span data-stu-id="e22a0-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e22a0-143">**const**</span><span class="sxs-lookup"><span data-stu-id="e22a0-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e22a0-144">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e22a0-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e22a0-145">**enum**</span><span class="sxs-lookup"><span data-stu-id="e22a0-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e22a0-146">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="e22a0-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e22a0-147">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="e22a0-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e22a0-148">**in**</span><span class="sxs-lookup"><span data-stu-id="e22a0-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="e22a0-149">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="e22a0-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e22a0-150">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="e22a0-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e22a0-151">**locale**</span><span class="sxs-lookup"><span data-stu-id="e22a0-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e22a0-152">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="e22a0-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e22a0-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e22a0-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e22a0-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="e22a0-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e22a0-155">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="e22a0-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e22a0-156">**string**</span><span class="sxs-lookup"><span data-stu-id="e22a0-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e22a0-157">**struct**</span><span class="sxs-lookup"><span data-stu-id="e22a0-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e22a0-158">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="e22a0-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e22a0-159">**Unione**</span><span class="sxs-lookup"><span data-stu-id="e22a0-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e22a0-160">**unico**</span><span class="sxs-lookup"><span data-stu-id="e22a0-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 