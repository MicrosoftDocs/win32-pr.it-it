---
title: attributo helpstringdll
description: L'attributo \ helpstringdll \ imposta il nome della DLL da usare per eseguire una ricerca di stringhe di documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- attributo MIDL di helpstringdll
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956396"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="4b280-104">attributo helpstringdll</span><span class="sxs-lookup"><span data-stu-id="4b280-104">helpstringdll attribute</span></span>

<span data-ttu-id="4b280-105">L'attributo **\[ helpstringdll \]** imposta il nome della dll da usare per eseguire una ricerca di stringhe di documento.</span><span class="sxs-lookup"><span data-stu-id="4b280-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="4b280-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b280-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b280-107">*Guida-testo-stringa*</span><span class="sxs-lookup"><span data-stu-id="4b280-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="4b280-108">Stringa di caratteri con terminazione zero che specifica il nome di file completo di una DLL.</span><span class="sxs-lookup"><span data-stu-id="4b280-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="4b280-109">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4b280-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4b280-110">Altri attributi applicabili all'intera istruzione della libreria.</span><span class="sxs-lookup"><span data-stu-id="4b280-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="4b280-111">*nome della libreria*</span><span class="sxs-lookup"><span data-stu-id="4b280-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4b280-112">Identificatore che i componenti software utilizzeranno per indicare la [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="4b280-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b280-113">*Library-Definition-Statements*</span><span class="sxs-lookup"><span data-stu-id="4b280-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="4b280-114">Una o più istruzioni MIDL che definiscono l'interfaccia della [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="4b280-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b280-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b280-115">Remarks</span></span>

<span data-ttu-id="4b280-116">Utilizzare l'attributo **\[ helpstringdll \]** in un'istruzione Library per specificare, come stringa di caratteri, il nome file completo di una libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="4b280-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="4b280-117">Questo consente a un utente di visualizzare una descrizione della DLL con il Visualizzatore oggetti.</span><span class="sxs-lookup"><span data-stu-id="4b280-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="4b280-118">Usare le funzioni **GetDocumentation2** nelle interfacce **ITypeLib2** e **ITypeInfo2** per recuperare la stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="4b280-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b280-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b280-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b280-120">**libreria**</span><span class="sxs-lookup"><span data-stu-id="4b280-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="4b280-121">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="4b280-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4b280-122">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="4b280-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4b280-123">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="4b280-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 