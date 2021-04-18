---
description: Uso del sink di supporto EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del sink di supporto EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320798"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="e4f63-103">Uso del sink di supporto EVR</span><span class="sxs-lookup"><span data-stu-id="e4f63-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="e4f63-104">Il sink multimediale EVR (Enhanced video renderer) può essere usato come componente autonomo.</span><span class="sxs-lookup"><span data-stu-id="e4f63-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="e4f63-105">Più spesso, tuttavia, un'applicazione creerà il sink del supporto EVR all'interno di una topologia e quindi utilizzerà la sessione multimediale per controllare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e4f63-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="e4f63-106">Esistono due modi per creare il sink di supporto EVR:</span><span class="sxs-lookup"><span data-stu-id="e4f63-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="e4f63-107">La funzione [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="e4f63-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="e4f63-108">La funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un oggetto Activation per il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="e4f63-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="e4f63-109">Il sink del supporto EVR inizialmente ha un sink di flusso, che corrisponde al flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="e4f63-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="e4f63-110">Per aggiungere nuovi sink di flusso, chiamare [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="e4f63-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f63-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4f63-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f63-112">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="e4f63-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="e4f63-113">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="e4f63-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



