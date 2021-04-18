---
title: Richiamo del compilatore MIDL
description: Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema. Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una versione specifica, consultare l'opzione/target.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL compilatore MIDL, chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "106299007"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="2a7b1-105">Richiamo del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="2a7b1-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="2a7b1-106">Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="2a7b1-107">Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una versione specifica, consultare l'opzione [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7b1-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="2a7b1-108">Eseguire il compilatore MIDL dalla riga di comando usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2a7b1-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="2a7b1-109"> *<  opzioni >* MIDL **nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="2a7b1-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="2a7b1-110">dove *<  Options >* rappresenta le opzioni della riga di comando che si vuole usare e filename. idl è il nome del file MIDL da compilare.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="2a7b1-111">Un elenco completo delle opzioni e dei commutatori del compilatore MIDL è disponibile quando si usa il compilatore MIDL [**/Help**](-help-.md) e/?</span><span class="sxs-lookup"><span data-stu-id="2a7b1-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="2a7b1-112">interruttori.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-112">switches.</span></span> <span data-ttu-id="2a7b1-113">Le opzioni sono organizzate in base alle categorie.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-113">The switches are organized by categories.</span></span> <span data-ttu-id="2a7b1-114">Per informazioni dettagliate, vedere la Guida di [riferimento a MIDL Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2a7b1-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2a7b1-115">Il nuovo flag globale **$ ( \_ ottimizzazione MIDL)** esiste in Win32. mak.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="2a7b1-116">Quando si compila un file con estensione IDL utilizzando questo flag, lo stub generato può utilizzare le funzionalità RPC più recenti disponibili sulla piattaforma specificata e potenzialmente migliorare le prestazioni e la stabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="2a7b1-117">È consigliabile che le applicazioni usino questo flag quando si usa MIDL.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="2a7b1-118">**MIDL** **$ ( \_ ottimizzazione MIDL)** **...**</span><span class="sxs-lookup"><span data-stu-id="2a7b1-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>