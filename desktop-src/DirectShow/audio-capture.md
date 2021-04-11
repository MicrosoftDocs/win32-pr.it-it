---
description: Acquisizione audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342016"
---
# <a name="audio-capture"></a><span data-ttu-id="1bd9a-103">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="1bd9a-103">Audio Capture</span></span>

<span data-ttu-id="1bd9a-104">Un'applicazione può usare DirectShow per acquisire dati audio da microfoni, lettori di nastri e altri dispositivi, tramite gli input nella scheda audio.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="1bd9a-105">Gli scenari tipici includono:</span><span class="sxs-lookup"><span data-stu-id="1bd9a-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="1bd9a-106">Registrazione di una narrazione VoiceOver per il duplicato successivo su un flusso video.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="1bd9a-107">Conversione del contenuto audio analogico legacy in formato digitale.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="1bd9a-108">Acquisizione di voce o musica per la trasmissione in rete.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="1bd9a-109">Gli utenti finali hanno diverse opzioni per l'acquisizione di audio dalla scheda audio al disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="1bd9a-110">La maggior parte delle schede fornisce applicazioni per la combinazione e la registrazione dagli input audio.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="1bd9a-111">Windows fornisce un registratore audio, una semplice applicazione di utilità per la registrazione da un microfono.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="1bd9a-112">Il codificatore Windows Media può essere incorporato in un'applicazione DirectShow come [oggetto DMO (DirectX Media Object](directx-media-objects.md) ).</span><span class="sxs-lookup"><span data-stu-id="1bd9a-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="1bd9a-113">Questa sezione descrive come integrare la funzionalità di acquisizione audio all'interno dell'applicazione usando DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1bd9a-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="1bd9a-114">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="1bd9a-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1bd9a-115">Informazioni sul filtro di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="1bd9a-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="1bd9a-116">Selezione di un dispositivo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="1bd9a-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="1bd9a-117">Creazione di un grafico di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="1bd9a-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="1bd9a-118">Creazione di un grafico di acquisizione audio con anteprima</span><span class="sxs-lookup"><span data-stu-id="1bd9a-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="1bd9a-119">Impostazione delle proprietà di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="1bd9a-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="1bd9a-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bd9a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd9a-121">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="1bd9a-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



