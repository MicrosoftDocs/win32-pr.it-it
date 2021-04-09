---
title: Funzioni in formato pixel
description: Le funzioni di Windows seguenti gestiscono i formati pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funzioni WGL, formato pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856885"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="cdc43-104">Funzioni in formato pixel</span><span class="sxs-lookup"><span data-stu-id="cdc43-104">Pixel Format Functions</span></span>

<span data-ttu-id="cdc43-105">Le funzioni di Windows seguenti gestiscono i formati pixel.</span><span class="sxs-lookup"><span data-stu-id="cdc43-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="cdc43-106">Funzione Windows</span><span class="sxs-lookup"><span data-stu-id="cdc43-106">Windows Function</span></span>                                               | <span data-ttu-id="cdc43-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc43-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdc43-108">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cdc43-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="cdc43-109">Ottiene il formato pixel del contesto di dispositivo che rappresenta la corrispondenza più vicina al formato pixel specificato.</span><span class="sxs-lookup"><span data-stu-id="cdc43-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="cdc43-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cdc43-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="cdc43-111">Imposta il formato pixel corrente di un contesto di dispositivo sul formato pixel specificato da un indice di formato pixel.</span><span class="sxs-lookup"><span data-stu-id="cdc43-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="cdc43-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cdc43-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="cdc43-113">Ottiene l'indice di formato pixel del formato pixel corrente di un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdc43-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="cdc43-114">**DescribePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cdc43-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="cdc43-115">Dato un contesto di dispositivo e un indice di formato pixel, compila una struttura di dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) con le proprietà del formato pixel.</span><span class="sxs-lookup"><span data-stu-id="cdc43-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="cdc43-116">**GetEnhMetaFilePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="cdc43-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="cdc43-117">Recupera le informazioni sul formato pixel per un metafile avanzato.</span><span class="sxs-lookup"><span data-stu-id="cdc43-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="cdc43-118">La funzione [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) restituisce un indice in formato pixel in base 1 che identifica la migliore corrispondenza tra i formati pixel supportati del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdc43-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="cdc43-119">La funzione [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica il formato desiderato usando un indice in formato pixel basato su uno.</span><span class="sxs-lookup"><span data-stu-id="cdc43-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="cdc43-120">In genere, si chiama **ChoosePixelFormat** per trovare un formato pixel con la corrispondenza migliore, quindi si chiama **SetPixelFormat** con il risultato di **ChoosePixelFormat**.</span><span class="sxs-lookup"><span data-stu-id="cdc43-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="cdc43-121">Se si chiama **SetPixelFormat** per un contesto di dispositivo che fa riferimento a una finestra, **SetPixelFormat** modifica anche il formato pixel della finestra.</span><span class="sxs-lookup"><span data-stu-id="cdc43-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="cdc43-122">L'impostazione del formato pixel di una finestra più volte può comportare complicazioni significative per gestione finestre e per le applicazioni multithread, quindi non è consentito.</span><span class="sxs-lookup"><span data-stu-id="cdc43-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="cdc43-123">È possibile impostare il formato pixel di una finestra una sola volta. Successivamente, il formato pixel della finestra non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="cdc43-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="cdc43-124">La funzione [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) restituisce un indice in formato pixel in base uno.</span><span class="sxs-lookup"><span data-stu-id="cdc43-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="cdc43-125">La funzione [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) accetta quanto segue come parametri:</span><span class="sxs-lookup"><span data-stu-id="cdc43-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="cdc43-126">Handle per un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="cdc43-126">A handle to a device context</span></span>
-   <span data-ttu-id="cdc43-127">Indice di formato pixel</span><span class="sxs-lookup"><span data-stu-id="cdc43-127">A pixel format index</span></span>
-   <span data-ttu-id="cdc43-128">Puntatore a una struttura di dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)</span><span class="sxs-lookup"><span data-stu-id="cdc43-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="cdc43-129">La funzione [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) restituisce con i membri di **PIXELFORMATDESCRIPTOR** impostati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="cdc43-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="cdc43-130">La funzione **GetEnhMetaFilePixelFormat** restituisce le dimensioni del formato pixel di un metafile e recupera le informazioni sul formato pixel del metafile.</span><span class="sxs-lookup"><span data-stu-id="cdc43-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




