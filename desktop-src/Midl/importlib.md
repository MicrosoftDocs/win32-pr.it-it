---
title: importlib (attributo)
description: La direttiva \ importlib \ rende disponibili i tipi già compilati in un'altra libreria dei tipi per la libreria dei tipi in fase di creazione.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- attributo MIDL di importlib
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472766"
---
# <a name="importlib-attribute"></a><span data-ttu-id="b328e-104">importlib (attributo)</span><span class="sxs-lookup"><span data-stu-id="b328e-104">importlib attribute</span></span>

<span data-ttu-id="b328e-105">La direttiva **\[ importlib \]** rende disponibili i tipi che sono già stati compilati in un'altra libreria dei tipi per la libreria dei tipi creata.</span><span class="sxs-lookup"><span data-stu-id="b328e-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="b328e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b328e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b328e-107">*Library-attributi*</span><span class="sxs-lookup"><span data-stu-id="b328e-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="b328e-108">Zero o più attributi che verranno applicati alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b328e-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="b328e-109">*nome della libreria*</span><span class="sxs-lookup"><span data-stu-id="b328e-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b328e-110">Identificatore che i componenti software utilizzeranno per indicare la [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="b328e-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b328e-111">*da file a importazione*</span><span class="sxs-lookup"><span data-stu-id="b328e-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="b328e-112">Nome e percorso del file importato in fase di compilazione MIDL.</span><span class="sxs-lookup"><span data-stu-id="b328e-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b328e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b328e-113">Remarks</span></span>

<span data-ttu-id="b328e-114">Tutte le direttive **\[ importlib \]** devono precedere le altre descrizioni dei tipi nella libreria.</span><span class="sxs-lookup"><span data-stu-id="b328e-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="b328e-115">Si noti che la libreria importata, così come la libreria generata, deve essere distribuita con l'applicazione in modo che sia disponibile in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b328e-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="b328e-116">Nella maggior parte dei casi è consigliabile usare la **\[** [](import.md) **\]** direttiva di importazione MIDL per fare riferimento alle definizioni di un altro. File IDL nel. File IDL.</span><span class="sxs-lookup"><span data-stu-id="b328e-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="b328e-117">Questo metodo fornisce alla libreria dei tipi tutte le informazioni del file originale, mentre **\[ importlib \]** porta solo il contenuto della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="b328e-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="b328e-118">La direttiva **\[ importlib \]** rende accessibili tutti i tipi definiti nella libreria importata dalla libreria in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b328e-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="b328e-119">Per evitare ambiguità in presenza di riferimenti duplicati, è consigliabile qualificare ogni riferimento con il nome della libreria appropriato, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b328e-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="b328e-120">In assenza di tale qualificazione, MIDL risolve ambiguità di riferimento duplicata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b328e-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="b328e-121">A partire dalla versione 3,1, MIDL usa il primo riferimento rilevato.</span><span class="sxs-lookup"><span data-stu-id="b328e-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="b328e-122">La versione 3,0 di MIDL, la prima versione di MIDL che può generare librerie dei tipi, usa l'ultimo riferimento rilevato.</span><span class="sxs-lookup"><span data-stu-id="b328e-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="b328e-123">Esempi</span><span class="sxs-lookup"><span data-stu-id="b328e-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="b328e-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b328e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b328e-125">**libreria**</span><span class="sxs-lookup"><span data-stu-id="b328e-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="b328e-126">**importare**</span><span class="sxs-lookup"><span data-stu-id="b328e-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="b328e-127">Importazione di file di intestazione di sistema</span><span class="sxs-lookup"><span data-stu-id="b328e-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="b328e-128">Importazione di file e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="b328e-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="b328e-129">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="b328e-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b328e-130">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="b328e-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b328e-131">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="b328e-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 