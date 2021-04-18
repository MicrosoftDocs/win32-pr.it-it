---
title: " ifndef"
description: La direttiva \ ifndef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298245"
---
# <a name="ifndef"></a><span data-ttu-id="eccf9-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="eccf9-103">\#ifndef</span></span>

<span data-ttu-id="eccf9-104">La direttiva **\# ifndef** controlla la compilazione condizionale del file di risorse controllando il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="eccf9-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="eccf9-105">Se il nome non è stato definito o la relativa definizione è stata rimossa usando la direttiva **\# undef** , **\# ifndef** indirizza il compilatore affinché continui a elaborare istruzioni fino alla successiva direttiva **\# endif**, **\# else** o **\# Elif** , quindi passare all'istruzione dopo la direttiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="eccf9-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="eccf9-106">Se il nome è definito, **\# ifndef** indica al compilatore di ignorare la direttiva **\# endif**, **\# else** o **\# Elif** successiva.</span><span class="sxs-lookup"><span data-stu-id="eccf9-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="eccf9-107"><span id="name"></span><span id="NAME"></span>*nome*</span><span class="sxs-lookup"><span data-stu-id="eccf9-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="eccf9-108">Nome che deve essere controllato dalla direttiva.</span><span class="sxs-lookup"><span data-stu-id="eccf9-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="eccf9-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="eccf9-109">Example</span></span>

<span data-ttu-id="eccf9-110">In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se Optimize non è definito:</span><span class="sxs-lookup"><span data-stu-id="eccf9-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="eccf9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eccf9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eccf9-112">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="eccf9-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




