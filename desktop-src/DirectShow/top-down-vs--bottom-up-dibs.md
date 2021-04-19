---
description: Confronto tra Top-Down e
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down rispetto a Bottom-Up
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313414"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="25967-103">Top-Down rispetto a Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="25967-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="25967-104">Se non si ha familiarità con la programmazione grafica, è possibile che una bitmap venga disposta nella memoria in modo che la riga superiore dell'immagine venga visualizzata all'inizio del buffer, seguita dalla riga successiva e così via.</span><span class="sxs-lookup"><span data-stu-id="25967-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="25967-105">Tuttavia, questo non è necessariamente il caso.</span><span class="sxs-lookup"><span data-stu-id="25967-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="25967-106">In Windows, le bitmap indipendenti dal dispositivo (DIB) possono essere posizionate in memoria in due diversi orientamenti, dal basso verso l'alto e dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="25967-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="25967-107">In una DIB dal basso in alto, il buffer dell'immagine inizia con la riga inferiore di pixel, seguita dalla riga successiva e così via.</span><span class="sxs-lookup"><span data-stu-id="25967-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="25967-108">La riga superiore dell'immagine è l'ultima riga nel buffer.</span><span class="sxs-lookup"><span data-stu-id="25967-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="25967-109">Il primo byte in memoria è pertanto il pixel inferiore sinistro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="25967-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="25967-110">In GDI tutte le mie priorità sono dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="25967-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="25967-111">Il diagramma seguente illustra il layout fisico di una DIB dal basso in alto.</span><span class="sxs-lookup"><span data-stu-id="25967-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![parte superiore della DIB](images/pixel-layout-bottomup.png)

<span data-ttu-id="25967-113">In una DIB dall'alto verso il basso l'ordine delle righe viene invertito.</span><span class="sxs-lookup"><span data-stu-id="25967-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="25967-114">La riga superiore dell'immagine è la prima riga in memoria, seguita dalla riga successiva.</span><span class="sxs-lookup"><span data-stu-id="25967-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="25967-115">La riga inferiore dell'immagine è l'ultima riga nel buffer.</span><span class="sxs-lookup"><span data-stu-id="25967-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="25967-116">Con una DIB dall'alto in basso, il primo byte in memoria è il pixel superiore sinistro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="25967-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="25967-117">DirectDraw utilizza l'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="25967-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="25967-118">Il diagramma seguente illustra il layout fisico di una DIB dall'alto verso il basso:</span><span class="sxs-lookup"><span data-stu-id="25967-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![DIB dall'alto in basso](images/pixel-layout-topdown.png)

<span data-ttu-id="25967-120">Per la priorità RGB, l'orientamento dell'immagine è indicato dal membro **biHeight** della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="25967-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="25967-121">Se **biHeight** è un valore positivo, l'immagine è dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="25967-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="25967-122">Se **biHeight** è negativo, l'immagine è dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="25967-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="25967-123">Le priorità nei formati YUV sono sempre dall'alto verso il basso e il segno del membro **biHeight** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="25967-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="25967-124">I decodificatori devono offrire formati YUV con una **bialtezza** positiva, ma devono accettare anche formati YUV con una **bialtezza** negativa e ignorare il segno.</span><span class="sxs-lookup"><span data-stu-id="25967-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="25967-125">Inoltre, qualsiasi tipo di DIB che usa un **fourcc** nel membro di **bicompressione** deve esprimere la propria **bialtezza** come numero positivo, indipendentemente dall'orientamento, poiché il **fourcc** stesso identifica uno schema di compressione il cui orientamento dell'immagine deve essere compreso da qualsiasi filtro compatibile.</span><span class="sxs-lookup"><span data-stu-id="25967-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25967-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25967-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25967-127">Utilizzo di fotogrammi video</span><span class="sxs-lookup"><span data-stu-id="25967-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



