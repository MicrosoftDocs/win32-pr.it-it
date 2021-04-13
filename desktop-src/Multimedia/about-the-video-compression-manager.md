---
title: Informazioni su Gestione compressione video
description: Informazioni su Gestione compressione video
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows Multimedia, Gestione compressione video (VCM)
- Multimedia, Gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472947"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="70542-105">Informazioni su Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="70542-105">About the Video Compression Manager</span></span>

<span data-ttu-id="70542-106">In genere, i compressori installabili operano con dati di immagini video archiviati in file audio-video con interfoliazione (AVI).</span><span class="sxs-lookup"><span data-stu-id="70542-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="70542-107">In questa panoramica vengono illustrate le tecniche di programmazione utilizzate per accedere ai compressori installabili tramite VCM e vengono trattati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="70542-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="70542-108">VCM e il video per l'architettura di Windows</span><span class="sxs-lookup"><span data-stu-id="70542-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="70542-109">Compressione e decompressione dei dati dell'immagine dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="70542-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="70542-110">Uso dei renderer di VCM per disegnare i dati dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="70542-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="70542-111">Funzioni e strutture di VCM</span><span class="sxs-lookup"><span data-stu-id="70542-111">VCM functions and structures</span></span>

<span data-ttu-id="70542-112">Prima di leggere questa panoramica, è necessario avere familiarità con i servizi grafici di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="70542-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="70542-113">In particolare, le bitmap e le strutture correlate a bitmap, ad esempio [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), vengono usate estensivamente da VCM.</span><span class="sxs-lookup"><span data-stu-id="70542-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="70542-114">Per ulteriori informazioni sulle strutture **BITMAPINFO** e **BITMAPINFOHEADER** , vedere [bitmap](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70542-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="70542-115">Audio Compression Manager (ACM) fornisce il supporto a livello di sistema per la compressione audio e i driver di decompressione.</span><span class="sxs-lookup"><span data-stu-id="70542-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="70542-116">Per una descrizione dei servizi di compressione audio, vedere [Gestione compressione audio](audio-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="70542-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="70542-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70542-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70542-118">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="70542-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 