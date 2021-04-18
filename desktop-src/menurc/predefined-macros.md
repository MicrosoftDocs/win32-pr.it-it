---
title: Macro predefinite
description: RC non supporta le macro predefinite ANSI C ( \_ \_ date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ STDC \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ). Di conseguenza, non è possibile includere queste macro nei file di intestazione da includere nello script della risorsa.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116800"
---
# <a name="predefined-macros"></a><span data-ttu-id="e4471-104">Macro predefinite</span><span class="sxs-lookup"><span data-stu-id="e4471-104">Predefined Macros</span></span>

<span data-ttu-id="e4471-105">RC non supporta le macro predefinite ANSI C (**\_ \_ date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ STDC \_ , Time \_** **\_ \_ , timestamp \_ ). \_** **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4471-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="e4471-106">Di conseguenza, non è possibile includere queste macro nei file di intestazione da includere nello script della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4471-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="e4471-107">RC definisce RC \_ richiamato, che consente di compilare in modo condizionale parti dei file di intestazione, a seconda che il compilatore sia il compilatore C o il compilatore RC.</span><span class="sxs-lookup"><span data-stu-id="e4471-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="e4471-108">Questo è importante perché il compilatore RC supporta solo un subset delle istruzioni supportate da un compilatore C.</span><span class="sxs-lookup"><span data-stu-id="e4471-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="e4471-109">Per compilare in modo condizionale il codice con il compilatore RC, racchiudere il codice che RC non può compilare con \# ifndef RC \_ richiamato e **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="e4471-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="e4471-110">L'esempio seguente è tratto dagli esempi di SDK.</span><span class="sxs-lookup"><span data-stu-id="e4471-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="e4471-111">Viene illustrato come creare un file di intestazione che può essere compilato in modo condizionale.</span><span class="sxs-lookup"><span data-stu-id="e4471-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




