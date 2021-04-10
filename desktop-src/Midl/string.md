---
title: string (attributo)
description: L'attributo \ string \ indica che la matrice unidimensionale char, WCHAR \_ t, byte (o equivalente) o il puntatore a una matrice di questo tipo devono essere considerati come una stringa.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- attributo stringa MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963033"
---
# <a name="string-attribute"></a><span data-ttu-id="2ceed-104">string (attributo)</span><span class="sxs-lookup"><span data-stu-id="2ceed-104">string attribute</span></span>

<span data-ttu-id="2ceed-105">L' **\[ attributo \] stringa** indica che la matrice unidimensionale [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o il puntatore a tale matrice deve essere considerata come una stringa.</span><span class="sxs-lookup"><span data-stu-id="2ceed-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="2ceed-106">La stringa può anche essere una matrice (o un puntatore a una matrice) di costrutti i cui campi sono tutti di tipo **byte**.</span><span class="sxs-lookup"><span data-stu-id="2ceed-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="2ceed-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ceed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ceed-108">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2ceed-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-109">Specifica uno o più attributi che si applicano a un tipo.</span><span class="sxs-lookup"><span data-stu-id="2ceed-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="2ceed-110">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[ stringa \]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="2ceed-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="2ceed-111">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="2ceed-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-112">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="2ceed-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-113">Specifica un [tipo di base](midl-base-types.md), un tipo di [**struct**](struct.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="2ceed-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="2ceed-114">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="2ceed-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-115">*dichiaratore standard*</span><span class="sxs-lookup"><span data-stu-id="2ceed-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-116">Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore o un dichiaratore di matrice.</span><span class="sxs-lookup"><span data-stu-id="2ceed-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="2ceed-117">Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2ceed-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-118">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="2ceed-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-119">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="2ceed-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2ceed-120">Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2ceed-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="2ceed-121">Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="2ceed-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="2ceed-122">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ceed-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-123">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2ceed-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-124">Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="2ceed-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="2ceed-125">I due attributi di campo validi sono **\[** [**Max \_**](max-is.md) **\]** e **\[** [**size \_ è**](size-is.md) **\]** ; gli attributi di utilizzo **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**, l'attributo puntatore **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** e il **\[ \_ tipo \] di opzione** attribute Union.</span><span class="sxs-lookup"><span data-stu-id="2ceed-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="2ceed-126">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="2ceed-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-127">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2ceed-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-128">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="2ceed-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="2ceed-129">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="2ceed-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-130">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="2ceed-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-131">Specifica un dichiaratore di puntatore facoltativo a cui si applica l'attributo **\[ stringa \]** .</span><span class="sxs-lookup"><span data-stu-id="2ceed-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="2ceed-132">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="2ceed-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-133">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="2ceed-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-134">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="2ceed-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="2ceed-135">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="2ceed-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2ceed-136">È costituito da zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="2ceed-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="2ceed-137">Gli attributi di parametro possono assumere ed **\[ \] escludere** gli attributi direzionali. gli attributi **\[ \] di** campo **\[** [**Max \_ è**](max-is.md) **\]** e **\[** [**size \_ sono**](size-is.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="2ceed-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="2ceed-138">L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="2ceed-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="2ceed-139">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="2ceed-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ceed-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ceed-140">Remarks</span></span>

<span data-ttu-id="2ceed-141">Se l'attributo **\[ stringa \]** viene usato con una matrice i cui limiti vengono determinati in fase di esecuzione, è necessario specificare anche **\[ \_ \] una dimensione** oppure il valore **\[ Max \_ è \]** attributo, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="2ceed-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="2ceed-142">Impossibile utilizzare l'attributo **\[ stringa \]** con attributi che specificano l'intervallo di elementi trasmessi, ad esempio **\[ First \_ è \]**, **\[ Last \_ è \]** e **\[ length \_ è \]**.</span><span class="sxs-lookup"><span data-stu-id="2ceed-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="2ceed-143">Quando viene utilizzato su matrici multidimensionali, l'attributo **\[ stringa \]** viene applicato alla matrice più a destra.</span><span class="sxs-lookup"><span data-stu-id="2ceed-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="2ceed-144">Per definire una stringa calcolata, non usare l'attributo **\[ String \]** .</span><span class="sxs-lookup"><span data-stu-id="2ceed-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="2ceed-145">Utilizzare una matrice di caratteri o un puntatore basato su caratteri come il seguente:</span><span class="sxs-lookup"><span data-stu-id="2ceed-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="2ceed-146">L'attributo **\[ String \]** specifica che lo stub deve usare un metodo fornito dal linguaggio per determinare la lunghezza delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="2ceed-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="2ceed-147">Quando si dichiarano stringhe in C, è necessario allocare spazio per un carattere aggiuntivo che contrassegna la fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="2ceed-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="2ceed-148">Esempi</span><span class="sxs-lookup"><span data-stu-id="2ceed-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="2ceed-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2ceed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ceed-150">**matrici**</span><span class="sxs-lookup"><span data-stu-id="2ceed-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="2ceed-151">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="2ceed-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="2ceed-152">**callback**</span><span class="sxs-lookup"><span data-stu-id="2ceed-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="2ceed-153">**char**</span><span class="sxs-lookup"><span data-stu-id="2ceed-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="2ceed-154">**const**</span><span class="sxs-lookup"><span data-stu-id="2ceed-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="2ceed-155">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="2ceed-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="2ceed-156">**enum**</span><span class="sxs-lookup"><span data-stu-id="2ceed-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2ceed-157">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="2ceed-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="2ceed-158">**gestire**</span><span class="sxs-lookup"><span data-stu-id="2ceed-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="2ceed-159">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="2ceed-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2ceed-160">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="2ceed-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="2ceed-161">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="2ceed-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="2ceed-162">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="2ceed-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="2ceed-163">**locale**</span><span class="sxs-lookup"><span data-stu-id="2ceed-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2ceed-164">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="2ceed-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="2ceed-165">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="2ceed-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="2ceed-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="2ceed-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="2ceed-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="2ceed-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="2ceed-168">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="2ceed-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="2ceed-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="2ceed-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="2ceed-170">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="2ceed-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="2ceed-171">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="2ceed-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="2ceed-172">**Unione**</span><span class="sxs-lookup"><span data-stu-id="2ceed-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="2ceed-173">**unico**</span><span class="sxs-lookup"><span data-stu-id="2ceed-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="2ceed-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="2ceed-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 