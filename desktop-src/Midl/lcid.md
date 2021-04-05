---
title: attributo LCID
description: L'attributo \ LCID \ specifica un identificatore delle impostazioni locali e Abilita il supporto del compilatore MIDL specifico delle impostazioni locali.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- attributo LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725095"
---
# <a name="lcid-attribute"></a><span data-ttu-id="9837e-104">attributo LCID</span><span class="sxs-lookup"><span data-stu-id="9837e-104">lcid attribute</span></span>

<span data-ttu-id="9837e-105">L'attributo **\[ LCID \]** specifica un identificatore delle impostazioni locali e Abilita il supporto del compilatore MIDL specifico delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="9837e-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="9837e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9837e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9837e-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="9837e-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-108">Specifica un numero di identificazione univoco universale per la [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="9837e-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="9837e-109">*localeID*</span><span class="sxs-lookup"><span data-stu-id="9837e-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-110">Specifica l'identificatore delle impostazioni locali a 32 bit utilizzato nel supporto della lingua nazionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="9837e-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="9837e-111">In genere l'identificatore delle impostazioni locali viene specificato in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="9837e-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="9837e-112">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9837e-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-113">Zero o più attributi da applicare alla [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="9837e-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="9837e-114">*nome della libreria*</span><span class="sxs-lookup"><span data-stu-id="9837e-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-115">Nome con cui i componenti software fanno riferimento alla [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="9837e-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="9837e-116">*Library-Definition-Statements*</span><span class="sxs-lookup"><span data-stu-id="9837e-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-117">Una o più istruzioni MIDL che definiscono il contenuto della [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="9837e-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="9837e-118">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="9837e-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-119">Specifica il nome della funzione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="9837e-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="9837e-120">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9837e-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-121">Zero o più attributi MIDL che verranno applicati al parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="9837e-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9837e-122">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="9837e-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9837e-123">Specifica il nome del parametro nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="9837e-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9837e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9837e-124">Remarks</span></span>

<span data-ttu-id="9837e-125">La sintassi **\[ \] LCID** presenta due forme diverse. l'effetto dell'attributo dipende dalla sintassi utilizzata, ovvero dalla sintassi dell'istruzione [**Library**](library.md) o dalla sintassi dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9837e-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="9837e-126">Quando viene applicato all'istruzione [**Library**](library.md) , insieme a un argomento LocaleID, come illustrato nel primo esempio, l'attributo **\[ LCID \]** identifica le impostazioni locali per una libreria dei tipi o per un argomento della funzione e consente di utilizzare caratteri internazionali all'interno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="9837e-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="9837e-127">A partire dalla versione 3.01.75 del compilatore MIDL, l'identificatore delle impostazioni locali fornito da questo attributo non solo decora la libreria dei tipi risultante, ma modifica effettivamente il comportamento del compilatore.</span><span class="sxs-lookup"><span data-stu-id="9837e-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="9837e-128">All'interno di un'istruzione [**Library**](library.md) , dal punto in cui viene usato l'attributo **\[ LCID \]** , MIDL accetterà l'input localizzato in base alle impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="9837e-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="9837e-129">In particolare, è disponibile il supporto completo per le lingue asiatiche come il giapponese, il cinese e il coreano (supporto completo DBCS).</span><span class="sxs-lookup"><span data-stu-id="9837e-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="9837e-130">Le funzionalità supportate dalla localizzazione sono: commenti, stringhe, HelpStrings e identificatori.</span><span class="sxs-lookup"><span data-stu-id="9837e-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="9837e-131">Usare l'opzione del compilatore [**/LCID**](-lcid.md) per fare in modo che questo supporto per la localizzazione sia disponibile per l'intero file di input, inclusi il nome file e il percorso della directory, anziché solo all'interno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="9837e-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="9837e-132">Quando viene applicato a un parametro, l'attributo **\[ LCID \]** consente di passare un identificatore delle impostazioni locali a una funzione, come illustrato nel secondo esempio.</span><span class="sxs-lookup"><span data-stu-id="9837e-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="9837e-133">Ai parametri **\[ LCID \]** si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9837e-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="9837e-134">Una funzione può avere al massimo un parametro **\[ LCID \]** .</span><span class="sxs-lookup"><span data-stu-id="9837e-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="9837e-135">Il tipo di dati del parametro deve essere [**Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="9837e-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="9837e-136">La direzione del parametro deve essere solo **\[** [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9837e-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="9837e-137">Il parametro **\[ LCID \]** deve seguire tutti gli altri parametri, ad eccezione di un **\[** parametro [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9837e-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="9837e-138">Non è possibile applicare l'attributo **\[ LCID \]** a un parametro [**Dispatch**](dispinterface.md) o [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="9837e-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="9837e-139">Esempi</span><span class="sxs-lookup"><span data-stu-id="9837e-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="9837e-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9837e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9837e-141">**coclass**</span><span class="sxs-lookup"><span data-stu-id="9837e-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="9837e-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="9837e-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="9837e-143">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="9837e-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="9837e-144">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="9837e-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="9837e-145">**libreria**</span><span class="sxs-lookup"><span data-stu-id="9837e-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="9837e-146">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="9837e-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9837e-147">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="9837e-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9837e-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="9837e-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 