---
description: Informazioni sui dispositivi di acquisizione video
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informazioni sui dispositivi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746375"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="4159a-103">Informazioni sui dispositivi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="4159a-103">About Video Capture Devices</span></span>

<span data-ttu-id="4159a-104">La maggior parte dei nuovi dispositivi di acquisizione video usa i driver Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="4159a-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="4159a-105">Nell'architettura WDM Microsoft fornisce un set di driver indipendenti dall'hardware, detti driver di classe, e il fornitore dell'hardware fornisce i minidriver specifici dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="4159a-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="4159a-106">Un minidriver implementa tutte le funzioni specifiche del dispositivo. per la maggior parte delle funzioni, minidriver chiama il driver di classe Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4159a-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="4159a-107">In un grafico di filtro DirectShow, qualsiasi dispositivo di acquisizione WDM viene visualizzato come filtro di [acquisizione video WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="4159a-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="4159a-108">Il filtro di acquisizione video WDM si configura in base alle caratteristiche del driver.</span><span class="sxs-lookup"><span data-stu-id="4159a-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="4159a-109">Viene visualizzato con un nome fornito dal driver. non verrà visualizzato un filtro denominato "Filtro acquisizione video WDM" in qualsiasi punto del grafico.</span><span class="sxs-lookup"><span data-stu-id="4159a-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="4159a-110">Alcuni dispositivi di acquisizione precedenti utilizzano ancora driver video for Windows (VFW).</span><span class="sxs-lookup"><span data-stu-id="4159a-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="4159a-111">Sebbene questi driver siano obsoleti, sono supportati in DirectShow tramite il filtro di [acquisizione VFW](vfw-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="4159a-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4159a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4159a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4159a-113">Informazioni su acquisizione video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4159a-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



