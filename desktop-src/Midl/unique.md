---
title: unique (attributo)
description: L'attributo \ Unique \ specifica un puntatore univoco.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- attributo univoco MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299620"
---
# <a name="unique-attribute"></a><span data-ttu-id="9e102-104">unique (attributo)</span><span class="sxs-lookup"><span data-stu-id="9e102-104">unique attribute</span></span>

<span data-ttu-id="9e102-105">L'attributo **\[ Unique \]** specifica un puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="9e102-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="9e102-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e102-107">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9e102-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-108">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="9e102-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="9e102-109">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[ univoco \]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9e102-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="9e102-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="9e102-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-111">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="9e102-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-112">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="9e102-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="9e102-113">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="9e102-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-114">*dichiaratore e declarator-list*</span><span class="sxs-lookup"><span data-stu-id="9e102-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-115">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="9e102-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="9e102-116">Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="9e102-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="9e102-117">Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="9e102-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="9e102-118">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9e102-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-119">*struct-or-Union-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="9e102-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-120">Specifica una [**struttura**](struct.md) MIDL o un dichiaratore di [**Unione**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="9e102-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-121">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9e102-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-122">Specifica zero o più attributi di campo che si applicano al membro della struttura, al membro di Unione o al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="9e102-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="9e102-123">Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e il **\[ \_ tipo \] di opzione** attribute Union.</span><span class="sxs-lookup"><span data-stu-id="9e102-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="9e102-124">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="9e102-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9e102-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-126">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="9e102-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="9e102-127">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="9e102-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-128">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="9e102-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-129">Specifica almeno un dichiaratore di puntatore a cui viene applicato l'attributo **\[ Unique \]** .</span><span class="sxs-lookup"><span data-stu-id="9e102-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="9e102-130">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="9e102-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e102-131">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="9e102-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-132">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="9e102-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="9e102-133">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9e102-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e102-134">È costituito da zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="9e102-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="9e102-135">Gli attributi **\[ di \]** parametro possono attivare e **\[ \]** disattivare gli attributi direzionali. gli attributi di campo **\[ First \_ \]** sono, **\[ Last \_ \] è**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **Unique** o [**ptr**](ptr.md)e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage.</span><span class="sxs-lookup"><span data-stu-id="9e102-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="9e102-136">L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="9e102-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="9e102-137">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="9e102-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e102-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e102-138">Remarks</span></span>

