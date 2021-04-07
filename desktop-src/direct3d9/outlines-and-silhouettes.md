---
description: È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Strutture e sagome (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745535"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="f7acd-103">Strutture e sagome (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7acd-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="f7acd-104">È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.</span><span class="sxs-lookup"><span data-stu-id="f7acd-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="f7acd-105">Se l'applicazione applica una maschera di stencil all'immagine di una primitiva che ha la stessa forma ma leggermente più piccola, l'immagine risultante contiene solo il contorno della primitiva.</span><span class="sxs-lookup"><span data-stu-id="f7acd-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="f7acd-106">L'applicazione può quindi riempire l'area con maschera di stencil dell'immagine con un colore a tinta unita, assegnando alla primitiva un aspetto in rilievo.</span><span class="sxs-lookup"><span data-stu-id="f7acd-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="f7acd-107">Se la maschera dello stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si sta eseguendo il rendering, l'immagine risultante contiene un foro in cui la primitiva deve essere.</span><span class="sxs-lookup"><span data-stu-id="f7acd-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="f7acd-108">L'applicazione può quindi riempire il foro con il nero per produrre una silhouette della primitiva.</span><span class="sxs-lookup"><span data-stu-id="f7acd-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7acd-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7acd-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7acd-110">Tecniche del buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="f7acd-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



