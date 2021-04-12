---
title: Strategie di disegno OpenGL multithread
description: GDI non supporta più thread.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL per Windows, disegno multithread
- OpenGL disegno OpenGL multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329503"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="275d4-105">Strategie di disegno OpenGL multithread</span><span class="sxs-lookup"><span data-stu-id="275d4-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="275d4-106">GDI non supporta più thread.</span><span class="sxs-lookup"><span data-stu-id="275d4-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="275d4-107">È necessario usare un contesto di dispositivo distinto e un contesto di rendering distinto per ogni thread.</span><span class="sxs-lookup"><span data-stu-id="275d4-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="275d4-108">Ciò tende a limitare i vantaggi in termini di prestazioni dell'utilizzo di più thread con sistemi a processore singolo che eseguono applicazioni OpenGL.</span><span class="sxs-lookup"><span data-stu-id="275d4-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="275d4-109">Esistono tuttavia modi per utilizzare i thread con un sistema a processore singolo per migliorare significativamente le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="275d4-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="275d4-110">Ad esempio, è possibile usare un thread separato per passare le chiamate di rendering OpenGL a hardware 3D dedicato.</span><span class="sxs-lookup"><span data-stu-id="275d4-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="275d4-111">I sistemi SMP (Symmetric Multiprocessor) possono trarre notevole vantaggio dall'uso di più thread.</span><span class="sxs-lookup"><span data-stu-id="275d4-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="275d4-112">Una strategia ovvia consiste nell'usare un thread separato per ogni processore per gestire il rendering OpenGL in finestre separate.</span><span class="sxs-lookup"><span data-stu-id="275d4-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="275d4-113">Ad esempio, in un'applicazione di simulazione del volo è possibile usare processori e thread distinti per eseguire il rendering delle visualizzazioni front, back e Side.</span><span class="sxs-lookup"><span data-stu-id="275d4-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="275d4-114">Un thread può avere un solo contesto di rendering attivo e corrente.</span><span class="sxs-lookup"><span data-stu-id="275d4-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="275d4-115">Quando si usano più thread e più contesti di rendering, è necessario prestare attenzione a sincronizzarne l'uso.</span><span class="sxs-lookup"><span data-stu-id="275d4-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="275d4-116">Usare, ad esempio, un solo thread per chiamare [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) al termine del disegno di tutti i thread.</span><span class="sxs-lookup"><span data-stu-id="275d4-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




