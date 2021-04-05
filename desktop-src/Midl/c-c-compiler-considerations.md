---
title: C/C++-considerazioni sul compilatore
description: Il compilatore MIDL deve interagire con il compilatore C e il preprocessore C.
ms.assetid: 3d91d0e4-3a47-4aa2-82d6-c3af11df3a78
keywords:
- MIDL compilatore MIDL, compilatore C
- MIDL del compilatore C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf6968951bbcbb423896f5609092054dfa65f4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045111"
---
# <a name="cc-compiler-considerations"></a><span data-ttu-id="04965-105">C/C++-considerazioni sul compilatore</span><span class="sxs-lookup"><span data-stu-id="04965-105">C/C++-Compiler Considerations</span></span>

<span data-ttu-id="04965-106">Il compilatore MIDL deve interagire con il compilatore C e il preprocessore C.</span><span class="sxs-lookup"><span data-stu-id="04965-106">The MIDL compiler must interoperate with the C compiler and C preprocessor.</span></span> <span data-ttu-id="04965-107">MIDL non accetta la sintassi C++ nell'input.</span><span class="sxs-lookup"><span data-stu-id="04965-107">MIDL does not accept C++ syntax on input.</span></span> <span data-ttu-id="04965-108">Il file con estensione h generato presenta le definizioni di tipo C e C++ per le interfacce.</span><span class="sxs-lookup"><span data-stu-id="04965-108">The generated .h file has both C-style and C++-style definitions for interfaces.</span></span> <span data-ttu-id="04965-109">Negli argomenti seguenti vengono descritti i requisiti per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="04965-109">The following topics describe the requirements for the C compiler.</span></span>

-   [<span data-ttu-id="04965-110">Problemi di compressione del compilatore C</span><span class="sxs-lookup"><span data-stu-id="04965-110">C-Compiler Packing Issues</span></span>](c-compiler-packing-issues.md)
-   [<span data-ttu-id="04965-111">Definizioni del compilatore C per proxy/stub</span><span class="sxs-lookup"><span data-stu-id="04965-111">C-Compiler Definitions for Proxy/Stubs</span></span>](c-compiler-definitions-for-proxy-stubs.md)

 

 




