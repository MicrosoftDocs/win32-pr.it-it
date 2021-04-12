---
title: ptr (attributo)
description: L'attributo \ PTR \ designa un puntatore come puntatore completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- attributo MIDL PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337030"
---
# <a name="ptr-attribute"></a><span data-ttu-id="79792-104">ptr (attributo)</span><span class="sxs-lookup"><span data-stu-id="79792-104">ptr attribute</span></span>

<span data-ttu-id="79792-105">L'attributo **\[ ptr \]** designa un puntatore come puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="79792-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="79792-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79792-107">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="79792-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-108">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="79792-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="79792-109">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md)o **\[ \] ptr** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="79792-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="79792-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="79792-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="79792-111">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="79792-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-112">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="79792-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="79792-113">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="79792-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="79792-114">*dichiaratore standard*</span><span class="sxs-lookup"><span data-stu-id="79792-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-115">Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice.</span><span class="sxs-lookup"><span data-stu-id="79792-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="79792-116">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="79792-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="79792-117">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="79792-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-118">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="79792-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="79792-119">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="79792-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="79792-120">Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="79792-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="79792-121">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="79792-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="79792-122">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="79792-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-123">Specifica zero o più attributi di campo che si applicano al membro della struttura o dell'Unione o al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="79792-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="79792-124">Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ \] ptr** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="79792-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="79792-125">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="79792-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="79792-126">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="79792-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-127">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="79792-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="79792-128">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ ptr \]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="79792-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="79792-129">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="79792-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-130">Specifica almeno un dichiaratore di puntatore a cui si applica l'attributo **\[ ptr \]** .</span><span class="sxs-lookup"><span data-stu-id="79792-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="79792-131">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="79792-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="79792-132">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="79792-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-133">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="79792-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="79792-134">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="79792-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79792-135">È costituito da zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="79792-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="79792-136">Gli attributi [**di**](in.md) parametro possono assumere ed [**estrarre**](out-idl.md)gli attributi direzionali; gli attributi di [**campo \_ First**](first-is.md)sono [**, Last \_ è**](last-is.md), [**length \_ is**](length-is.md), [**Max \_ is**](max-is.md), [**size \_ is**](size-is.md)e [**Switch \_ Type**](switch-type.md), l'attributo Pointer [**ref**](ref.md), [**Unique**](unique.md)o **\[ ptr \]** e la [**stringa**](string.md)e l' [**\_ handle di contesto**](context-handle.md) degli attributi Usage.</span><span class="sxs-lookup"><span data-stu-id="79792-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="79792-137">L'attributo Usage [**Ignore**](ignore.md) non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="79792-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="79792-138">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="79792-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79792-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="79792-139">Remarks</span></span>

<span data-ttu-id="79792-140">Il puntatore completo definito dall'attributo **\[ ptr \]** si avvicina alla funzionalità completa del puntatore del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="79792-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="79792-141">Il puntatore completo può avere valore **null** e può cambiare durante la chiamata da **null** a non **null**.</span><span class="sxs-lookup"><span data-stu-id="79792-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="79792-142">Lo spazio di archiviazione a cui puntano i puntatori completi può essere raggiunto da altri nomi nell'applicazione che supportano gli alias e i cicli.</span><span class="sxs-lookup"><span data-stu-id="79792-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="79792-143">Questa funzionalità richiede un sovraccarico maggiore durante una chiamata di procedura remota per identificare i dati a cui fa riferimento il puntatore, determinare se il valore è **null** e per individuare se due puntatori puntano agli stessi dati.</span><span class="sxs-lookup"><span data-stu-id="79792-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="79792-144">USA puntatori completi per:</span><span class="sxs-lookup"><span data-stu-id="79792-144">Use full pointers for:</span></span>

