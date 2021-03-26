---
description: Per creare una bitmap, usare la funzione CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226713"
---
# <a name="bitmap-creation"></a><span data-ttu-id="e490c-103">Creazione di bitmap</span><span class="sxs-lookup"><span data-stu-id="e490c-103">Bitmap Creation</span></span>

<span data-ttu-id="e490c-104">Per creare una bitmap, usare la funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span><span class="sxs-lookup"><span data-stu-id="e490c-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="e490c-105">Queste funzioni consentono di specificare la larghezza e l'altezza, in pixel, della bitmap.</span><span class="sxs-lookup"><span data-stu-id="e490c-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="e490c-106">La funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) consente inoltre di specificare il numero di piani di colore e il numero di bit necessari per identificare il colore.</span><span class="sxs-lookup"><span data-stu-id="e490c-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="e490c-107">D'altra parte, le funzioni [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usano un contesto di dispositivo specifico per ottenere il numero di piani di colore e il numero di bit necessari per identificare il colore.</span><span class="sxs-lookup"><span data-stu-id="e490c-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="e490c-108">La funzione [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea una bitmap dipendente dal dispositivo da una bitmap indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e490c-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="e490c-109">Contiene una tabella colori che descrive il modo in cui i valori dei pixel corrispondono ai valori dei colori RGB.</span><span class="sxs-lookup"><span data-stu-id="e490c-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="e490c-110">Per altre informazioni, vedere [bitmap dipendenti dal dispositivo](device-dependent-bitmaps.md) e [bitmap indipendenti dal dispositivo](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="e490c-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="e490c-111">Dopo la creazione della bitmap, non è possibile modificarne le dimensioni, il numero di piani di colore o il numero di bit necessari per identificare il colore.</span><span class="sxs-lookup"><span data-stu-id="e490c-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="e490c-112">Quando non è più necessaria una bitmap, chiamare la funzione [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) per eliminarla.</span><span class="sxs-lookup"><span data-stu-id="e490c-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



