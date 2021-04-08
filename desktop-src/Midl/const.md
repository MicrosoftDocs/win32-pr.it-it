---
title: attributo const
description: La parola chiave const modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- attributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724967"
---
# <a name="const-attribute"></a><span data-ttu-id="02fb4-104">attributo const</span><span class="sxs-lookup"><span data-stu-id="02fb4-104">const attribute</span></span>

<span data-ttu-id="02fb4-105">La parola chiave **const** modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.</span><span class="sxs-lookup"><span data-stu-id="02fb4-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="02fb4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02fb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02fb4-107">*tipo const*</span><span class="sxs-lookup"><span data-stu-id="02fb4-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-108">Specifica un Integer MIDL, un carattere, una stringa o un tipo booleano valido.</span><span class="sxs-lookup"><span data-stu-id="02fb4-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="02fb4-109">I tipi MIDL validi [**includono Small**](small.md), [**short**](short.md), [**Long**](long.md), [**char**](char-idl.md), **\* charÂ**, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tÂ \***, [**byte**](byte.md), **byteÂ \*** e [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="02fb4-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \***, [**wchar\_t**](wchar-t.md), **wchar\_tÂ \***, [**byte**](byte.md), **byteÂ \***, and [**voidÂ \***](void.md).</span></span> <span data-ttu-id="02fb4-110">I tipi integer e character possono essere [**firmati**](signed.md) o [**senza segno**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="02fb4-110">The integer and character types can be [**signed**](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="02fb4-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-112">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="02fb4-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="02fb4-113">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="02fb4-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-114">*const-espressione*</span><span class="sxs-lookup"><span data-stu-id="02fb4-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-115">Specifica un'espressione, un identificatore o una costante numerica o carattere appropriata per il tipo specificato: valori letterali integer costanti o espressioni integer costanti per le costanti Integer; Espressioni booleane che possono essere calcolate in fase di compilazione per i tipi [**booleani**](boolean.md) ; costanti a carattere singolo per i tipi [**char**](char-idl.md) ; e costanti di stringa per i tipi di **\[** [**stringa**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="02fb4-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="02fb4-116">Il [**tipo \* voidÂ**](void.md) può essere inizializzato solo su **null**.</span><span class="sxs-lookup"><span data-stu-id="02fb4-116">The [**voidÂ \***](void.md) type can be initialized only to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-117">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="02fb4-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-118">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="02fb4-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-119">*tipo di puntatore*</span><span class="sxs-lookup"><span data-stu-id="02fb4-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-120">Specifica un tipo di puntatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="02fb4-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-121">*dichiaratore e declarator-list*</span><span class="sxs-lookup"><span data-stu-id="02fb4-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-122">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="02fb4-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="02fb4-123">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="02fb4-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="02fb4-124">Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="02fb4-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="02fb4-125">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="02fb4-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-126">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="02fb4-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-127">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="02fb4-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="02fb4-128">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="02fb4-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-129">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="02fb4-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-130">Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="02fb4-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="02fb4-131">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="02fb4-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-132">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="02fb4-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-133">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="02fb4-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="02fb4-134">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C. Viene costruita dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore **const**.</span><span class="sxs-lookup"><span data-stu-id="02fb4-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the **\*** designator, modifiers such as **far**, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-135">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="02fb4-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-136">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="02fb4-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="02fb4-137">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="02fb4-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02fb4-138">Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="02fb4-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="02fb4-139">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="02fb4-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02fb4-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="02fb4-140">Remarks</span></span>

<span data-ttu-id="02fb4-141">MIDL consente di dichiarare tipi integer costanti, caratteri, stringa e booleani nel corpo dell'interfaccia del file IDL.</span><span class="sxs-lookup"><span data-stu-id="02fb4-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="02fb4-142">Le dichiarazioni di tipo **const** vengono riprodotte nel file di intestazione generato come direttive **\# define** .</span><span class="sxs-lookup"><span data-stu-id="02fb4-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="02fb4-143">I compilatori IDL DCE non supportano espressioni costanti.</span><span class="sxs-lookup"><span data-stu-id="02fb4-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="02fb4-144">Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="02fb4-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="02fb4-145">Una costante definita in precedenza può essere usata come valore assegnato di una costante successiva.</span><span class="sxs-lookup"><span data-stu-id="02fb4-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="02fb4-146">Il valore di un'espressione integrale costante viene convertito automaticamente nel rispettivo tipo integer in base alle regole di conversione C.</span><span class="sxs-lookup"><span data-stu-id="02fb4-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="02fb4-147">Il valore di una costante carattere deve essere un carattere ASCII racchiuso tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="02fb4-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="02fb4-148">Quando la costante carattere è il carattere con virgolette singole ('), il carattere barra rovesciata ( \) deve precedere il carattere con virgolette singole, come in \\ '.</span><span class="sxs-lookup"><span data-stu-id="02fb4-148">When the character constant is the single-quote character itself ('), the backslash character (\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="02fb4-149">Il valore di una costante stringa di caratteri deve essere una stringa racchiusa tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="02fb4-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="02fb4-150">All'interno di una stringa, il carattere barra rovesciata ( **\\** ) deve precedere un carattere virgolette doppie ( **"** ), come in **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="02fb4-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="02fb4-151">All'interno di una stringa, il carattere barra rovesciata ( **\\** ) rappresenta un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="02fb4-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="02fb4-152">Le costanti di stringa possono contenere fino a 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="02fb4-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="02fb4-153">Il valore **null** è l'unico valore valido per le costanti di tipo [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="02fb4-153">The value **NULL** is the only valid value for constants of type [**voidÂ \***](void.md).</span></span> <span data-ttu-id="02fb4-154">Qualsiasi attributo associato alla Dichiarazione **const** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="02fb4-154">Any attributes associated with the **const** declaration are ignored.</span></span>

<span data-ttu-id="02fb4-155">Il compilatore MIDL non controlla la presenza di errori di intervallo nell'inizializzazione **const** .</span><span class="sxs-lookup"><span data-stu-id="02fb4-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="02fb4-156">Ad esempio, quando si specifica "const short x = 0xFFFFFFFF;", il compilatore MIDL non segnala un errore e l'inizializzatore viene riprodotto nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="02fb4-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="02fb4-157">Esempi</span><span class="sxs-lookup"><span data-stu-id="02fb4-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="02fb4-158">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02fb4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02fb4-159">**matrici**</span><span class="sxs-lookup"><span data-stu-id="02fb4-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="02fb4-160">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="02fb4-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="02fb4-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="02fb4-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="02fb4-162">**byte**</span><span class="sxs-lookup"><span data-stu-id="02fb4-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="02fb4-163">**callback**</span><span class="sxs-lookup"><span data-stu-id="02fb4-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="02fb4-164">**char**</span><span class="sxs-lookup"><span data-stu-id="02fb4-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="02fb4-165">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="02fb4-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="02fb4-166">**enum**</span><span class="sxs-lookup"><span data-stu-id="02fb4-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="02fb4-167">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="02fb4-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="02fb4-168">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="02fb4-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="02fb4-169">**locale**</span><span class="sxs-lookup"><span data-stu-id="02fb4-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="02fb4-170">**long**</span><span class="sxs-lookup"><span data-stu-id="02fb4-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="02fb4-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="02fb4-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="02fb4-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="02fb4-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="02fb4-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="02fb4-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="02fb4-174">**short**</span><span class="sxs-lookup"><span data-stu-id="02fb4-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="02fb4-175">**con segno**</span><span class="sxs-lookup"><span data-stu-id="02fb4-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="02fb4-176">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="02fb4-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="02fb4-177">**string**</span><span class="sxs-lookup"><span data-stu-id="02fb4-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="02fb4-178">**struct**</span><span class="sxs-lookup"><span data-stu-id="02fb4-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="02fb4-179">**Unione**</span><span class="sxs-lookup"><span data-stu-id="02fb4-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="02fb4-180">**unico**</span><span class="sxs-lookup"><span data-stu-id="02fb4-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="02fb4-181">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="02fb4-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="02fb4-182">**void**</span><span class="sxs-lookup"><span data-stu-id="02fb4-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="02fb4-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="02fb4-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 