-   <span data-ttu-id="79792-145">Valori restituiti remoti.</span><span class="sxs-lookup"><span data-stu-id="79792-145">Remote return values.</span></span>
-   <span data-ttu-id="79792-146">Puntatori doppi, quando la dimensione di un parametro di output non è nota.</span><span class="sxs-lookup"><span data-stu-id="79792-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="79792-147">Puntatori **null** .</span><span class="sxs-lookup"><span data-stu-id="79792-147">**NULL** pointers.</span></span>

<span data-ttu-id="79792-148">I puntatori Full (e Unique) non possono essere usati per descrivere le dimensioni di una matrice o di un'Unione, perché questi puntatori possono avere il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="79792-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="79792-149">Questa restrizione di MIDL impedisce un errore che può verificarsi quando viene utilizzato un valore **null** come dimensione.</span><span class="sxs-lookup"><span data-stu-id="79792-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="79792-150">Si presuppone che il riferimento e i puntatori univoci non causino l'aliasing dei dati.</span><span class="sxs-lookup"><span data-stu-id="79792-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="79792-151">Un grafico diretto ottenuto iniziando da un puntatore univoco o di riferimento e che segue solo puntatori univoci o di riferimento non contiene né riconvergenza né cicli.</span><span class="sxs-lookup"><span data-stu-id="79792-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="79792-152">Per evitare alias, è necessario ottenere tutti i valori di puntatore da un puntatore di input della stessa classe di puntatore.</span><span class="sxs-lookup"><span data-stu-id="79792-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="79792-153">Se più di un puntatore punta alla stessa posizione di memoria, tutti i puntatori devono essere puntatori completi.</span><span class="sxs-lookup"><span data-stu-id="79792-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="79792-154">In alcuni casi, i puntatori completi e univoci possono essere misti.</span><span class="sxs-lookup"><span data-stu-id="79792-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="79792-155">A un puntatore completo è possibile assegnare il valore di un puntatore univoco, purché l'assegnazione non violi le restrizioni relative alla modifica del valore di un puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="79792-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="79792-156">Tuttavia, quando si assegna un puntatore univoco al valore di un puntatore completo, è possibile che si verifichi l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="79792-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="79792-157">La combinazione di puntatori completi e univoci può causare l'aliasing, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="79792-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="79792-158">Sebbene "t->left" e "t->Right" puntino a posizioni di memoria univoche, "t->Left->pData" e "t->right->di pData" sono con alias.</span><span class="sxs-lookup"><span data-stu-id="79792-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="79792-159">Per questo motivo, gli algoritmi di supporto degli alias devono seguire tutti i puntatori (inclusi i puntatori univoci e di riferimento) che potrebbero raggiungere un puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="79792-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="79792-160">Esempi</span><span class="sxs-lookup"><span data-stu-id="79792-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="79792-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="79792-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79792-162">**matrici**</span><span class="sxs-lookup"><span data-stu-id="79792-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="79792-163">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="79792-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="79792-164">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="79792-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="79792-165">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="79792-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="79792-166">**callback**</span><span class="sxs-lookup"><span data-stu-id="79792-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="79792-167">**const**</span><span class="sxs-lookup"><span data-stu-id="79792-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="79792-168">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="79792-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="79792-169">**enum**</span><span class="sxs-lookup"><span data-stu-id="79792-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="79792-170">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="79792-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="79792-171">**gestire**</span><span class="sxs-lookup"><span data-stu-id="79792-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="79792-172">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="79792-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="79792-173">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="79792-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="79792-174">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="79792-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="79792-175">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="79792-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="79792-176">**locale**</span><span class="sxs-lookup"><span data-stu-id="79792-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="79792-177">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="79792-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="79792-178">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="79792-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="79792-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="79792-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="79792-180">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="79792-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="79792-181">**string**</span><span class="sxs-lookup"><span data-stu-id="79792-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="79792-182">**struct**</span><span class="sxs-lookup"><span data-stu-id="79792-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="79792-183">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="79792-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="79792-184">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="79792-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="79792-185">**Unione**</span><span class="sxs-lookup"><span data-stu-id="79792-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="79792-186">**unico**</span><span class="sxs-lookup"><span data-stu-id="79792-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 