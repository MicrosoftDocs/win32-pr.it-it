---
title: " if"
description: La direttiva \ if controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298246"
---
# <a name="if"></a><span data-ttu-id="cb4da-103">\#Se</span><span class="sxs-lookup"><span data-stu-id="cb4da-103">\#if</span></span>

<span data-ttu-id="cb4da-104">La direttiva **\# if** controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata.</span><span class="sxs-lookup"><span data-stu-id="cb4da-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="cb4da-105">Se l'espressione costante è diversa da zero, **\# se** indica al compilatore di continuare a elaborare istruzioni fino alla direttiva **\# endif**, **\# else** o **\# Elif** successiva e quindi di passare all'istruzione dopo la direttiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="cb4da-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="cb4da-106">Se l'espressione costante è zero, **\# se** indica al compilatore di ignorare la direttiva **\# endif**, **\# else** o **\# Elif** successiva.</span><span class="sxs-lookup"><span data-stu-id="cb4da-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="cb4da-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*espressione costante*</span><span class="sxs-lookup"><span data-stu-id="cb4da-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="cb4da-108">Espressione da controllare.</span><span class="sxs-lookup"><span data-stu-id="cb4da-108">Expression to be checked.</span></span> <span data-ttu-id="cb4da-109">Questo valore è un nome definito, una costante Integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.</span><span class="sxs-lookup"><span data-stu-id="cb4da-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="cb4da-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="cb4da-110">Example</span></span>

<span data-ttu-id="cb4da-111">In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se la versione assegnata al valore è minore di 3:</span><span class="sxs-lookup"><span data-stu-id="cb4da-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="cb4da-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb4da-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb4da-113">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="cb4da-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




