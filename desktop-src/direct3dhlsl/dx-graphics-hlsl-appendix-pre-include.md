---
title: " include (direttiva)"
description: Direttiva per il preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- includere la direttiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993437"
---
# <a name="include-directive"></a><span data-ttu-id="530f9-104">\#include (direttiva)</span><span class="sxs-lookup"><span data-stu-id="530f9-104">\#include Directive</span></span>

<span data-ttu-id="530f9-105">Direttiva per il preprocessore che inserisce il contenuto del file specificato nel programma di origine nel punto in cui viene visualizzata la direttiva.</span><span class="sxs-lookup"><span data-stu-id="530f9-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="530f9-106">\#Includi "*filename*"</span><span class="sxs-lookup"><span data-stu-id="530f9-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="530f9-107">\#Includi *nome file* <></span><span class="sxs-lookup"><span data-stu-id="530f9-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="530f9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="530f9-108">Parameters</span></span>

| <span data-ttu-id="530f9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="530f9-109">Item</span></span> | <span data-ttu-id="530f9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="530f9-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="530f9-111">*nomefile*</span><span class="sxs-lookup"><span data-stu-id="530f9-111">*filename*</span></span> | <span data-ttu-id="530f9-112">Nome del file da includere, facoltativamente preceduto da una specifica di directory.</span><span class="sxs-lookup"><span data-stu-id="530f9-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="530f9-113">Il nome file deve specificare un file esistente.</span><span class="sxs-lookup"><span data-stu-id="530f9-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="530f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="530f9-114">Remarks</span></span>

<span data-ttu-id="530f9-115">La \# direttiva include causa la sostituzione della direttiva dall'intero contenuto del file specificato.</span><span class="sxs-lookup"><span data-stu-id="530f9-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="530f9-116">Il preprocessore arresta la ricerca non appena trova un file con il nome specificato; Se si specifica un percorso completo e non ambiguo per il file, il preprocessore esegue la ricerca solo nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="530f9-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="530f9-117">Lo [strumento di compilazione degli effetti](/windows/desktop/direct3dtools/fxc) ha un gestore di inclusione incorporato che usa l'opzione/i.</span><span class="sxs-lookup"><span data-stu-id="530f9-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="530f9-118">Tuttavia, quando si esegue il compilatore dall'API, è possibile fornire un gestore di inclusione personalizzato implementando l'interfaccia ID3DXInclude.</span><span class="sxs-lookup"><span data-stu-id="530f9-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="530f9-119">La differenza tra le due forme di sintassi è l'ordine in cui il preprocessore cerca i file di intestazione quando il percorso viene specificato in modo incompleto, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="530f9-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="530f9-120">Forma di sintassi</span><span class="sxs-lookup"><span data-stu-id="530f9-120">Syntax form</span></span></th>
<th><span data-ttu-id="530f9-121">Modello di ricerca del preprocessore</span><span class="sxs-lookup"><span data-stu-id="530f9-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="530f9-122">#Includi <b>&quot;</b> <em>nome file</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="530f9-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="530f9-123">Cerca il file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="530f9-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="530f9-124">nella stessa directory del file che contiene la direttiva #include.</span><span class="sxs-lookup"><span data-stu-id="530f9-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="530f9-125">nelle directory dei file che contengono una direttiva #include per il file che contiene la direttiva #include.</span><span class="sxs-lookup"><span data-stu-id="530f9-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="530f9-126">nei percorsi specificati dall'opzione del compilatore/I nell'ordine in cui sono elencati.</span><span class="sxs-lookup"><span data-stu-id="530f9-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="530f9-127">nei percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</span><span class="sxs-lookup"><span data-stu-id="530f9-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="530f9-128">La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="530f9-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="530f9-129">Vedere la documentazione dell'ambiente di sviluppo per informazioni su come impostare i percorsi di inclusione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="530f9-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="530f9-130">#Includi <b><</b> <em>nome file</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="530f9-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="530f9-131">Cerca il file di inclusione:</span><span class="sxs-lookup"><span data-stu-id="530f9-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="530f9-132">nei percorsi specificati dall'opzione del compilatore/I nell'ordine in cui sono elencati.</span><span class="sxs-lookup"><span data-stu-id="530f9-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="530f9-133">nei percorsi specificati dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencati.</span><span class="sxs-lookup"><span data-stu-id="530f9-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="530f9-134">La variabile di ambiente INCLUDE viene ignorata in un ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="530f9-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="530f9-135">Vedere la documentazione dell'ambiente di sviluppo per informazioni su come impostare i percorsi di inclusione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="530f9-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="530f9-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="530f9-136">Examples</span></span>

<span data-ttu-id="530f9-137">L'esempio seguente fa sì che il preprocessore sostituisca la \# direttiva include con il contenuto di stdio. h.</span><span class="sxs-lookup"><span data-stu-id="530f9-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="530f9-138">Poiché nell'esempio viene usato il formato della parentesi angolare, il preprocessore cercherà il file solo nelle directory elencate dall'opzione del compilatore/I e nella variabile di ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="530f9-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="530f9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="530f9-139">See also</span></span>

- [<span data-ttu-id="530f9-140">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="530f9-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="530f9-141">[Interfaccia ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="530f9-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="530f9-142">Effect-strumento compilatore</span><span class="sxs-lookup"><span data-stu-id="530f9-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)