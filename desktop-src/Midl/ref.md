---
title: ref (attributo)
description: L'attributo \ Ref \ identifica un puntatore di riferimento. Viene usato semplicemente per rappresentare un livello di riferimento indiretto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- attributo ref MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872382"
---
# <a name="ref-attribute"></a><span data-ttu-id="5ceca-105">ref (attributo)</span><span class="sxs-lookup"><span data-stu-id="5ceca-105">ref attribute</span></span>

<span data-ttu-id="5ceca-106">L'attributo **\[ ref \]** identifica un puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5ceca-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="5ceca-107">Viene usato semplicemente per rappresentare un livello di riferimento indiretto.</span><span class="sxs-lookup"><span data-stu-id="5ceca-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="5ceca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ceca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ceca-109">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5ceca-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-110">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="5ceca-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="5ceca-111">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md), **\]** gli attributi del puntatore **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l'handle del contesto degli attributi di utilizzo **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="5ceca-112">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="5ceca-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-113">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="5ceca-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-114">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="5ceca-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="5ceca-115">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="5ceca-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-116">*dichiaratore standard*</span><span class="sxs-lookup"><span data-stu-id="5ceca-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-117">Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice.</span><span class="sxs-lookup"><span data-stu-id="5ceca-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="5ceca-118">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5ceca-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-119">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="5ceca-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-120">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="5ceca-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5ceca-121">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5ceca-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="5ceca-122">Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="5ceca-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="5ceca-123">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5ceca-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-124">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5ceca-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-125">Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="5ceca-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="5ceca-126">Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="5ceca-127">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="5ceca-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-128">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5ceca-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-129">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="5ceca-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="5ceca-130">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-131">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="5ceca-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-132">Specifica almeno un dichiaratore di puntatore a cui si applica l'attributo **\[ ref \]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="5ceca-133">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="5ceca-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-134">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="5ceca-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-135">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="5ceca-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="5ceca-136">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5ceca-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ceca-137">È costituito da zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="5ceca-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="5ceca-138">Gli attributi di parametro possono **\[** [](in.md) **\]** attivare e disattivare gli attributi direzionali **\[** [](out-idl.md) **\]** . gli attributi di campo **\[** [**First \_**](first-is.md)sono **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**size \_ is**](size-is.md) **\]** e **\[** [**Switch \_ Type**](switch-type.md), **\]** l'attributo Pointer **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle**](context-handle.md) **\]** e la **\[** [**stringa**](string.md)del contesto degli attributi Usage **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="5ceca-139">L'attributo Usage **\[** [**Ignore**](ignore.md) **\]** non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="5ceca-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="5ceca-140">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="5ceca-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ceca-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ceca-141">Remarks</span></span>

<span data-ttu-id="5ceca-142">Un attributo del puntatore può essere applicato come attributo di tipo, come un attributo di campo che si applica a un membro di struttura, a un membro di Unione o a un parametro; o come attributo di funzione applicabile al tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="5ceca-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="5ceca-143">L'attributo pointer può essere visualizzato anche con la **\[** parola chiave [**\_ default del puntatore**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5ceca-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="5ceca-144">Un puntatore di riferimento presenta le seguenti caratteristiche:</span><span class="sxs-lookup"><span data-stu-id="5ceca-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="5ceca-145">Punta sempre a un archivio valido; il valore non è mai **null**.</span><span class="sxs-lookup"><span data-stu-id="5ceca-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="5ceca-146">È sempre possibile dereferenziare un puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5ceca-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="5ceca-147">Non cambia mai durante una chiamata.</span><span class="sxs-lookup"><span data-stu-id="5ceca-147">Never changes during a call.</span></span> <span data-ttu-id="5ceca-148">Un puntatore di riferimento punta sempre alla stessa risorsa di archiviazione nel client prima e dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5ceca-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="5ceca-149">Non alloca la nuova memoria nel client.</span><span class="sxs-lookup"><span data-stu-id="5ceca-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="5ceca-150">I dati restituiti dal server vengono scritti nella risorsa di archiviazione esistente specificata dal valore del puntatore di riferimento prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="5ceca-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="5ceca-151">Non provoca l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="5ceca-151">Does not cause aliasing.</span></span> <span data-ttu-id="5ceca-152">Non è possibile raggiungere lo spazio di archiviazione a cui punta un puntatore di riferimento da un altro nome nella funzione.</span><span class="sxs-lookup"><span data-stu-id="5ceca-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="5ceca-153">Un puntatore di riferimento non può essere utilizzato come tipo di un puntatore restituito da una funzione.</span><span class="sxs-lookup"><span data-stu-id="5ceca-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="5ceca-154">Se non è specificato alcun attributo per un parametro puntatore di primo livello, viene considerato come un puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5ceca-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="5ceca-155">Esempi</span><span class="sxs-lookup"><span data-stu-id="5ceca-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="5ceca-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5ceca-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ceca-157">**matrici**</span><span class="sxs-lookup"><span data-stu-id="5ceca-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="5ceca-158">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="5ceca-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="5ceca-159">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="5ceca-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ceca-160">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="5ceca-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="5ceca-161">**callback**</span><span class="sxs-lookup"><span data-stu-id="5ceca-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="5ceca-162">**const**</span><span class="sxs-lookup"><span data-stu-id="5ceca-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="5ceca-163">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="5ceca-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5ceca-164">**enum**</span><span class="sxs-lookup"><span data-stu-id="5ceca-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="5ceca-165">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="5ceca-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="5ceca-166">**gestire**</span><span class="sxs-lookup"><span data-stu-id="5ceca-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="5ceca-167">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="5ceca-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="5ceca-168">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="5ceca-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="5ceca-169">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="5ceca-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="5ceca-170">**locale**</span><span class="sxs-lookup"><span data-stu-id="5ceca-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="5ceca-171">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="5ceca-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="5ceca-172">**out**</span><span class="sxs-lookup"><span data-stu-id="5ceca-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="5ceca-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="5ceca-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="5ceca-174">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="5ceca-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="5ceca-175">**string**</span><span class="sxs-lookup"><span data-stu-id="5ceca-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="5ceca-176">**struct**</span><span class="sxs-lookup"><span data-stu-id="5ceca-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="5ceca-177">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="5ceca-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="5ceca-178">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="5ceca-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="5ceca-179">**Unione**</span><span class="sxs-lookup"><span data-stu-id="5ceca-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="5ceca-180">**unico**</span><span class="sxs-lookup"><span data-stu-id="5ceca-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 