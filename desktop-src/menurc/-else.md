---
title: " else"
description: La direttiva \ else contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva \ ifdef, \ ifndef o \ if. La direttiva \ else deve essere l'ultima direttiva prima della direttiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710912"
---
# <a name="else"></a><span data-ttu-id="1e23b-104">\#else</span><span class="sxs-lookup"><span data-stu-id="1e23b-104">\#else</span></span>

<span data-ttu-id="1e23b-105">La direttiva **\# else** contrassegna una clausola facoltativa di un blocco di compilazione condizionale definito da una direttiva **\# ifdef**, **\# ifndef** o **\# if** .</span><span class="sxs-lookup"><span data-stu-id="1e23b-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="1e23b-106">La direttiva **\# else** deve essere l'ultima direttiva prima della direttiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="1e23b-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="1e23b-107">Questa direttiva non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="1e23b-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="1e23b-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="1e23b-108">Example</span></span>

<span data-ttu-id="1e23b-109">Questo esempio compila la seconda istruzione [**bitmap**](bitmap-resource.md) solo se il debug non è definito:</span><span class="sxs-lookup"><span data-stu-id="1e23b-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="1e23b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e23b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e23b-111">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="1e23b-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




