---
title: Importazione di file e librerie dei tipi
description: Le parole chiave MIDL includono, import e importlib consentono di riutilizzare il codice facendo riferimento ai file di intestazione, IDL e di definizione degli oggetti (FAD) esistenti e alle librerie dei tipi compilate.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, attività, importazione di file e librerie dei tipi
- importazione di MIDL
- librerie di tipi MIDL, importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353991"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="c8a38-106">Importazione di file e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="c8a38-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="c8a38-107">Le parole chiave MIDL [**includono**](include.md), [**Import**](import.md)e [**importlib**](importlib.md) consentono di riutilizzare il codice facendo riferimento ai file di intestazione, IDL e di definizione degli oggetti (FAD) esistenti e alle librerie dei tipi compilate.</span><span class="sxs-lookup"><span data-stu-id="c8a38-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="c8a38-108">Con la direttiva ACF [**include**](include.md) è possibile specificare in un file ACF uno o più file di intestazione del linguaggio C da includere nel codice stub generato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="c8a38-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="c8a38-109">Il file generato avrà una riga con una direttiva **\# Includi** il preprocessore C con il file di intestazione indicato.</span><span class="sxs-lookup"><span data-stu-id="c8a38-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="c8a38-110">Usare questa direttiva **include per inserire** i file di intestazione specifici di un determinato ambiente operativo e che non contengono informazioni necessarie per l'interfaccia tra client e server.</span><span class="sxs-lookup"><span data-stu-id="c8a38-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="c8a38-111">Non utilizzare **Includi** per i file di intestazione che contengono i tipi di dati che si desidera siano disponibili per il file IDL. usare invece la direttiva [**Import**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a38-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="c8a38-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8a38-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="c8a38-113">La direttiva di [**importazione**](import.md) IDL è il metodo standard per portare le definizioni di tipo e interfaccia da altri file IDL (o FAD) e file di intestazione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="c8a38-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="c8a38-114">Tutte le istruzioni IDL nel file importato, ad esempio i typedef, le dichiarazioni [**const**](const.md) e le definizioni di interfaccia, diventano disponibili per il file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="c8a38-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="c8a38-115">Analogamente alla direttiva per il preprocessore del linguaggio **C, la direttiva \#** [**Import**](import.md) indica al compilatore di includere i tipi di dati definiti nei file IDL importati.</span><span class="sxs-lookup"><span data-stu-id="c8a38-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="c8a38-116">A differenza della direttiva **\# include** , la direttiva **Import** ignora i prototipi di routine, perché non vengono generati stub per alcun elemento nel file importato.</span><span class="sxs-lookup"><span data-stu-id="c8a38-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="c8a38-117">Poiché il preprocessore viene richiamato separatamente per il file importato, le direttive per il preprocessore, ad esempio \* \*, non vengono riportate nel file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="c8a38-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="c8a38-118">Per ulteriori informazioni sull'utilizzo dell' [**importazione**](import.md) per includere i file di intestazione di sistema in un file IDL, vedere [importazione di file di intestazione di sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="c8a38-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="c8a38-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8a38-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="c8a38-120">La direttiva [**importlib**](importlib.md) di FAD consente di fare riferimento a una libreria dei tipi compilata nel file IDL o FAD.</span><span class="sxs-lookup"><span data-stu-id="c8a38-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="c8a38-121">La direttiva **importlib** deve trovarsi all'interno di un'istruzione [**Library**](library.md) e deve precedere altre descrizioni dei tipi nella libreria.</span><span class="sxs-lookup"><span data-stu-id="c8a38-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="c8a38-122">La libreria importata, così come la libreria generata, deve essere disponibile per l'applicazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c8a38-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="c8a38-123">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c8a38-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="c8a38-124">È anche possibile usare la direttiva di **\# inclusione** del preprocessore C per includere intestazioni e altri file nel file IDL o FAD.</span><span class="sxs-lookup"><span data-stu-id="c8a38-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="c8a38-125">Tenere presente, tuttavia, che questa direttiva includerà letteralmente l'intero contenuto del file specificato.</span><span class="sxs-lookup"><span data-stu-id="c8a38-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="c8a38-126">Se un file di intestazione contiene prototipi non necessari o desiderati nei file stub generati da MIDL o se contiene definizioni di tipi non, è necessario usare la direttiva di [**importazione**](import.md) MIDL invece della direttiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="c8a38-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8a38-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8a38-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a38-128">**importare**</span><span class="sxs-lookup"><span data-stu-id="c8a38-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="c8a38-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="c8a38-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="c8a38-130">**includere**</span><span class="sxs-lookup"><span data-stu-id="c8a38-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="c8a38-131">Importazione di file di intestazione di sistema</span><span class="sxs-lookup"><span data-stu-id="c8a38-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




