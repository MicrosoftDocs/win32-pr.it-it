---
title: attributo module
description: L'istruzione Module definisce un gruppo di funzioni, in genere un set di punti di ingresso della DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- attributo del modulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337134"
---
# <a name="module-attribute"></a><span data-ttu-id="0775c-104">attributo module</span><span class="sxs-lookup"><span data-stu-id="0775c-104">module attribute</span></span>

<span data-ttu-id="0775c-105">L'istruzione **Module** definisce un gruppo di funzioni, in genere un set di punti di ingresso della dll.</span><span class="sxs-lookup"><span data-stu-id="0775c-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="0775c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0775c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0775c-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="0775c-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0775c-108">Gli \[ attributi [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**helpstring**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] e \[ [**dllname**](dllname-str-.md) \] sono accettati prima di un'istruzione **Module** .</span><span class="sxs-lookup"><span data-stu-id="0775c-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="0775c-109">Per ulteriori informazioni sugli attributi accettati prima della definizione di un modulo, vedere [descrizioni](/previous-versions/windows/desktop/automat/attribute-descriptions)degli attributi nel manuale di automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="0775c-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="0775c-110">L' \[ attributo **dllname** \] è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0775c-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="0775c-111">Se l' \[  \] attributo uuid viene omesso, il modulo non viene specificato in modo univoco nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0775c-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="0775c-112">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="0775c-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="0775c-113">Nome del modulo.</span><span class="sxs-lookup"><span data-stu-id="0775c-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="0775c-114">*elemento element*</span><span class="sxs-lookup"><span data-stu-id="0775c-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="0775c-115">Elenco di definizioni di costanti e prototipi di funzione per ogni funzione nella DLL.</span><span class="sxs-lookup"><span data-stu-id="0775c-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="0775c-116">Un numero qualsiasi di definizioni di funzione può essere visualizzato nell'elenco di funzioni.</span><span class="sxs-lookup"><span data-stu-id="0775c-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="0775c-117">Una funzione nell'elenco di funzioni ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="0775c-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="0775c-118">\[*attributi* \] di *returnType* \[ funcname della convenzione di *chiamata* \] (*params*);</span><span class="sxs-lookup"><span data-stu-id="0775c-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="0775c-119">\[*attributi* \] di [**const**](const.md) constantType *const*  =  *ConstVal*;</span><span class="sxs-lookup"><span data-stu-id="0775c-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="0775c-120">\[ [](helpstring.md) \] \[ [](helpcontext.md) \] Per un [**const**](const.md)sono accettati solo gli attributi helpstring e HelpContext.</span><span class="sxs-lookup"><span data-stu-id="0775c-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="0775c-121">Gli attributi seguenti sono accettati in una funzione in un modulo: \[ [**helpstring**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] e \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="0775c-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="0775c-122">Se \[  \] viene specificato vararg, l'ultimo parametro deve essere una matrice sicura di tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="0775c-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="0775c-123">La convenzione di chiamata facoltativa può essere uno dei \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl o \_ \_ stdcall/ \_ stdcall/stdcall.</span><span class="sxs-lookup"><span data-stu-id="0775c-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="0775c-124">Il *tipo della convenzione di chiamata paramName* può includere fino a due caratteri di sottolineatura iniziali.</span><span class="sxs-lookup"><span data-stu-id="0775c-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="0775c-125">L'elenco di parametri è un elenco delimitato da virgole di:</span><span class="sxs-lookup"><span data-stu-id="0775c-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="0775c-126">\[*attributi*\]</span><span class="sxs-lookup"><span data-stu-id="0775c-126">\[*attributes*\]</span></span>

<span data-ttu-id="0775c-127">Il tipo può essere qualsiasi tipo dichiarato in precedenza o tipo incorporato, un puntatore a qualsiasi tipo o un puntatore a un tipo incorporato.</span><span class="sxs-lookup"><span data-stu-id="0775c-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="0775c-128">Gli attributi nei parametri sono:</span><span class="sxs-lookup"><span data-stu-id="0775c-128">Attributes on parameters are:</span></span>

<span data-ttu-id="0775c-129">\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**facoltativo**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="0775c-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="0775c-130">Se \[ [](optional.md) \] si utilizza facoltativo, i tipi di tali parametri devono essere **Variant** o **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="0775c-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0775c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="0775c-131">Remarks</span></span>

<span data-ttu-id="0775c-132">L'output del file di intestazione (. h) per i moduli è costituito da una serie di prototipi di funzione.</span><span class="sxs-lookup"><span data-stu-id="0775c-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="0775c-133">La parola chiave **Module** e le parentesi circostanti vengono rimosse dall'output del file di intestazione (. h), ma prima dei prototipi viene inserito un commento (// **Module** *ModuleName*).</span><span class="sxs-lookup"><span data-stu-id="0775c-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="0775c-134">La parola chiave **extern** viene inserita prima delle dichiarazioni.</span><span class="sxs-lookup"><span data-stu-id="0775c-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="0775c-135">Esempi</span><span class="sxs-lookup"><span data-stu-id="0775c-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="0775c-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0775c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0775c-137">**const**</span><span class="sxs-lookup"><span data-stu-id="0775c-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0775c-138">Contenuto di una libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0775c-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="0775c-139">**DllName**</span><span class="sxs-lookup"><span data-stu-id="0775c-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="0775c-140">**voce**</span><span class="sxs-lookup"><span data-stu-id="0775c-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="0775c-141">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="0775c-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0775c-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="0775c-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="0775c-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="0775c-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="0775c-144">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="0775c-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="0775c-145">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="0775c-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0775c-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="0775c-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="0775c-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="0775c-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="0775c-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="0775c-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="0775c-149">**string**</span><span class="sxs-lookup"><span data-stu-id="0775c-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="0775c-150">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="0775c-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="0775c-151">**uuid**</span><span class="sxs-lookup"><span data-stu-id="0775c-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="0775c-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="0775c-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="0775c-153">**Versione**</span><span class="sxs-lookup"><span data-stu-id="0775c-153">**version**</span></span>](version.md)
</dt> </dl>

 

 