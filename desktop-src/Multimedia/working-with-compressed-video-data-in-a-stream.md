---
title: Utilizzo di dati video compressi in un flusso
description: Utilizzo di dati video compressi in un flusso
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046638"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="fbad4-103">Utilizzo di dati video compressi in un flusso</span><span class="sxs-lookup"><span data-stu-id="fbad4-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="fbad4-104">AVIFile offre diversi modi per accedere ai flussi video compressi.</span><span class="sxs-lookup"><span data-stu-id="fbad4-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="fbad4-105">Se si desidera visualizzare uno o più frame di un flusso video compresso, è possibile recuperare i frame utilizzando la funzione [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) e inviando i dati del frame compresso alle funzioni DrawDib per visualizzarli.</span><span class="sxs-lookup"><span data-stu-id="fbad4-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="fbad4-106">Le funzioni DrawDib possono visualizzare immagini di diverse profondità dell'immagine e dithering automatico delle immagini per le visualizzazioni che non possono gestire determinati tipi di bitmap indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbad4-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="fbad4-107">Queste funzioni funzionano con immagini non compresse e compresse.</span><span class="sxs-lookup"><span data-stu-id="fbad4-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="fbad4-108">Per ulteriori informazioni sulle funzioni DrawDib, vedere [funzioni DrawDib](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fbad4-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="fbad4-109">AVIFile fornisce funzioni per la decompressione di un singolo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="fbad4-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="fbad4-110">Per allocare le risorse, usare la funzione [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) .</span><span class="sxs-lookup"><span data-stu-id="fbad4-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="fbad4-111">Questa funzione crea un buffer per i dati decompressi.</span><span class="sxs-lookup"><span data-stu-id="fbad4-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="fbad4-112">È possibile decomprimere un singolo fotogramma video usando la funzione [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) .</span><span class="sxs-lookup"><span data-stu-id="fbad4-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="fbad4-113">Questa funzione decomprime il frame e recupera un frame completo di dati dell'immagine, restituendo l'indirizzo della DIB nella struttura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fbad4-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="fbad4-114">L'applicazione può visualizzare la DIB usando le funzioni di disegno standard o le funzioni DrawDib.</span><span class="sxs-lookup"><span data-stu-id="fbad4-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="fbad4-115">Se l'applicazione effettua chiamate successive a **AVIStreamGetFrame**, la funzione sovrascrive il buffer con ogni frame recuperato.</span><span class="sxs-lookup"><span data-stu-id="fbad4-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="fbad4-116">Quando si termina l'uso di **AVIStreamGetFrame** e la DIB decompressa si trova nel buffer, è possibile rilasciare le risorse allocate usando la funzione [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .</span><span class="sxs-lookup"><span data-stu-id="fbad4-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="fbad4-117">Per ulteriori informazioni sulla decompressione delle immagini, vedere [Gestione compressione video](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="fbad4-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 