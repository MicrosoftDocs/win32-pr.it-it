---
title: Strumento Command-Line MkTypLib
description: MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi. Può essere usato anche per generare un file di intestazione C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730639"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="766f1-104">Strumento Command-Line MkTypLib</span><span class="sxs-lookup"><span data-stu-id="766f1-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="766f1-105">\[Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="766f1-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="766f1-106">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="766f1-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="766f1-107">Se è necessaria la compatibilità con le versioni precedenti dei programmi di automazione, usare il compilatore MIDL con l'opzione **/mktyplib203** .\]</span><span class="sxs-lookup"><span data-stu-id="766f1-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="766f1-108">MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="766f1-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="766f1-109">Può essere usato anche per generare un file di intestazione C o C++.</span><span class="sxs-lookup"><span data-stu-id="766f1-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="766f1-110">Per generare una libreria dei tipi da un file FAD:</span><span class="sxs-lookup"><span data-stu-id="766f1-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="766f1-111">Al prompt dei comandi eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="766f1-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="766f1-112">\**mktyplibÂ \* \* \* nomefile*</span><span class="sxs-lookup"><span data-stu-id="766f1-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="766f1-113">dove *filename* è il nome del file FAD.</span><span class="sxs-lookup"><span data-stu-id="766f1-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="766f1-114">MkTypLib supporta inoltre diversi parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="766f1-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="766f1-115">Per un elenco completo, eseguire la riga di comando seguente:</span><span class="sxs-lookup"><span data-stu-id="766f1-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="766f1-116">**MkTypLib/?**</span><span class="sxs-lookup"><span data-stu-id="766f1-116">**mktyplib /?**</span></span>

<span data-ttu-id="766f1-117">Poiché MkTypLib è un'applicazione obsoleta, non è in grado di analizzare file o file IDL con interfacce definite all'esterno di un'istruzione di [**libreria**](/windows/desktop/Midl/library) .</span><span class="sxs-lookup"><span data-stu-id="766f1-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="766f1-118">Per altre informazioni, vedere [differenze tra MIDL e MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="766f1-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="766f1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="766f1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766f1-120">Conversione in C++</span><span class="sxs-lookup"><span data-stu-id="766f1-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 