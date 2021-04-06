---
title: Microsoft Interface Definition Language
description: Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL (vedere Microsoft Interface Definition Language MIDL)
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046641"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="9f1de-107">Microsoft Interface Definition Language</span><span class="sxs-lookup"><span data-stu-id="9f1de-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="9f1de-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="9f1de-108">Purpose</span></span>

<span data-ttu-id="9f1de-109">Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server.</span><span class="sxs-lookup"><span data-stu-id="9f1de-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="9f1de-110">Microsoft include il compilatore MIDL con Platform Software Development Kit (SDK) per consentire agli sviluppatori di creare i file IDL (Interface Definition Language) e i file di configurazione dell'applicazione (ACF) necessari per le interfacce RPC (Remote Procedure Call) e le interfacce COM/DCOM.</span><span class="sxs-lookup"><span data-stu-id="9f1de-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="9f1de-111">MIDL supporta inoltre la generazione di librerie dei tipi per l'automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="9f1de-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9f1de-112">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="9f1de-112">Where applicable</span></span>

<span data-ttu-id="9f1de-113">MIDL può essere usato in tutte le applicazioni client/server basate su sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="9f1de-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="9f1de-114">Può essere usato anche per creare programmi client e server per ambienti di rete eterogenei che includono sistemi operativi come UNIX e Apple.</span><span class="sxs-lookup"><span data-stu-id="9f1de-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="9f1de-115">Microsoft supporta il gruppo aperto (noto in precedenza come Open Software Foundation) DCE standard per l'interoperabilità RPC.</span><span class="sxs-lookup"><span data-stu-id="9f1de-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9f1de-116">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="9f1de-116">Developer audience</span></span>

<span data-ttu-id="9f1de-117">Quando si usa MIDL con RPC, è necessaria una certa familiarità con la programmazione C/C++ e il paradigma RPC.</span><span class="sxs-lookup"><span data-stu-id="9f1de-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="9f1de-118">Quando si usa MIDL con COM, è necessaria una certa familiarità con la programmazione C++ e il paradigma RPC che si applica a COM. in alternativa, è necessaria una certa familiarità con gli script e le librerie dei tipi di modelli di automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="9f1de-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9f1de-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="9f1de-119">Run-time requirements</span></span>

<span data-ttu-id="9f1de-120">Le librerie di runtime appropriate per l'utilizzo di MIDL sono incluse in Windows.</span><span class="sxs-lookup"><span data-stu-id="9f1de-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="9f1de-121">Il compilatore MIDL e i componenti dell'ambiente di sviluppo RPC vengono installati quando si installa il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9f1de-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="9f1de-122">Per ulteriori informazioni, vedere [utilizzo del compilatore MIDL](using-the-midl-compiler-2.md) e [installazione dell'ambiente di programmazione RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="9f1de-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f1de-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9f1de-123">In this section</span></span>



| <span data-ttu-id="9f1de-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="9f1de-124">Topic</span></span>                                                                                               | <span data-ttu-id="9f1de-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f1de-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f1de-126">Overview</span><span class="sxs-lookup"><span data-stu-id="9f1de-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="9f1de-127">Informazioni generali su MIDL e sul compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="9f1de-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="9f1de-128">Uso del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="9f1de-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="9f1de-129">Informazioni sull'uso di MIDL compilatore per generare stub RPC.</span><span class="sxs-lookup"><span data-stu-id="9f1de-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="9f1de-130">Definizioni di interfaccia e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="9f1de-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="9f1de-131">Documentazione delle definizioni di interfaccia specifiche di RPC e delle librerie dei tipi.</span><span class="sxs-lookup"><span data-stu-id="9f1de-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="9f1de-132">Riferimento Command-Line MIDL</span><span class="sxs-lookup"><span data-stu-id="9f1de-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="9f1de-133">Documentazione delle opzioni della riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="9f1de-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="9f1de-134">Riferimenti per il linguaggio MIDL</span><span class="sxs-lookup"><span data-stu-id="9f1de-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="9f1de-135">Riferimenti al linguaggio del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="9f1de-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="9f1de-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f1de-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f1de-137">RPC (Remote Procedure Call)</span><span class="sxs-lookup"><span data-stu-id="9f1de-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

