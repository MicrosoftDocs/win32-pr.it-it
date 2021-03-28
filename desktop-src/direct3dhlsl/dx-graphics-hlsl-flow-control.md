---
title: Controllo di flusso
description: La maggior parte dell'hardware è progettata per eseguire il codice dello shader riga per riga, eseguendo ogni istruzione HLSL una sola volta.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329255"
---
# <a name="flow-control"></a><span data-ttu-id="8c762-103">Controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="8c762-103">Flow Control</span></span>

<span data-ttu-id="8c762-104">La maggior parte dell'hardware è progettata per eseguire il codice dello shader riga per riga, eseguendo ogni istruzione HLSL una sola volta.</span><span class="sxs-lookup"><span data-stu-id="8c762-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="8c762-105">Un'istruzione di controllo di flusso determina in fase di esecuzione il blocco di istruzioni HLSL da eseguire successivamente.</span><span class="sxs-lookup"><span data-stu-id="8c762-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="8c762-106">Usando un'istruzione di controllo del flusso, uno shader può scorrere un set di istruzioni o passare a un'istruzione diversa da quella nella riga successiva.</span><span class="sxs-lookup"><span data-stu-id="8c762-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="8c762-107">Alcune istruzioni di controllo del flusso supportano il controllo statico specificato in fase di compilazione. altri offrono un controllo predicato che è una decisione per componente effettuata in fase di esecuzione e altri ancora supportano il controllo dinamico che è una decisione presa in fase di esecuzione in base al contenuto di una variabile.</span><span class="sxs-lookup"><span data-stu-id="8c762-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="8c762-108">HLSL supporta le seguenti istruzioni di controllo del flusso.</span><span class="sxs-lookup"><span data-stu-id="8c762-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="8c762-109">break</span><span class="sxs-lookup"><span data-stu-id="8c762-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="8c762-110">continuare</span><span class="sxs-lookup"><span data-stu-id="8c762-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="8c762-111">rimuovere</span><span class="sxs-lookup"><span data-stu-id="8c762-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="8c762-112">do</span><span class="sxs-lookup"><span data-stu-id="8c762-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="8c762-113">for</span><span class="sxs-lookup"><span data-stu-id="8c762-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="8c762-114">if</span><span class="sxs-lookup"><span data-stu-id="8c762-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="8c762-115">switch</span><span class="sxs-lookup"><span data-stu-id="8c762-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="8c762-116">mentre</span><span class="sxs-lookup"><span data-stu-id="8c762-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="8c762-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c762-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c762-118">Sintassi del linguaggio (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c762-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




