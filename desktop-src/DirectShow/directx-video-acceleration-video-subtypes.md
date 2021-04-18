---
description: I sottotipi seguenti vengono usati dai decodificatori che usano l'accelerazione video DirectX (DXVA).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Sottotipi video di accelerazione video DirectX (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328477"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="bf156-103">Sottotipi video di accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="bf156-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="bf156-104">I sottotipi seguenti vengono usati dai decodificatori che usano l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="bf156-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="bf156-105">AI44 e IA44 sono superfici con un valore bits per pixel pari a 8.</span><span class="sxs-lookup"><span data-stu-id="bf156-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="bf156-106">Sono presenti 4 *bit di I* e 4 bit di. *I* rappresenta un indice in una tavolozza YUV a 16 voci.</span><span class="sxs-lookup"><span data-stu-id="bf156-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="bf156-107">*Un oggetto* rappresenta 4 bit di informazioni di trasparenza (anche noto come per pixel-alfa).</span><span class="sxs-lookup"><span data-stu-id="bf156-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="bf156-108">Pertanto, le superfici AI44 e IA44 consentono 16 colori diversi con 16 diversi valori di trasparenza o 256 diverse rappresentazioni di pixel.</span><span class="sxs-lookup"><span data-stu-id="bf156-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="bf156-109">Con AI44, il Alpha viene archiviato nell'oggetto Hi-sgranocchiate, in IA44 l'alfa viene archiviato nello lo-bocconcino.</span><span class="sxs-lookup"><span data-stu-id="bf156-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="bf156-110">Entrambi i formati sono molto utili per immagini di sottoimmagine DVD e immagini di Line21 e televideo.</span><span class="sxs-lookup"><span data-stu-id="bf156-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="bf156-111">Microsoft preferisce la versione AI44 perché è leggermente più semplice generare testo usando questo formato.</span><span class="sxs-lookup"><span data-stu-id="bf156-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="bf156-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="bf156-112">Subtype</span></span>            | <span data-ttu-id="bf156-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf156-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="bf156-114">\_AI44 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="bf156-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="bf156-115">Per la sovrimpressione di immagini e testo.</span><span class="sxs-lookup"><span data-stu-id="bf156-115">For subpicture and text overlays.</span></span> <span data-ttu-id="bf156-116">Vedere la descrizione precedente.</span><span class="sxs-lookup"><span data-stu-id="bf156-116">See previous description.</span></span> |
| <span data-ttu-id="bf156-117">\_IA44 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="bf156-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="bf156-118">Per la sovrimpressione di immagini e testo.</span><span class="sxs-lookup"><span data-stu-id="bf156-118">For subpicture and text overlays.</span></span> <span data-ttu-id="bf156-119">Vedere la descrizione precedente.</span><span class="sxs-lookup"><span data-stu-id="bf156-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bf156-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf156-120">Requirements</span></span>



| <span data-ttu-id="bf156-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf156-121">Requirement</span></span> | <span data-ttu-id="bf156-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bf156-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf156-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf156-123">Header</span></span><br/> | <dl> <span data-ttu-id="bf156-124"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf156-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf156-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf156-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf156-126">Sottotipi video</span><span class="sxs-lookup"><span data-stu-id="bf156-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




