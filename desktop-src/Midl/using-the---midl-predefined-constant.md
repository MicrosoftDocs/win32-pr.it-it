---
title: Uso della costante __midl predefinita
description: Quando il compilatore MIDL elabora i file di input IDL e ACF, \_ \_ MIDL viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere la coerenza durante la compilazione.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL Compiler MIDL, uso della _midl costante predefinita
- _midl MIDL costante predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044791"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="77195-105">Uso della \_ \_ costante predefinita MIDL</span><span class="sxs-lookup"><span data-stu-id="77195-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="77195-106">Quando il compilatore MIDL elabora i file di input IDL e ACF, \_ \_ MIDL viene definito per impostazione predefinita e viene usato per la compilazione condizionale per ottenere la coerenza durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="77195-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="77195-107">In questo modo si elimina l'uso di istruzioni define nei file di intestazione, ad esempio il **\_ passaggio MIDL**, e li sostituisce con un flag coerente.</span><span class="sxs-lookup"><span data-stu-id="77195-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="77195-108">Il valore della \_ \_ costante MIDL indica la versione del compilatore *Major. minor* in base alla formula *principale* \* 100 + *minor*, ad esempio MIDL ver.</span><span class="sxs-lookup"><span data-stu-id="77195-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="77195-109">la versione 6.0. x ha il \_ \_ MIDL definito come 600.</span><span class="sxs-lookup"><span data-stu-id="77195-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="77195-110">Se si sceglie, è possibile eseguire l'override di questa impostazione predefinita specificando quanto segue nella riga di comando: **/u \_ \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="77195-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="77195-111">Per ulteriori informazioni, vedere [**/u**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="77195-111">For more information, see [**/U**](-u.md).</span></span>

 

 




