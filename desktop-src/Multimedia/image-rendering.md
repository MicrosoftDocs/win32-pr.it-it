---
title: Rendering di immagini
description: Rendering di immagini
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, rendering di immagini
- DrawDib, disegno di DIB
- DrawDibDraw (funzione)
- DrawDibGetBuffer (funzione)
- DrawDibUpdate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045284"
---
# <a name="image-rendering"></a><span data-ttu-id="5ae9d-108">Rendering di immagini</span><span class="sxs-lookup"><span data-stu-id="5ae9d-108">Image Rendering</span></span>

<span data-ttu-id="5ae9d-109">Dopo aver chiamato [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) per creare un controller di dominio DrawDib (vedere [operazioni DrawDib](drawdib-operations.md)), è possibile creare una DIB sullo schermo usando la funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="5ae9d-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="5ae9d-110">**DrawDibDraw** presenta le bitmap con colori reali quando vengono visualizzate con adattatori video a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="5ae9d-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="5ae9d-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) supporta anche i compressione video in modo trasparente quando si visualizzano le bitmap compresse.</span><span class="sxs-lookup"><span data-stu-id="5ae9d-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="5ae9d-112">È possibile accedere al buffer che contiene l'immagine decompressa usando la funzione [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="5ae9d-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="5ae9d-113">**DrawDibGetBuffer** restituisce **null** quando si disegna una bitmap non compressa.</span><span class="sxs-lookup"><span data-stu-id="5ae9d-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="5ae9d-114">È necessario preparare l'applicazione per gestire le bitmap compresse e non compresse.</span><span class="sxs-lookup"><span data-stu-id="5ae9d-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="5ae9d-115">È possibile aggiornare un'immagine o una parte di un'immagine visualizzata dall'applicazione usando la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .</span><span class="sxs-lookup"><span data-stu-id="5ae9d-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ae9d-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ae9d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae9d-117">Informazioni sulle funzioni DrawDib</span><span class="sxs-lookup"><span data-stu-id="5ae9d-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




