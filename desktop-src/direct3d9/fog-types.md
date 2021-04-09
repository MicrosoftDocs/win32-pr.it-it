---
description: 'Esistono due modi per aggiungere la nebbia a una scena: con nebbia pixel e/o nebbia vertice.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Tipi di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123867"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="4289b-103">Tipi di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4289b-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="4289b-104">Esistono due modi per aggiungere la nebbia a una scena: con nebbia pixel e/o nebbia vertice.</span><span class="sxs-lookup"><span data-stu-id="4289b-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="4289b-105">Negli argomenti seguenti vengono illustrate le formule utilizzate nelle equazioni di nebbia, oltre a implementare la nebbia dei vertici e dei pixel.</span><span class="sxs-lookup"><span data-stu-id="4289b-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="4289b-106">Un'applicazione può implementare la nebbia con un vertex shader e contemporaneamente la nebbia pixel, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="4289b-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="4289b-107">Formule di nebbia</span><span class="sxs-lookup"><span data-stu-id="4289b-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="4289b-108">Parametri di nebbia</span><span class="sxs-lookup"><span data-stu-id="4289b-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="4289b-109">Blending di nebbia</span><span class="sxs-lookup"><span data-stu-id="4289b-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="4289b-110">Colore nebbia</span><span class="sxs-lookup"><span data-stu-id="4289b-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="4289b-111">Nebbia vertice</span><span class="sxs-lookup"><span data-stu-id="4289b-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="4289b-112">Nebbia pixel</span><span class="sxs-lookup"><span data-stu-id="4289b-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="4289b-113">La fusione di nebbia è controllata dagli Stati di rendering; non fa parte della pipeline di pixel programmabile.</span><span class="sxs-lookup"><span data-stu-id="4289b-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4289b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4289b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4289b-115">Buffer frame</span><span class="sxs-lookup"><span data-stu-id="4289b-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



