---
title: Funzioni buffer
description: Per copiare il contenuto di un buffer fuori schermo in un buffer a schermo, chiamare SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funzioni WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320316"
---
# <a name="buffer-functions"></a><span data-ttu-id="23f93-104">Funzioni buffer</span><span class="sxs-lookup"><span data-stu-id="23f93-104">Buffer Functions</span></span>

<span data-ttu-id="23f93-105">Per copiare il contenuto di un buffer fuori schermo in un buffer a schermo, chiamare [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="23f93-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="23f93-106">La funzione **SwapBuffers** accetta un handle per un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23f93-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="23f93-107">Il formato pixel corrente per il contesto di dispositivo specificato deve includere un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="23f93-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="23f93-108">Per impostazione predefinita, il buffer nascosto è fuori schermo e il buffer anteriore è visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="23f93-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="23f93-109">La funzione **SwapBuffers** non scambia effettivamente il contenuto dei due buffer, bensì copia il contenuto di un buffer in un altro.</span><span class="sxs-lookup"><span data-stu-id="23f93-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="23f93-110">Il contenuto del buffer fuori schermo non è definito dopo una chiamata a **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="23f93-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="23f93-111">Pertanto, il risultato di due chiamate consecutive a **SwapBuffers** non è definito.</span><span class="sxs-lookup"><span data-stu-id="23f93-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="23f93-112">Nella figura seguente viene illustrato il modo in cui il contenuto dei buffer viene copiato quando si chiama **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="23f93-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Diagramma che mostra i risultati non definiti di chiamate consecutive alla funzione SwapBuffers.](images/opengl00.png)

<span data-ttu-id="23f93-114">Diverse funzioni di base di OpenGL gestiscono anche i buffer.</span><span class="sxs-lookup"><span data-stu-id="23f93-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="23f93-115">La funzione [**glDrawBuffer**](gldrawbuffer.md) è l'unica più rilevante per il doppio buffer; Specifica il framebuffer o i buffer in cui viene disegnato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="23f93-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="23f93-116">Anche le funzioni seguenti influiscono sui buffer:</span><span class="sxs-lookup"><span data-stu-id="23f93-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="23f93-117">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="23f93-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="23f93-118">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="23f93-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="23f93-119">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="23f93-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="23f93-120">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="23f93-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="23f93-121">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="23f93-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="23f93-122">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="23f93-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="23f93-123">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="23f93-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="23f93-124">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="23f93-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="23f93-125">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="23f93-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="23f93-126">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="23f93-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="23f93-127">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="23f93-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="23f93-128">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="23f93-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="23f93-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="23f93-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




