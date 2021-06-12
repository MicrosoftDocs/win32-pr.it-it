---
title: Informazioni su DirectShow in Windows Media Format 11 SDK, un'architettura di streaming di dati di alto livello, modulare, estendibile per la piattaforma Windows.
description: Informazioni su DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format),DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011294"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="cae49-107">Informazioni su DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="cae49-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="cae49-108">DirectShow è un'architettura di flusso dei dati di alto livello, modulare, estendibile e di streaming dei dati per la piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="cae49-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="cae49-109">Fornisce i componenti software sottostanti e le API (Application Programming Interface) per un'ampia gamma di applicazioni audio e video digitali attualmente disponibili sul mercato.</span><span class="sxs-lookup"><span data-stu-id="cae49-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="cae49-110">DirectShow è disponibile come parte di Microsoft DirectX Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="cae49-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="cae49-111">Per altre informazioni su DirectShow, vedere Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="cae49-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="cae49-112">In DirectShow tutti i componenti di streaming dei dati sono denominati *filtri*.</span><span class="sxs-lookup"><span data-stu-id="cae49-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="cae49-113">Un filtro può rappresentare un dispositivo hardware, un codificatore software o un decodificatore, un renderer audio o video o qualsiasi funzionalità di elaborazione audio-video.</span><span class="sxs-lookup"><span data-stu-id="cae49-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="cae49-114">Per consentire alle applicazioni basate su DirectShow di leggere e scrivere contenuto di Windows Media Format, incluso il contenuto protetto da Digital Rights Management (DRM), Microsoft fornisce due filtri che incapsulano parti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cae49-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="cae49-115">Si tratta del [lettore ASF WM](wm-asf-reader-filter.md) e [di WM ASF Writer.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="cae49-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="cae49-116">Questi filtri e le interfacce che espongono vengono collettivamente definiti componenti QASF, dopo la DLL in cui sono in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cae49-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="cae49-117">La Q è l'acronimo di Quartz, un nome in codice iniziale per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cae49-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="cae49-118">L'uso dei codec Windows Media Audio e Video 9 tramite i componenti QASF DirectShow richiede Microsoft Windows Millennium Edition o versione successiva o DirectX 8.0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="cae49-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="cae49-119">Il diagramma seguente mostra un grafico di filtro DirectShow per la riproduzione Windows Media Video file.</span><span class="sxs-lookup"><span data-stu-id="cae49-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Grafico di riproduzione di video multimediali di Windows](images/wmv-wmasfreader.png)

<span data-ttu-id="cae49-121">Wm [ASF Reader](wm-asf-reader-filter.md) è un componente QASF, i decodificatori sono componenti di Windows Media Format SDK ospitati nel filtro wrapper DMO (un componente QASF) e i renderer sono componenti DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cae49-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




