---
title: Componenti di MIDLRT e Windows Runtime
description: Viene illustrato come creare i file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime personalizzati.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL compilatore MIDL
- MIDL Compiler MIDL, MIDL e Windows Runtime WinRT
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517217"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="3cd14-106">Componenti di MIDLRT e Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="3cd14-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="3cd14-107">Viene illustrato come creare i file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3cd14-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="3cd14-108">Usare il compilatore MIDLRT per compilare file di metadati (con estensione winmd) per i componenti Windows Runtime personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3cd14-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="3cd14-109">Quando vengono generati i file di metadati, è possibile comprimerli in un pacchetto più efficiente tramite l'utilità MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="3cd14-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="3cd14-110">Per altre informazioni, vedere [MDMERGE e file di metadati](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="3cd14-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="3cd14-111">L'uso di MIDLRT è simile all'uso del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="3cd14-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="3cd14-112">Eseguire MIDLRT dalla riga di comando usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="3cd14-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="3cd14-113">**midlrt**  *<* **Opzioni** _>_ di **filename. idl**</span><span class="sxs-lookup"><span data-stu-id="3cd14-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="3cd14-114">dove \* < \***Opzioni** _>_ rappresenta le opzioni della riga di comando che si desidera utilizzare e filename. idl è il nome del file IDL da compilare.</span><span class="sxs-lookup"><span data-stu-id="3cd14-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="3cd14-115">Nell'elenco seguente vengono illustrate le opzioni della riga di comando utilizzate da MIDLRT.EXE.</span><span class="sxs-lookup"><span data-stu-id="3cd14-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="3cd14-116">**\_classe/enum**</span><span class="sxs-lookup"><span data-stu-id="3cd14-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="3cd14-117">**\_dir/Metadata**</span><span class="sxs-lookup"><span data-stu-id="3cd14-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="3cd14-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="3cd14-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="3cd14-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="3cd14-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="3cd14-120">**\_prefisso/NS**</span><span class="sxs-lookup"><span data-stu-id="3cd14-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="3cd14-121">**/WinMD**</span><span class="sxs-lookup"><span data-stu-id="3cd14-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="3cd14-122">**/WinRT**</span><span class="sxs-lookup"><span data-stu-id="3cd14-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="3cd14-123">Un elenco completo delle opzioni e delle opzioni del compilatore MIDLRT è disponibile quando si usa il compilatore MIDLRT [**/Help**](-help-.md) e/?</span><span class="sxs-lookup"><span data-stu-id="3cd14-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="3cd14-124">interruttori.</span><span class="sxs-lookup"><span data-stu-id="3cd14-124">switches.</span></span> <span data-ttu-id="3cd14-125">Le opzioni sono organizzate in base alle categorie.</span><span class="sxs-lookup"><span data-stu-id="3cd14-125">The switches are organized by categories.</span></span> <span data-ttu-id="3cd14-126">Per altre informazioni, vedere la Guida di [riferimento a MIDL Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3cd14-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cd14-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3cd14-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd14-128">MDMERGE e file di metadati</span><span class="sxs-lookup"><span data-stu-id="3cd14-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




