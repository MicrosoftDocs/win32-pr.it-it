---
title: " ifdef"
description: La direttiva \ ifdef controlla la compilazione condizionale del file di risorse controllando il nome specificato.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396051"
---
# <a name="ifdef"></a><span data-ttu-id="a4bb8-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="a4bb8-103">\#ifdef</span></span>

<span data-ttu-id="a4bb8-104">La direttiva **\# ifdef** controlla la compilazione condizionale del file di risorse controllando il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="a4bb8-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="a4bb8-105">Se il nome è stato definito usando una direttiva **\# define** o l'opzione della riga di comando **/d** con il compilatore di risorse, **\# ifdef** indica al compilatore di continuare con l'istruzione immediatamente dopo la direttiva **\# ifdef** .</span><span class="sxs-lookup"><span data-stu-id="a4bb8-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="a4bb8-106">Se il nome non è stato definito, **\# ifdef** indica al compilatore di ignorare tutte le istruzioni fino alla direttiva **\# endif** successiva.</span><span class="sxs-lookup"><span data-stu-id="a4bb8-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="a4bb8-107"><span id="name"></span><span id="NAME"></span>*nome*</span><span class="sxs-lookup"><span data-stu-id="a4bb8-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="a4bb8-108">Nome che deve essere controllato dalla direttiva.</span><span class="sxs-lookup"><span data-stu-id="a4bb8-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="a4bb8-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="a4bb8-109">Example</span></span>

<span data-ttu-id="a4bb8-110">In questo esempio viene compilata l'istruzione [**bitmap**](bitmap-resource.md) solo se è definito il debug:</span><span class="sxs-lookup"><span data-stu-id="a4bb8-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="a4bb8-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4bb8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4bb8-112">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="a4bb8-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