<span data-ttu-id="9e102-139">È possibile applicare gli attributi del puntatore come attributo di tipo; come attributo di campo che si applica a un membro di struttura, a un membro di Unione o a un parametro; o come attributo di funzione applicabile al tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="9e102-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="9e102-140">L'attributo pointer può essere visualizzato anche con la **\[** parola chiave [**\_ default del puntatore**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9e102-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="9e102-141">Un puntatore univoco presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e102-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="9e102-142">Il valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9e102-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="9e102-143">Può cambiare durante una chiamata da **null** a non **null**, da un valore **diverso da\*\*\*\*null** o da un valore non **null** a un altro.</span><span class="sxs-lookup"><span data-stu-id="9e102-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="9e102-144">Consente di allocare una nuova memoria nel client.</span><span class="sxs-lookup"><span data-stu-id="9e102-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="9e102-145">Quando il puntatore univoco passa da **null** a non **null**, i dati restituiti dal server vengono scritti in una nuova risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e102-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="9e102-146">Può usare la memoria esistente sul client senza allocare la nuova memoria.</span><span class="sxs-lookup"><span data-stu-id="9e102-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="9e102-147">Quando un puntatore univoco viene modificato durante una chiamata da un valore non **null** a un altro, si presuppone che il puntatore punti a un oggetto dati dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="9e102-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="9e102-148">I dati restituiti dal server vengono scritti nella risorsa di archiviazione esistente specificata dal valore del puntatore univoco prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="9e102-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="9e102-149">Può avere memoria orfana sul client.</span><span class="sxs-lookup"><span data-stu-id="9e102-149">Can orphan memory on the client.</span></span> <span data-ttu-id="9e102-150">La memoria a cui fa riferimento un puntatore univoco non **null** può non essere mai liberata se il puntatore univoco diventa **null** durante una chiamata e il client non dispone di un altro mezzo per dereferenziare l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e102-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="9e102-151">Non provoca l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="9e102-151">Does not cause aliasing.</span></span> <span data-ttu-id="9e102-152">Analogamente all'archiviazione a cui punta un puntatore di riferimento, non è possibile raggiungere lo spazio di archiviazione a cui punta un puntatore univoco da un altro nome nella funzione.</span><span class="sxs-lookup"><span data-stu-id="9e102-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="9e102-153">Gli stub chiamano le funzioni di gestione della memoria fornite dall'utente [**MIDL \_ User \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) e [**MIDL \_ User \_ Free**](/windows/desktop/Rpc/the-midl-user-free-function) per allocare e deallocare la memoria necessaria per i puntatori univoci e i relativi riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9e102-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="9e102-154">Ai puntatori univoci si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e102-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="9e102-155">Non è possibile applicare l'attributo **\[ Unique \]** ai parametri dell'handle di binding ( [**handle \_ t**](handle-t.md)) e ai parametri dell'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="9e102-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="9e102-156">Non è possibile applicare l'attributo **\[ Unique \]** ai parametri del puntatore di **\[** [](out-idl.md) **\]** primo livello solo out (parametri che hanno solo l'attributo **\[ out \]** Directional).</span><span class="sxs-lookup"><span data-stu-id="9e102-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="9e102-157">Per impostazione predefinita, i puntatori di primo livello negli elenchi di parametri sono **\[** [](ref.md) **\]** puntatori Ref.</span><span class="sxs-lookup"><span data-stu-id="9e102-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="9e102-158">Questo vale anche se l'interfaccia specifica il **puntatore \_ predefinito (univoco)**.</span><span class="sxs-lookup"><span data-stu-id="9e102-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="9e102-159">I parametri di primo livello negli elenchi di parametri devono essere specificati con l'attributo **\[ Unique \]** come puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="9e102-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="9e102-160">Non è possibile usare i puntatori univoci per descrivere le dimensioni di una matrice o di un ARM di Unione perché i puntatori univoci possono avere il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="9e102-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="9e102-161">Questa restrizione impedisce l'errore risultante se viene usato un valore **null** come dimensione della matrice o dimensione del ARM di Unione.</span><span class="sxs-lookup"><span data-stu-id="9e102-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="9e102-162">Esempi</span><span class="sxs-lookup"><span data-stu-id="9e102-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="9e102-163">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9e102-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e102-164">**matrici**</span><span class="sxs-lookup"><span data-stu-id="9e102-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="9e102-165">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="9e102-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="9e102-166">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="9e102-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e102-167">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="9e102-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="9e102-168">**callback**</span><span class="sxs-lookup"><span data-stu-id="9e102-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="9e102-169">**const**</span><span class="sxs-lookup"><span data-stu-id="9e102-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9e102-170">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="9e102-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="9e102-171">**enum**</span><span class="sxs-lookup"><span data-stu-id="9e102-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="9e102-172">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="9e102-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="9e102-173">**gestire**</span><span class="sxs-lookup"><span data-stu-id="9e102-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="9e102-174">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="9e102-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="9e102-175">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="9e102-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="9e102-176">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="9e102-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="9e102-177">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="9e102-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="9e102-178">**locale**</span><span class="sxs-lookup"><span data-stu-id="9e102-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="9e102-179">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="9e102-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="9e102-180">\_alloca utente \_ MIDL</span><span class="sxs-lookup"><span data-stu-id="9e102-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="9e102-181">\_utente MIDL \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="9e102-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="9e102-182">**out**</span><span class="sxs-lookup"><span data-stu-id="9e102-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="9e102-183">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="9e102-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="9e102-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="9e102-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="9e102-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="9e102-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="9e102-186">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="9e102-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="9e102-187">**string**</span><span class="sxs-lookup"><span data-stu-id="9e102-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9e102-188">**struct**</span><span class="sxs-lookup"><span data-stu-id="9e102-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="9e102-189">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="9e102-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="9e102-190">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="9e102-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="9e102-191">**Unione**</span><span class="sxs-lookup"><span data-stu-id="9e102-191">**union**</span></span>](union.md)
</dt> </dl>

 

 