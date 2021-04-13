---
description: Introduzione ai servizi di modifica DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introduzione ai servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481613"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="a5ee2-103">Introduzione ai servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5ee2-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="a5ee2-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a5ee2-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a5ee2-105">Il nucleo di DirectShow è un'architettura potente per la gestione dei flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="a5ee2-106">Un'applicazione può usarla per riprodurre contenuti multimediali creati in un'ampia gamma di formati, senza che lo sviluppatore debba preoccuparsi della compressione dei file e di altri dettagli noiosi.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="a5ee2-107">Prima di [DirectShow editing Services](directshow-editing-services.md) (des), tuttavia, DirectShow non aveva la flessibilità necessaria per la modifica non lineare.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="a5ee2-108">Si supponga, ad esempio, di voler creare una sequenza video composta da 4 secondi dall'origine A, seguita da 10 secondi dall'origine B, fino a 5 secondi dall'origine C. È possibile eseguire questa operazione in modo molto semplice usando solo l'API DirectShow di base.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="a5ee2-109">Tuttavia, se si è deciso che l'origine C deve precedere l'origine B, non dopo; che la sequenza usi 8 secondi dall'origine A, non 4; e che l'intera produzione avesse bisogno di una traccia audio separata in background?</span><span class="sxs-lookup"><span data-stu-id="a5ee2-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="a5ee2-110">Anche le modifiche minime, ad esempio, potrebbero essere difficili da implementare.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="a5ee2-111">Tuttavia, lo scenario appena descritto è un semplice progetto di modifica in DES: è possibile eseguire questa operazione con alcune chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="a5ee2-112">Di seguito sono riportate alcune delle funzionalità che DES apporta a DirectShow:</span><span class="sxs-lookup"><span data-stu-id="a5ee2-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="a5ee2-113">Modello di sequenza temporale che organizza tracce video e audio in livelli annidati, semplificando la manipolazione della produzione finale</span><span class="sxs-lookup"><span data-stu-id="a5ee2-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="a5ee2-114">La possibilità di visualizzare in tempo reale un progetto video</span><span class="sxs-lookup"><span data-stu-id="a5ee2-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="a5ee2-115">Persistenza del progetto tramite un formato basato su XML</span><span class="sxs-lookup"><span data-stu-id="a5ee2-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="a5ee2-116">Supporto per effetti audio e video, nonché transizioni tra tracce video, ad esempio dissolvenze e cancellazioni.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="a5ee2-117">Oltre 100 salviettine standard, come definito dalla società di Motion Picture and Television Engineers (SMPTE)</span><span class="sxs-lookup"><span data-stu-id="a5ee2-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="a5ee2-118">Digitazione in base a tonalità, luminanza, valore RGB o valore alfa</span><span class="sxs-lookup"><span data-stu-id="a5ee2-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="a5ee2-119">Conversione automatica delle frequenze dei fotogrammi e del campionamento audio, consentendo a un ambiente di produzione di utilizzare origini eterogenee</span><span class="sxs-lookup"><span data-stu-id="a5ee2-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="a5ee2-120">Ridimensionamento o ritaglio di video</span><span class="sxs-lookup"><span data-stu-id="a5ee2-120">Resizing or cropping of video</span></span>

<span data-ttu-id="a5ee2-121">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="a5ee2-121">Limitations:</span></span>

-   <span data-ttu-id="a5ee2-122">DES non supporta le origini video MPEG-2 o H. 264.</span><span class="sxs-lookup"><span data-stu-id="a5ee2-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5ee2-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5ee2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ee2-124">Servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5ee2-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



