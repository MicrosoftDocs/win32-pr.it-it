---
title: Annota attributo
description: L'attributo \ annotate \ consente di specificare una stringa di annotazione SAL per il metodo, il parametro o il campo della struttura specificato.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- Annota attributo MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732087"
---
# <a name="annotate-attribute"></a><span data-ttu-id="781eb-104">Annota attributo</span><span class="sxs-lookup"><span data-stu-id="781eb-104">annotate attribute</span></span>

<span data-ttu-id="781eb-105">L'attributo annotate consente di specificare una stringa di annotazione SAL per il metodo, il parametro o il campo della struttura specificato. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="781eb-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="781eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="781eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="781eb-107">*string*</span><span class="sxs-lookup"><span data-stu-id="781eb-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-108">Stringa di annotazione SAL specificata.</span><span class="sxs-lookup"><span data-stu-id="781eb-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-109">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="781eb-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-110">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="781eb-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="781eb-111">Gli attributi di funzione validi includono [**\[ \] callback**](callback.md), gli attributi del puntatore [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ \] ptr**](ptr.md)e la [**\[ stringa \]**](string.md)degli attributi di utilizzo, [**\[ Ignore \]**](ignore.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="781eb-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="781eb-112">Più attributi devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="781eb-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-113">*Function-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="781eb-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-114">Specifica l'identificatore di tipo, il nome della funzione e l'elenco di parametri per la funzione.</span><span class="sxs-lookup"><span data-stu-id="781eb-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-115">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="781eb-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-116">Specifica un **\_ tipo di base**, uno [**\[ struct \]**](struct.md), un' [**Unione**](union.md)o un tipo [**\[ enum \]**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="781eb-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="781eb-117">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="781eb-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-118">*puntatore-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="781eb-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-119">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="781eb-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="781eb-120">Un dichiaratore di puntatore è lo stesso di un dichiaratore di puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**\[ const \]**](const.md).</span><span class="sxs-lookup"><span data-stu-id="781eb-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="781eb-121">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="781eb-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-122">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="781eb-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-123">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="781eb-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-124">Specifica zero o più attributi appropriati per il tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="781eb-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="781eb-125">Gli attributi dei parametri con l'attributo in possono anche assumere l' [**\[ attributo \] Directional; gli**](out-idl.md)attributi [**\[ \] di**](in.md) campo [**\[ First \_ \] sono**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)e [**\[ Switch \_ Type \]**](switch-type.md); gli attributi Pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); e la [**\[ stringa \]**](string.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md) degli attributi Usage.</span><span class="sxs-lookup"><span data-stu-id="781eb-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="781eb-126">L'attributo Usage [**\[ Ignore \]**](ignore.md) non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="781eb-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="781eb-127">Più attributi devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="781eb-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="781eb-128">*dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="781eb-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="781eb-129">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="781eb-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="781eb-130">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**\[ \] matrici**](../rpc/arrays.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="781eb-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="781eb-131">Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="781eb-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="781eb-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="781eb-132">Remarks</span></span>

<span data-ttu-id="781eb-133">L'attributo **\[ annotate \]** consente di eseguire l'override delle annotazioni SAL generate da MIDL o di aggiungerle in posizioni in cui MIDL non genera in modo esplicito un'annotazione.</span><span class="sxs-lookup"><span data-stu-id="781eb-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="781eb-134">Se [**/Sal**](-sal.md) non è specificato nella riga di comando, questo attributo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="781eb-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="781eb-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="781eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781eb-136">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="781eb-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="781eb-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="781eb-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="781eb-138">**/SAL \_ locale**</span><span class="sxs-lookup"><span data-stu-id="781eb-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 