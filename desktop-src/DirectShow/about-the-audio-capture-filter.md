---
description: Informazioni sul filtro di acquisizione audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Informazioni sul filtro di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125280"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="8ab79-103">Informazioni sul filtro di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="8ab79-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="8ab79-104">DirectShow consente l'acquisizione dagli input analoghi in una scheda audio tramite il [filtro di acquisizione audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8ab79-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="8ab79-105">Questo filtro usa le API di WaveIn *xxx* per controllare qualsiasi dispositivo il cui driver supporta queste API.</span><span class="sxs-lookup"><span data-stu-id="8ab79-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="8ab79-106">Ogni scheda del sistema è rappresentata da un'istanza separata del filtro.</span><span class="sxs-lookup"><span data-stu-id="8ab79-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="8ab79-107">Il filtro di acquisizione audio espone ogni input sulla scheda, ad esempio il microfono o l'input MIDI, come un pin di input.</span><span class="sxs-lookup"><span data-stu-id="8ab79-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="8ab79-108">I pin di input rappresentano gli elementi esposti dal driver come righe di origine audio.</span><span class="sxs-lookup"><span data-stu-id="8ab79-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="8ab79-109">Tuttavia, non vengono trasmessi dati attraverso questi pin di input e non si connettono ad altri filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8ab79-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="8ab79-110">Forniscono semplicemente un modo per consentire a un'applicazione di controllare gli input.</span><span class="sxs-lookup"><span data-stu-id="8ab79-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="8ab79-111">L'applicazione può usare un pin di input per abilitare o disabilitare l'input o per impostare le proprietà di combinazione, ad esempio la equalizzazione dei bassi, l'equalizzazione degli acuti, il Pan e così via.</span><span class="sxs-lookup"><span data-stu-id="8ab79-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="8ab79-112">La quantità di controllo disponibile dipende dal driver.</span><span class="sxs-lookup"><span data-stu-id="8ab79-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="8ab79-113">Per comprendere e sfruttare appieno le funzionalità di una scheda audio specifica, sarà necessaria la documentazione del produttore della scheda.</span><span class="sxs-lookup"><span data-stu-id="8ab79-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="8ab79-114">È possibile acquisire dall'input di CD-Audio, ma questo flusso audio è già passato attraverso il convertitore da digitale a analogico, quindi si verifica una perdita di qualità del suono dal CD originale.</span><span class="sxs-lookup"><span data-stu-id="8ab79-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ab79-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ab79-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab79-116">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="8ab79-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



