---
title: Interfacce livello
description: Questa sezione contiene informazioni sulle interfacce del livello.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- interfacce, livello Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993637"
---
# <a name="layer-interfaces"></a><span data-ttu-id="fe44b-104">Interfacce livello</span><span class="sxs-lookup"><span data-stu-id="fe44b-104">Layer Interfaces</span></span>

<span data-ttu-id="fe44b-105">Questa sezione contiene informazioni sulle interfacce del livello.</span><span class="sxs-lookup"><span data-stu-id="fe44b-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="fe44b-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="fe44b-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe44b-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="fe44b-107">Topic</span></span></th>
<th><span data-ttu-id="fe44b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe44b-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe44b-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="fe44b-110">Un'interfaccia di debug controlla le impostazioni di debug, convalida lo stato della pipeline e può essere usata solo se il livello di debug è attivato.</span><span class="sxs-lookup"><span data-stu-id="fe44b-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe44b-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="fe44b-112">Un'interfaccia della coda di informazioni archivia, recupera e filtra i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="fe44b-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="fe44b-113">La coda è costituita da una coda di messaggi, da uno stack di filtri di archiviazione facoltativo e da uno stack di filtri di recupero facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fe44b-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe44b-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="fe44b-115">L'interfaccia di rilevamento predefinita imposta le opzioni di rilevamento predefinite di riferimento.</span><span class="sxs-lookup"><span data-stu-id="fe44b-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe44b-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="fe44b-117">L'interfaccia di rilevamento imposta le opzioni di rilevamento dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="fe44b-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe44b-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fe44b-119">L'interfaccia <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> e i relativi metodi non sono supportati in Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="fe44b-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe44b-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe44b-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="fe44b-121">L'interfaccia del dispositivo di traccia imposta le informazioni di rilevamento dello shader, che consente la registrazione e la riproduzione accurate dell'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="fe44b-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fe44b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe44b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe44b-123">Riferimento al livello</span><span class="sxs-lookup"><span data-stu-id="fe44b-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





