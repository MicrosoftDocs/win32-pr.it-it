---
title: Arrays (attributo)
description: Le matrici sono raccolte omogenee di dati a cui si accede tramite un indice o un numero di elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- Arrays attribute MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299097"
---
# <a name="arrays-attribute"></a><span data-ttu-id="898b0-104">Arrays (attributo)</span><span class="sxs-lookup"><span data-stu-id="898b0-104">arrays attribute</span></span>

<span data-ttu-id="898b0-105">Le matrici sono raccolte omogenee di dati a cui si accede tramite un indice o un numero di elemento.</span><span class="sxs-lookup"><span data-stu-id="898b0-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="898b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="898b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="898b0-107">*tipo-attr-List*</span><span class="sxs-lookup"><span data-stu-id="898b0-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-108">Specifica zero o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="898b0-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="898b0-109">Gli attributi di tipo validi includono [**\[ \] handle**](handle.md), [**\[ \_ \] tipo di commutione**](switch-type.md), [**\[ trasmissione \_ come \]**](transmit-as.md); [**\[ riferimento \]**](ref.md)all'attributo del puntatore, [**\[ univoco \]**](unique.md)o [**\[ ptr \]**](ptr.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md), la [**\[ stringa \]**](string.md)e l' [**\[ Ignore \]**](ignore.md)degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="898b0-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="898b0-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="898b0-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-111">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="898b0-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-112">Specifica l'identificatore del tipo, il tipo di base, lo [**struct**](struct.md), l' [**Unione**](union.md)o il tipo [**enum**](enum.md) .</span><span class="sxs-lookup"><span data-stu-id="898b0-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="898b0-113">La specifica del tipo può includere una specifica di archiviazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="898b0-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-114">*puntatore-decl*</span><span class="sxs-lookup"><span data-stu-id="898b0-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-115">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="898b0-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="898b0-116">Un dichiaratore di puntatore è lo stesso del dichiaratore del puntatore utilizzato in C, costruito dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="898b0-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="898b0-117">*dichiaratore di matrici*</span><span class="sxs-lookup"><span data-stu-id="898b0-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-118">Specifica il nome della matrice, seguito da uno dei costrutti seguenti per ogni dimensione della matrice: "**\[ \]**", " **\[\*\]** ", "**\[ ***Cost1*** \]**" o "**\[ ***lower...*** Upper \]**"dove *Lower* e *Upper* sono valori costanti che rappresentano i limiti inferiore e superiore.</span><span class="sxs-lookup"><span data-stu-id="898b0-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="898b0-119">La costante *inferiore* deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="898b0-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-120">*tag*</span><span class="sxs-lookup"><span data-stu-id="898b0-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-121">Specifica un tag facoltativo per la struttura o l'Unione.</span><span class="sxs-lookup"><span data-stu-id="898b0-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-122">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="898b0-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-123">Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="898b0-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="898b0-124">Gli attributi di campo validi includono [**\[ First \_ è \]**](first-is.md), [**\[ Last \_ è \]**](last-is.md), [**\[ length \_ \] is**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md); the usage Attributes [**\[ String \]**](string.md), and [**\[ Ignore \]**](ignore.md); The Pointer Attributes [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md), [**\[ ptr \]**](ptr.md)e The Union Attribute [**\[ Switch \_ Type \]**](switch-type.md).</span><span class="sxs-lookup"><span data-stu-id="898b0-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="898b0-125">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="898b0-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="898b0-126">Si noti che gli attributi elencati sopra, **\[ First \_ \]** sono, **\[ Last \_ is \]** e [**\[ Ignore \]**](ignore.md) non sono validi per le unioni.</span><span class="sxs-lookup"><span data-stu-id="898b0-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-127">*espressione limitata*</span><span class="sxs-lookup"><span data-stu-id="898b0-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-128">Specifica un'espressione del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="898b0-128">Specifies a C-language expression.</span></span> <span data-ttu-id="898b0-129">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="898b0-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="898b0-130">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="898b0-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-131">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="898b0-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-132">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="898b0-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="898b0-133">Gli attributi di funzione validi sono [**\[ \] callback**](callback.md), [**\[ \] local**](local.md), l'attributo Pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md)e la [**\[ stringa \]**](string.md)degli attributi di utilizzo e l' [**\[ \_ handle \] di contesto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="898b0-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="898b0-134">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="898b0-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-135">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="898b0-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="898b0-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="898b0-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="898b0-137">Specifica gli attributi direzionali e uno o più attributi di campo facoltativi che si applicano al parametro di matrice.</span><span class="sxs-lookup"><span data-stu-id="898b0-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="898b0-138">Gli attributi di campo validi includono [**\[ Max \_ è \]**](max-is.md), [**\[ size \_ \] è**](size-is.md), [**\[ length \_ è \]**](length-is.md), [**\[ First \_ è \]**](first-is.md)e [**\[ Last \_ è \]**](last-is.md).</span><span class="sxs-lookup"><span data-stu-id="898b0-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="898b0-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="898b0-139">Remarks</span></span>

<span data-ttu-id="898b0-140">Le matrici in MIDL usano uno stile simile a, ma non esattamente come C e C++.</span><span class="sxs-lookup"><span data-stu-id="898b0-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="898b0-141">Per altre informazioni, vedere [matrici MIDL](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="898b0-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="898b0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="898b0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="898b0-143">**callback**</span><span class="sxs-lookup"><span data-stu-id="898b0-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="898b0-144">**const**</span><span class="sxs-lookup"><span data-stu-id="898b0-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="898b0-145">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="898b0-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="898b0-146">**enum**</span><span class="sxs-lookup"><span data-stu-id="898b0-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="898b0-147">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="898b0-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="898b0-148">**gestire**</span><span class="sxs-lookup"><span data-stu-id="898b0-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="898b0-149">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="898b0-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="898b0-150">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="898b0-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="898b0-151">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="898b0-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="898b0-152">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="898b0-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="898b0-153">**locale**</span><span class="sxs-lookup"><span data-stu-id="898b0-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="898b0-154">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="898b0-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="898b0-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="898b0-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="898b0-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="898b0-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="898b0-157">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="898b0-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="898b0-158">**string**</span><span class="sxs-lookup"><span data-stu-id="898b0-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="898b0-159">**struct**</span><span class="sxs-lookup"><span data-stu-id="898b0-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="898b0-160">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="898b0-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="898b0-161">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="898b0-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="898b0-162">**Unione**</span><span class="sxs-lookup"><span data-stu-id="898b0-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="898b0-163">**unico**</span><span class="sxs-lookup"><span data-stu-id="898b0-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




