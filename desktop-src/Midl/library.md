---
title: attribute Library
description: L'istruzione Library contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- attributo della libreria MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299788"
---
# <a name="library-attribute"></a><span data-ttu-id="746c8-104">attribute Library</span><span class="sxs-lookup"><span data-stu-id="746c8-104">library attribute</span></span>

<span data-ttu-id="746c8-105">L'istruzione **Library** contiene tutte le informazioni utilizzate dal compilatore MIDL per generare una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="746c8-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="746c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="746c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746c8-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="746c8-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="746c8-108">Specifica un numero di identificazione univoco universale per la libreria.</span><span class="sxs-lookup"><span data-stu-id="746c8-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="746c8-109">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="746c8-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="746c8-110">Specifica gli attributi aggiuntivi che si applicano all'intera istruzione della **libreria** .</span><span class="sxs-lookup"><span data-stu-id="746c8-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="746c8-111">Gli attributi consentiti includono **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**filelima**](helpfile.md), **\]** **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** e **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="746c8-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="746c8-112">*nome della libreria*</span><span class="sxs-lookup"><span data-stu-id="746c8-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="746c8-113">Nome con cui i componenti software fanno riferimento alla **libreria**.</span><span class="sxs-lookup"><span data-stu-id="746c8-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="746c8-114">*Library-Definition-Statements*</span><span class="sxs-lookup"><span data-stu-id="746c8-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="746c8-115">Una o più istruzioni MIDL che definiscono il contenuto della **libreria**.</span><span class="sxs-lookup"><span data-stu-id="746c8-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="746c8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="746c8-116">Remarks</span></span>

<span data-ttu-id="746c8-117">Le istruzioni all'interno del blocco di libreria possono usare elementi dichiarati all'interno o all'esterno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="746c8-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="746c8-118">Le istruzioni Library possono usare tali elementi come tipi di base, ereditando da tali elementi o semplicemente facendo riferimento a essi su una riga, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="746c8-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="746c8-119">Il compilatore MIDL creerà una libreria dei tipi che include le definizioni per ogni elemento all'interno del blocco Library, più le definizioni per tutti gli elementi definiti all'esterno e a cui viene fatto riferimento dall'interno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="746c8-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="746c8-120">Per informazioni sulla generazione di una libreria dei tipi e di stub e intestazioni proxy da un singolo file IDL, vedere [generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="746c8-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="746c8-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="746c8-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="746c8-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="746c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746c8-123">Contenuto di una libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="746c8-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="746c8-124">**controllo**</span><span class="sxs-lookup"><span data-stu-id="746c8-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="746c8-125">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="746c8-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="746c8-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="746c8-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="746c8-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="746c8-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="746c8-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="746c8-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="746c8-129">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="746c8-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="746c8-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="746c8-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="746c8-131">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="746c8-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="746c8-132">**limitato**</span><span class="sxs-lookup"><span data-stu-id="746c8-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="746c8-133">**Versione**</span><span class="sxs-lookup"><span data-stu-id="746c8-133">**version**</span></span>](version.md)
</dt> </dl>

 

 