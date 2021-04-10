---
title: switch_is (attributo)
description: Il parametro \ Switch \_ is \ attribute specifica l'espressione o l'identificatore che funge da discriminante di Unione che seleziona il membro di Unione.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- attributo switch_is MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955976"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="abe3c-104">Switch \_ è attributo</span><span class="sxs-lookup"><span data-stu-id="abe3c-104">switch\_is attribute</span></span>

<span data-ttu-id="abe3c-105">L' **\[ opzione \_ è \]** attribute specifica l'espressione o l'identificatore che funge da discriminante di Unione che seleziona il membro di Unione.</span><span class="sxs-lookup"><span data-stu-id="abe3c-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="abe3c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abe3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe3c-107">*struct-Tag*</span><span class="sxs-lookup"><span data-stu-id="abe3c-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-108">Specifica un tag facoltativo per una struttura.</span><span class="sxs-lookup"><span data-stu-id="abe3c-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-109">*Limited-expr*</span><span class="sxs-lookup"><span data-stu-id="abe3c-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-110">Specifica un'espressione del linguaggio C supportata da MIDL.</span><span class="sxs-lookup"><span data-stu-id="abe3c-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="abe3c-111">Sono supportate quasi tutte le espressioni in linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="abe3c-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="abe3c-112">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="abe3c-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="abe3c-113">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di pre-e post-incremento e di pre-e post-decremento.</span><span class="sxs-lookup"><span data-stu-id="abe3c-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-114">*Field-attr-List*</span><span class="sxs-lookup"><span data-stu-id="abe3c-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-115">Specifica zero o più attributi di campo che si applicano a un membro di Unione.</span><span class="sxs-lookup"><span data-stu-id="abe3c-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="abe3c-116">Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e per i membri che sono a loro volta Unions, il **\[** [**\_ tipo di opzione**](switch-type.md)dell'attributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="abe3c-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="abe3c-117">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="abe3c-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-118">*Union-Type-specifier*</span><span class="sxs-lookup"><span data-stu-id="abe3c-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-119">Specifica l'identificatore del tipo di [**Unione**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="abe3c-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="abe3c-120">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="abe3c-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-121">*dichiaratore e declarator-list*</span><span class="sxs-lookup"><span data-stu-id="abe3c-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-122">Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore e un dichiaratore di matrice.</span><span class="sxs-lookup"><span data-stu-id="abe3c-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="abe3c-123">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle unioni trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="abe3c-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="abe3c-124">Questi dichiaratori sono consentiti nelle unioni non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="abe3c-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="abe3c-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-126">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="abe3c-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="abe3c-127">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="abe3c-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-128">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="abe3c-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-129">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="abe3c-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="abe3c-130">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="abe3c-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-131">*puntatore-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="abe3c-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-132">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="abe3c-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="abe3c-133">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="abe3c-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-134">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="abe3c-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-135">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="abe3c-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="abe3c-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-137">Specifica zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="abe3c-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="abe3c-138">Gli attributi **\[ di \]** parametro possono attivare e **\[ \]** disattivare gli attributi direzionali, gli attributi di campo **\[ First \_ \]** sono, **\[ Last \_ \] è**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage.</span><span class="sxs-lookup"><span data-stu-id="abe3c-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="abe3c-139">L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="abe3c-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="abe3c-140">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="abe3c-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="abe3c-141">*tipo Unione*</span><span class="sxs-lookup"><span data-stu-id="abe3c-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="abe3c-142">Identifica l'identificatore del tipo di [**Unione**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="abe3c-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abe3c-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="abe3c-143">Remarks</span></span>

<span data-ttu-id="abe3c-144">Il discriminante associato all' **\[ opzione \_ è \]** l'attributo deve essere definito allo stesso livello logico dell'Unione:</span><span class="sxs-lookup"><span data-stu-id="abe3c-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="abe3c-145">Quando l'Unione è un parametro, il discriminante di Unione deve essere un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="abe3c-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="abe3c-146">Quando l'Unione è un campo di una struttura, discriminante deve essere un altro campo della stessa struttura.</span><span class="sxs-lookup"><span data-stu-id="abe3c-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="abe3c-147">La sequenza in una struttura o in un elenco di parametri di funzione non è significativa.</span><span class="sxs-lookup"><span data-stu-id="abe3c-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="abe3c-148">L'Unione può precedere o seguire discriminante.</span><span class="sxs-lookup"><span data-stu-id="abe3c-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="abe3c-149">L' **\[ opzione \_ è \]** attributo può essere visualizzata come attributo di campo o come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="abe3c-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="abe3c-150">Esempi</span><span class="sxs-lookup"><span data-stu-id="abe3c-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="abe3c-151">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="abe3c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe3c-152">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="abe3c-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="abe3c-153">**callback**</span><span class="sxs-lookup"><span data-stu-id="abe3c-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="abe3c-154">**const**</span><span class="sxs-lookup"><span data-stu-id="abe3c-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="abe3c-155">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="abe3c-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="abe3c-156">Unioni incapsulate</span><span class="sxs-lookup"><span data-stu-id="abe3c-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="abe3c-157">**enum**</span><span class="sxs-lookup"><span data-stu-id="abe3c-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="abe3c-158">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="abe3c-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="abe3c-159">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="abe3c-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="abe3c-160">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="abe3c-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="abe3c-161">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="abe3c-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="abe3c-162">**locale**</span><span class="sxs-lookup"><span data-stu-id="abe3c-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="abe3c-163">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="abe3c-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="abe3c-164">Unioni non incapsulate</span><span class="sxs-lookup"><span data-stu-id="abe3c-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="abe3c-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="abe3c-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="abe3c-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="abe3c-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="abe3c-167">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="abe3c-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="abe3c-168">**string**</span><span class="sxs-lookup"><span data-stu-id="abe3c-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="abe3c-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="abe3c-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="abe3c-170">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="abe3c-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="abe3c-171">**Unione**</span><span class="sxs-lookup"><span data-stu-id="abe3c-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="abe3c-172">**unico**</span><span class="sxs-lookup"><span data-stu-id="abe3c-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




