---
title: helpfile (attributo)
description: L'attributo \ fileguide \ imposta il nome del file della Guida per una libreria dei tipi. Tutti i tipi in una libreria condividono lo stesso file della guida.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- attributo filelima MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725162"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="aaf0d-105">helpfile (attributo)</span><span class="sxs-lookup"><span data-stu-id="aaf0d-105">helpfile attribute</span></span>

<span data-ttu-id="aaf0d-106">L'attributo **\[ filelima \]** imposta il nome del file della Guida per una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="aaf0d-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="aaf0d-107">Tutti i tipi in una libreria condividono lo stesso file della guida.</span><span class="sxs-lookup"><span data-stu-id="aaf0d-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="aaf0d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aaf0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf0d-109">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="aaf0d-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf0d-110">Specifica un numero di identificazione univoco universale per la [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="aaf0d-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaf0d-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="aaf0d-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf0d-112">Specifica il nome del file contenente il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="aaf0d-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="aaf0d-113">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="aaf0d-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf0d-114">Specifica zero o più attributi che verranno applicati al compilatore MIDL alla [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="aaf0d-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaf0d-115">*istruzioni Library*</span><span class="sxs-lookup"><span data-stu-id="aaf0d-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf0d-116">Specifica una o più istruzioni MIDL che definiscono l'interfaccia della libreria.</span><span class="sxs-lookup"><span data-stu-id="aaf0d-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaf0d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaf0d-117">Remarks</span></span>

<span data-ttu-id="aaf0d-118">Usare le funzioni **GetDocumentation** nelle interfacce **ITypeLib** e **ITypeInfo** per recuperare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="aaf0d-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="aaf0d-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="aaf0d-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="aaf0d-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aaf0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf0d-121">**libreria**</span><span class="sxs-lookup"><span data-stu-id="aaf0d-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="aaf0d-122">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="aaf0d-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="aaf0d-123">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="aaf0d-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="aaf0d-124">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="aaf0d-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 