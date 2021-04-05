---
title: Scelta tra RGBA e modalità Color-Index
description: In generale, usare la modalità RGBA per le applicazioni OpenGL; offre maggiore flessibilità rispetto alla modalità di indice dei colori per gli effetti come ombreggiatura, illuminazione, mappatura dei colori, nebbia, anti-aliasing e fusione.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL in Windows, modalità RGBA
- OpenGL per Windows, modalità indice colori
- OpenGL in modalità RGBA
- OpenGL modalità di indice colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710423"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="bf24c-107">Scelta tra RGBA e modalità Color-Index</span><span class="sxs-lookup"><span data-stu-id="bf24c-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="bf24c-108">In generale, usare la modalità RGBA per le applicazioni OpenGL; offre maggiore flessibilità rispetto alla modalità di indice dei colori per gli effetti come ombreggiatura, illuminazione, mappatura dei colori, nebbia, anti-aliasing e fusione.</span><span class="sxs-lookup"><span data-stu-id="bf24c-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="bf24c-109">Provare a usare la modalità di indice dei colori nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf24c-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="bf24c-110">Se è disponibile un numero limitato di bitplane; la modalità di indicizzazione dei colori può produrre ombreggiatura meno grossolana rispetto alla modalità RGBA.</span><span class="sxs-lookup"><span data-stu-id="bf24c-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="bf24c-111">Se non si è interessati a usare i colori "reali"; ad esempio, usando più colori in una mappa topografica per designare le elevazioni relative.</span><span class="sxs-lookup"><span data-stu-id="bf24c-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="bf24c-112">Quando si esegue il porting di un'applicazione esistente che usa ampiamente la modalità di indice colori.</span><span class="sxs-lookup"><span data-stu-id="bf24c-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="bf24c-113">Quando si desidera utilizzare l'animazione e gli effetti della mappa dei colori nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf24c-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="bf24c-114">Questa operazione non è possibile nei dispositivi con colori reali.</span><span class="sxs-lookup"><span data-stu-id="bf24c-114">(This is not possible on true-color devices.)</span></span>

 

 




