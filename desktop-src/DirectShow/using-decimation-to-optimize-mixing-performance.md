---
description: Uso della decimazione per ottimizzare le prestazioni di combinazione
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Uso della decimazione per ottimizzare le prestazioni di combinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883102"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="5d3a3-103">Uso della decimazione per ottimizzare le prestazioni di combinazione</span><span class="sxs-lookup"><span data-stu-id="5d3a3-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d3a3-104">L'ottimizzazione descritta in questa sezione dipende molto dall'hardware sottostante.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="5d3a3-105">A meno che non sia possibile garantire il tipo di hardware grafico che verrà usato con l'applicazione, l'aspetto dell'immagine video potrebbe risultare grave.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="5d3a3-106">Per HDTV è necessaria una quantità elevata di potenza di elaborazione, che nei sistemi più recenti viene fornita principalmente dalla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="5d3a3-107">Tuttavia, anche se la scheda grafica e il decodificatore sono in grado di supportare le risoluzioni di 1920x1080, è possibile che l'utente non abbia sempre il proprio monitor impostato su questa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="5d3a3-108">In questo caso, il chip grafico è necessario per creare un'immagine 1920 x 1080, quindi ridurre la risoluzione prima di inviarla al buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="5d3a3-109">Poiché si tratta di una perdita di potenza di elaborazione, VMR offre un modo per decimare (ridurre) l'immagine nel momento in cui viene eseguito il rendering sulla superficie di DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="5d3a3-110">In questo modo si elimina la copia di memoria aggiuntiva necessaria se l'immagine deve essere ridimensionata dopo il rendering.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="5d3a3-111">**VMR-7:** Per abilitare la decimazione, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il \_ flag DecimateOutput di MixerPref.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="5d3a3-112">**VMR-9:** Per abilitare la decimazione, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag DecimateOutput di MixerPref9.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="5d3a3-113">Il metodo **SetMixingPrefs** deve essere chiamato prima della connessione di VMR.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="5d3a3-114">I flag di preferenza di combinazione non possono essere modificati dopo l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="5d3a3-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d3a3-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d3a3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3a3-116">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="5d3a3-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



