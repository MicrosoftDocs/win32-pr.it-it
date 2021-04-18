---
description: Interfacce di acquisizione e rendering audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfacce di acquisizione e rendering audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304255"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="c4f04-103">Interfacce di acquisizione e rendering audio</span><span class="sxs-lookup"><span data-stu-id="c4f04-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="c4f04-104">Queste interfacce supportano l'acquisizione e il rendering audio in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c4f04-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="c4f04-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="c4f04-105">Interface</span></span>                                              | <span data-ttu-id="c4f04-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4f04-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4f04-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="c4f04-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="c4f04-108">Accedere agli input analoghi sulla scheda audio del sistema e modificare le caratteristiche, ad esempio mono o stereo, livello di combinazione, livello pan, sonorità, acute e bassi.</span><span class="sxs-lookup"><span data-stu-id="c4f04-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="c4f04-109">**IAMAudioRendererStats**</span><span class="sxs-lookup"><span data-stu-id="c4f04-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="c4f04-110">Ottenere informazioni statistiche sulle prestazioni relative al renderer audio.</span><span class="sxs-lookup"><span data-stu-id="c4f04-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="c4f04-111">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="c4f04-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="c4f04-112">Controllare il modo in cui il filtro di acquisizione audio alloca i buffer.</span><span class="sxs-lookup"><span data-stu-id="c4f04-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="c4f04-113">**IAMClockSlave**</span><span class="sxs-lookup"><span data-stu-id="c4f04-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="c4f04-114">Controllare la tolleranza di un renderer audio quando corrisponde a frequenze con un altro Clock.</span><span class="sxs-lookup"><span data-stu-id="c4f04-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="c4f04-115">**IAMDirectSound**</span><span class="sxs-lookup"><span data-stu-id="c4f04-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="c4f04-116">Consente a un'applicazione di specificare quale finestra ha lo stato attivo per il controllo della riproduzione di audio DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c4f04-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="c4f04-117">**IAMResourceControl**</span><span class="sxs-lookup"><span data-stu-id="c4f04-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="c4f04-118">Mantenere una risorsa del dispositivo audio prima che sia necessaria.</span><span class="sxs-lookup"><span data-stu-id="c4f04-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="c4f04-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="c4f04-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="c4f04-120">Eseguire una query e impostare il formato di output del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c4f04-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="c4f04-121">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="c4f04-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="c4f04-122">Imposta volume e bilancia di output audio.</span><span class="sxs-lookup"><span data-stu-id="c4f04-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="c4f04-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4f04-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f04-124">Interfacce</span><span class="sxs-lookup"><span data-stu-id="c4f04-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



