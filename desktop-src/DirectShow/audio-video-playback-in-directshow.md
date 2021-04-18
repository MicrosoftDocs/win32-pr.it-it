---
description: Questa esercitazione illustra come scrivere un'applicazione DirectShow che riproduce un file multimediale.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Riproduzione audio/video in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303932"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="4cc2e-103">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cc2e-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="4cc2e-104">Questa esercitazione illustra come scrivere un'applicazione DirectShow che riproduce un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="4cc2e-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="4cc2e-105">Prima di leggere questa esercitazione, è consigliabile leggere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cc2e-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="4cc2e-106">Introduzione alla programmazione di applicazioni DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cc2e-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="4cc2e-107">Come riprodurre un file</span><span class="sxs-lookup"><span data-stu-id="4cc2e-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="4cc2e-108">Informazioni sui filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cc2e-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="4cc2e-109">Informazioni su Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="4cc2e-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="4cc2e-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4cc2e-110">In this section</span></span>

-   [<span data-ttu-id="4cc2e-111">Passaggio 1: dichiarare la classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="4cc2e-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="4cc2e-112">Passaggio 2: dichiarare CVideoRenderer e classi derivate</span><span class="sxs-lookup"><span data-stu-id="4cc2e-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="4cc2e-113">Passaggio 3: creare il grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="4cc2e-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="4cc2e-114">Passaggio 4: aggiungere il renderer video</span><span class="sxs-lookup"><span data-stu-id="4cc2e-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="4cc2e-115">Passaggio 5: aggiungere funzionalità video</span><span class="sxs-lookup"><span data-stu-id="4cc2e-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="4cc2e-116">Passaggio 6: gestire gli eventi del grafo</span><span class="sxs-lookup"><span data-stu-id="4cc2e-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="4cc2e-117">Passaggio 7: controlli di trasporto</span><span class="sxs-lookup"><span data-stu-id="4cc2e-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="4cc2e-118">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cc2e-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="4cc2e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cc2e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc2e-120">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="4cc2e-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



