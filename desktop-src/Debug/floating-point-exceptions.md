---
description: Per impostazione predefinita, tutte le eccezioni FP del sistema sono state disattivate.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Eccezioni a virgola mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304414"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="23fdd-103">Eccezioni a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="23fdd-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="23fdd-104">Per impostazione predefinita, tutte le eccezioni FP del sistema sono state disattivate.</span><span class="sxs-lookup"><span data-stu-id="23fdd-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="23fdd-105">Pertanto, i calcoli generano NAN o INFINITY, anziché un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="23fdd-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="23fdd-106">Prima di poter intercettare le eccezioni a virgola mobile (FP) utilizzando la gestione delle eccezioni strutturata, è necessario chiamare la funzione della libreria di runtime C di [ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) per attivare tutte le eccezioni FP possibili.</span><span class="sxs-lookup"><span data-stu-id="23fdd-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="23fdd-107">Per intercettare solo determinate eccezioni, utilizzare solo i flag che corrispondono alle eccezioni da intercettare.</span><span class="sxs-lookup"><span data-stu-id="23fdd-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="23fdd-108">Si noti che qualsiasi gestore per gli errori FP deve chiamare [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) come prima istruzione FP.</span><span class="sxs-lookup"><span data-stu-id="23fdd-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="23fdd-109">Questa funzione Cancella le eccezioni a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="23fdd-109">This function clears floating-point exceptions.</span></span>

 

 
