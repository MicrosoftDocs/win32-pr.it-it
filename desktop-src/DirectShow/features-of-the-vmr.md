---
description: Funzionalità di VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Funzionalità di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304390"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="7f6fb-103">Funzionalità di VMR</span><span class="sxs-lookup"><span data-stu-id="7f6fb-103">Features of the VMR</span></span>

<span data-ttu-id="7f6fb-104">Il video che combina il renderer 7 (VMR-7) supporta le seguenti nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="7f6fb-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="7f6fb-105">Combinazione reale di più flussi video, usando le funzionalità di fusione alfa dei dispositivi hardware Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="7f6fb-106">La possibilità di collegare il proprio componente di composizione per implementare gli effetti e le transizioni tra più flussi video che entrano in VMR.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="7f6fb-107">Vero rendering senza finestra.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-107">True windowless rendering.</span></span> <span data-ttu-id="7f6fb-108">Non è più necessario rendere la finestra di riproduzione del video un figlio della finestra dell'applicazione per poter contenere la riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="7f6fb-109">La nuova modalità di rendering senza finestra di VMR consente alle applicazioni di ospitare facilmente la riproduzione video in qualsiasi finestra senza dover inviare i messaggi della finestra al renderer per l'elaborazione specifica del renderer.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="7f6fb-110">Nuova modalità di riproduzione con rendering in cui le applicazioni possono fornire il proprio componente allocatore per ottenere l'accesso all'immagine video decodificata prima che venga visualizzata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="7f6fb-111">Supporto migliorato per i PC dotati di più monitor.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="7f6fb-112">Supporto per la nuova architettura di accelerazione video DirectX Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="7f6fb-113">Supporto per la riproduzione video di alta qualità simultaneamente su più finestre.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="7f6fb-114">Supporto per la modalità esclusiva di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="7f6fb-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="7f6fb-115">100% di compatibilità con le versioni precedenti delle applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="7f6fb-116">Supporto per l'esecuzione dei frame e un modo affidabile per acquisire l'immagine corrente da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="7f6fb-117">La possibilità per le applicazioni di incorporare facilmente i dati di immagini statiche, ad esempio i loghi dei canali o i componenti dell'interfaccia utente, con il video in modo senza sfarfallio.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="7f6fb-118">VMR-9 supporta tutte le funzionalità sopra elencate, oltre a:</span><span class="sxs-lookup"><span data-stu-id="7f6fb-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="7f6fb-119">Possibilità di elaborare i dati video direttamente con le API Direct3D, ad esempio i pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="7f6fb-120">Supporto migliorato per contenuto video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="7f6fb-121">Supporto per qualsiasi piattaforma supportata da DirectX.</span><span class="sxs-lookup"><span data-stu-id="7f6fb-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f6fb-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f6fb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6fb-123">Informazioni sul rendering del mixaggio video</span><span class="sxs-lookup"><span data-stu-id="7f6fb-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



