---
title: Uso del compilatore MIDL
description: Il compilatore MIDL viene installato automaticamente come parte dell'installazione di Platform Software Development Kit (SDK).
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Microsoft Interface Definition Language MIDL, attività
- MIDL compilatore MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398974"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="dfe5a-105">Uso del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="dfe5a-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="dfe5a-106">Il compilatore MIDL viene installato automaticamente come parte dell'installazione di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="dfe5a-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="dfe5a-107">Negli argomenti seguenti vengono descritti i requisiti del compilatore C MIDL e del preprocessore C, le librerie di collegamento che fanno parte del prodotto RPC (Remote Procedure Call) e i file generati da MIDL per le interfacce DCOM, le interfacce RPC e le interfacce della libreria dei tipi di automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="dfe5a-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="dfe5a-108">Richiamo del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="dfe5a-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="dfe5a-109">File di risposta</span><span class="sxs-lookup"><span data-stu-id="dfe5a-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="dfe5a-110">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="dfe5a-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="dfe5a-111">C/C++-considerazioni sul compilatore</span><span class="sxs-lookup"><span data-stu-id="dfe5a-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="dfe5a-112">Uso della \_ \_ costante predefinita MIDL</span><span class="sxs-lookup"><span data-stu-id="dfe5a-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="dfe5a-113">MIDL e RPC</span><span class="sxs-lookup"><span data-stu-id="dfe5a-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="dfe5a-114">MIDL e COM</span><span class="sxs-lookup"><span data-stu-id="dfe5a-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="dfe5a-115">MIDL e FAD</span><span class="sxs-lookup"><span data-stu-id="dfe5a-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="dfe5a-116">Per ulteriori informazioni sui file che costituiscono il prodotto RPC, vedere [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="dfe5a-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 