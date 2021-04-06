---
title: " elif"
description: La direttiva \ Elif contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva \ ifdef, \ ifndef o \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044849"
---
# <a name="elif"></a><span data-ttu-id="ad36d-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="ad36d-103">\#elif</span></span>

<span data-ttu-id="ad36d-104">La direttiva **\# Elif** contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva **\# ifdef**, **\# ifndef** o **\# if** .</span><span class="sxs-lookup"><span data-stu-id="ad36d-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="ad36d-105">La direttiva controlla la compilazione condizionale del file di risorse controllando l'espressione costante specificata.</span><span class="sxs-lookup"><span data-stu-id="ad36d-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="ad36d-106">Se l'espressione costante è diversa da zero, **\# Elif** indica al compilatore di continuare l'elaborazione delle istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# Elif** e quindi di passare all'istruzione dopo **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="ad36d-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="ad36d-107">Se l'espressione costante è zero, **\# Elif** indica al compilatore di passare alla successiva direttiva **\# endif**, **\# else** o **\# Elif** .</span><span class="sxs-lookup"><span data-stu-id="ad36d-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="ad36d-108">È possibile utilizzare un numero qualsiasi di direttive **\# Elif** in un blocco condizionale.</span><span class="sxs-lookup"><span data-stu-id="ad36d-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="ad36d-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*espressione costante*</span><span class="sxs-lookup"><span data-stu-id="ad36d-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="ad36d-110">Espressione da controllare.</span><span class="sxs-lookup"><span data-stu-id="ad36d-110">Expression to be checked.</span></span> <span data-ttu-id="ad36d-111">Questo valore è un nome definito, una costante Integer o un'espressione costituita da nomi, numeri interi e operatori aritmetici e relazionali.</span><span class="sxs-lookup"><span data-stu-id="ad36d-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="ad36d-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad36d-112">Example</span></span>

<span data-ttu-id="ad36d-113">In questo esempio, **\# Elif** indica al compilatore di elaborare la seconda istruzione [**bitmap**](bitmap-resource.md) solo se il valore assegnato alla versione del nome è minore di 7.</span><span class="sxs-lookup"><span data-stu-id="ad36d-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="ad36d-114">La direttiva **\# Elif** viene elaborata solo se Version è maggiore o uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="ad36d-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="ad36d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad36d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad36d-116">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="ad36d-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




