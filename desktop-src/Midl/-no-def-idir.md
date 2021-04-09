---
title: /no_def_idir opzione
description: Quando si specificano le directory con l'opzione/I, \_ l' \_ opzione/No def Idir indica al compilatore MIDL di eseguire la ricerca solo nelle directory specificate con l'opzione/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir switch MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857585"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="ac79e-104">/No \_ def \_ Idir switch</span><span class="sxs-lookup"><span data-stu-id="ac79e-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="ac79e-105">Quando si specificano le directory con l'opzione [**/i**](-i.md) , l'opzione **/No \_ def \_ Idir** indica al compilatore MIDL di eseguire la ricerca solo nelle directory specificate con l'opzione **/i** , ignorando la directory corrente e le directory specificate dalla variabile di ambiente include.</span><span class="sxs-lookup"><span data-stu-id="ac79e-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="ac79e-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="ac79e-106">Switch Options</span></span>

<span data-ttu-id="ac79e-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ac79e-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac79e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac79e-108">Remarks</span></span>

<span data-ttu-id="ac79e-109">Quando non viene specificata alcuna directory con l'opzione [**/i**](-i.md) , l'opzione **/No \_ def \_ Idir** indica al compilatore MIDL di eseguire la ricerca solo nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="ac79e-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="ac79e-110">Esempi</span><span class="sxs-lookup"><span data-stu-id="ac79e-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="ac79e-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ac79e-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac79e-112">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="ac79e-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ac79e-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="ac79e-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="ac79e-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="ac79e-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




