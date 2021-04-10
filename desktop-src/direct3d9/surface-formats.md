---
description: In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da una gamma lineare di memoria denominata superficie.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formati di superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124812"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="84e55-103">Formati di superficie (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="84e55-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="84e55-104">In Direct3D tutte le immagini bidimensionali (2D) sono rappresentate da una gamma lineare di memoria denominata superficie.</span><span class="sxs-lookup"><span data-stu-id="84e55-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="84e55-105">Una superficie può essere considerata come una matrice 2D in cui ogni elemento include un valore di colore che rappresenta una piccola sezione dell'immagine, detta pixel.</span><span class="sxs-lookup"><span data-stu-id="84e55-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="84e55-106">Il livello di dettaglio di un'immagine viene definito sia dal numero di pixel necessari per rappresentare l'immagine che dal numero di bit necessari per lo spettro di colore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84e55-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="84e55-107">Ad esempio, un'immagine di 800 pixel di larghezza per 600 pixel di altezza con 32 bit di colore per ogni pixel (scritta come 800x600x32) sarà più dettagliata di un'immagine con una larghezza di 640 pixel in larghezza per 480 pixel di altezza con 16 bit di colore per ogni pixel (scritto come 640x480x16).</span><span class="sxs-lookup"><span data-stu-id="84e55-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="84e55-108">Analogamente, l'immagine più dettagliata richiederà una superficie più ampia per archiviare i dati.</span><span class="sxs-lookup"><span data-stu-id="84e55-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="84e55-109">Per un'immagine 800x600x32, le dimensioni della matrice della superficie saranno 800x600 e ogni elemento manterrà un valore a 32 bit per rappresentare il colore.</span><span class="sxs-lookup"><span data-stu-id="84e55-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="84e55-110">Tutte le superfici hanno una dimensione e archiviano un numero specifico di bit che rappresentano il colore.</span><span class="sxs-lookup"><span data-stu-id="84e55-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="84e55-111">I bit che rappresentano il colore sono separati in singoli elementi di colore: rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="84e55-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="84e55-112">In Direct3D tutti gli elementi di colore sono definiti dal tipo enumerato [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="84e55-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="84e55-113">Un formato di colore Direct3D viene suddiviso nel numero di addii riservati per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="84e55-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="84e55-114">Un formato di colore a 16 bit in Direct3D, ad esempio, è definito come D3DFMT \_ R5G6B5, dove 5 bit sono riservati per rosso (R), 6 bit per il verde (G) e 5 bit per il blu (B).</span><span class="sxs-lookup"><span data-stu-id="84e55-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84e55-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84e55-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e55-116">Superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="84e55-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



