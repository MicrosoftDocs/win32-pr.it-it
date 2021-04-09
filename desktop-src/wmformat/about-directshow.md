---
title: Informazioni su DirectShow (Windows Media Format 11 SDK)
description: Informazioni su DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047745"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="9cc8b-107">Informazioni su DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="9cc8b-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9cc8b-108">DirectShow è un'architettura di streaming di dati di alto livello, modulare, estendibile e modulare per la piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="9cc8b-109">Fornisce i componenti software e le API (Application Programming Interface) sottostanti per un'ampia gamma di applicazioni audio e video digitali sul mercato.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="9cc8b-110">DirectShow è disponibile come parte di Microsoft DirectX Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="9cc8b-111">Per ulteriori informazioni su DirectShow, vedere Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="9cc8b-112">In DirectShow tutti i componenti del flusso di dati sono denominati *filtri*.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="9cc8b-113">Un filtro può rappresentare un dispositivo hardware, un codificatore software o un decodificatore, un renderer audio o video o qualsiasi funzionalità di elaborazione video audio.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="9cc8b-114">Per consentire alle applicazioni basate su DirectShow di leggere e scrivere contenuto in formato Windows Media, incluso il contenuto protetto da Digital Rights Management (DRM), Microsoft offre due filtri che incapsulano parti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="9cc8b-115">Si tratta del [lettore WM ASF](wm-asf-reader-filter.md) e del [writer ASF WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9cc8b-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="9cc8b-116">Questi filtri e le interfacce che espongono sono collettivamente denominati componenti QASF, dopo la DLL in cui sono inclusi nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="9cc8b-117">(Q sta per quarzo, un nome di codice iniziale per DirectShow).</span><span class="sxs-lookup"><span data-stu-id="9cc8b-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="9cc8b-118">L'uso dei codec della serie Windows Media Audio e video 9 con i componenti DirectShow QASF richiede Microsoft Windows Millennium Edition o versione successiva o DirectX 8,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="9cc8b-119">Il diagramma seguente mostra un grafico filtro DirectShow per la riproduzione di file di Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![grafico di riproduzione video di Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="9cc8b-121">Il [lettore di WM ASF](wm-asf-reader-filter.md) è un componente qasf, i decodificatori sono componenti Windows Media Format SDK ospitati nel filtro del wrapper DMO (un componente QASF) e i renderer sono componenti DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9cc8b-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




