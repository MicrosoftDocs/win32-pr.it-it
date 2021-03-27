---
title: Novità dell'SDK di agosto 2009 per Windows 7/Direct3D 11
description: Questa versione di Windows 7/Direct3D 11 viene fornita come parte di DirectX SDK e contiene nuove funzionalità, strumenti e documentazione.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731559"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="0819f-103">Novità dell'SDK di agosto 2009 per Windows 7/Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0819f-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="0819f-104">Questa versione di Windows 7/Direct3D 11 viene fornita come parte di DirectX SDK e contiene nuove funzionalità, strumenti e documentazione.</span><span class="sxs-lookup"><span data-stu-id="0819f-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0819f-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="0819f-105">Item</span></span></th>
<th><span data-ttu-id="0819f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0819f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0819f-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="0819f-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="0819f-108">Direct2D è un'API grafica 2D, con accelerazione immediata e in modalità immediata, che offre prestazioni elevate e rendering di elevata qualità per la geometria 2D, le bitmap e il testo.</span><span class="sxs-lookup"><span data-stu-id="0819f-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="0819f-109">L'API Direct2D è progettata per interagire correttamente con Direct3D e GDI.</span><span class="sxs-lookup"><span data-stu-id="0819f-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="0819f-110">Questo SDK consente agli sviluppatori di valutare l'API e scrivere semplici applicazioni, con alcune delle funzionalità più avanzate possibile nei computer configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0819f-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="0819f-111">La <a href="/windows/win32/direct2d/direct2d-portal">documentazione</a> e gli <a href="/previous-versions//dd372354(v=vs.85)">esempi</a> per Direct2D sono attualmente disponibili su MSDN.</span><span class="sxs-lookup"><span data-stu-id="0819f-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0819f-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0819f-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="0819f-113">DirectWrite fornisce il supporto per il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione, il supporto completo per testo e layout Unicode e molto altro ancora:</span><span class="sxs-lookup"><span data-stu-id="0819f-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="0819f-114">Sistema di layout del testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0819f-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="0819f-115">Rendering di testo di alta qualità, sottopixel e ClearType in grado di utilizzare GDI Direct3D, Direct2D o la tecnologia di rendering specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0819f-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="0819f-116">Supporto per il testo in più formati.</span><span class="sxs-lookup"><span data-stu-id="0819f-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="0819f-117">Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.</span><span class="sxs-lookup"><span data-stu-id="0819f-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="0819f-118">Supporto per il layout e il rendering del testo in tutte le lingue supportate da Windows.</span><span class="sxs-lookup"><span data-stu-id="0819f-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="0819f-119">Questo SDK consente agli sviluppatori di valutare l'API e scrivere applicazioni di base solo a scopo dimostrativo.</span><span class="sxs-lookup"><span data-stu-id="0819f-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="0819f-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentazione</a> ed <a href="/windows/win32/directwrite/samples">esempi</a> per DirectWrite sono attualmente disponibili su MSDN.</span><span class="sxs-lookup"><span data-stu-id="0819f-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0819f-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="0819f-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="0819f-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> si basa su DXGI 1,0 e sarà disponibile sia in Windows Vista che in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0819f-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="0819f-123">DXGI 1,1 aggiunge diverse nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="0819f-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="0819f-124">Supporto delle superfici condivise sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="0819f-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="0819f-125">Ciò consente una condivisione efficiente della superficie di lettura e scrittura tra più dispositivi D3D (potrebbe essere compreso tra D3D10 e D3D11).</span><span class="sxs-lookup"><span data-stu-id="0819f-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="0819f-126">Supporto del formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="0819f-126">BGRA format support.</span></span> <span data-ttu-id="0819f-127">In questo modo è possibile eseguire il rendering di GDI nella stessa superficie DXGI di destinazione di un dispositivo Direct2D, Direct3D 10,1 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="0819f-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="0819f-128">Latenza massima del frame.</span><span class="sxs-lookup"><span data-stu-id="0819f-128">Maximum Frame Latency.</span></span> <span data-ttu-id="0819f-129">Utilizzando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, i titoli possono controllare il numero di frame che possono essere archiviati in una coda, prima dell'invio per il rendering.</span><span class="sxs-lookup"><span data-stu-id="0819f-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="0819f-130">La latenza viene spesso utilizzata per controllare il modo in cui la CPU sceglie di rispondere all'input dell'utente e ai frame presenti nella coda di rendering.</span><span class="sxs-lookup"><span data-stu-id="0819f-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="0819f-131">Enumerazione dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="0819f-131">Adapter Enumeration.</span></span> <span data-ttu-id="0819f-132">Se si usa <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, i titoli possono enumerare le schede locali senza i monitoraggi o gli output collegati, nonché gli adapter con output collegati.</span><span class="sxs-lookup"><span data-stu-id="0819f-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0819f-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Esempi aggiornati</span><span class="sxs-lookup"><span data-stu-id="0819f-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="0819f-134">Questa versione include alcuni esempi nuovi e aggiornati.</span><span class="sxs-lookup"><span data-stu-id="0819f-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="0819f-135">Il nuovo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> è un'illustrazione di tecniche di elaborazione shader più avanzate che possono essere eseguite su una GPU D3D10 o d3d11.</span><span class="sxs-lookup"><span data-stu-id="0819f-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="0819f-136">L' <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">esempio HDRToneMappingCS11</a> è stato espanso per implementare gli effetti sfocatura e Bloom (oltre al mapping dei toni) usando compute shader, oltre a fornire pixel shader implementazioni per il confronto.</span><span class="sxs-lookup"><span data-stu-id="0819f-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="0819f-137">L' <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">esempio MultithreadedRendering11</a> è stato aggiornato in modo significativo, con risorse dell'arte più complesse e l'elaborazione per thread più intensiva.</span><span class="sxs-lookup"><span data-stu-id="0819f-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="0819f-138">L' <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">esempio SubD11</a> è stato aggiornato con un nuovo modello facciale e l'esempio USA ora la funzionalità di calcolo adiacenza dell'utilità di esportazione dei contenuti degli esempi.</span><span class="sxs-lookup"><span data-stu-id="0819f-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0819f-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0819f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0819f-140">Funzionalità introdotte nelle versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="0819f-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

