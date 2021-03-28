---
title: Funzionalità di Direct3D 11,4
description: In Direct3D 11,4 sono state aggiunte le funzionalità seguenti.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963241"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="05fa5-103">Funzionalità di Direct3D 11,4</span><span class="sxs-lookup"><span data-stu-id="05fa5-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="05fa5-104">In Direct3D 11,4 sono state aggiunte le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="05fa5-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="05fa5-105">Vedere anche [dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="05fa5-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="05fa5-106">Rimozione del dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="05fa5-106">Direct3D device removal</span></span>

<span data-ttu-id="05fa5-107">I metodi [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) sono supportati da una nuova interfaccia, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), per supportare la ricezione di una notifica di evento asincrono quando un dispositivo Direct3D è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="05fa5-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="05fa5-108">Protezione multithreading</span><span class="sxs-lookup"><span data-stu-id="05fa5-108">Multithreaded protection</span></span>

<span data-ttu-id="05fa5-109">Per assicurarsi che i comandi grafici in particolare vengano eseguiti in un ordine specifico, l'interfaccia [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) dispone di metodi per attivare e disattivare la protezione multithread e i metodi per immettere e lasciare codice critico che richiede la protezione.</span><span class="sxs-lookup"><span data-stu-id="05fa5-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="05fa5-110">Barriere per la sincronizzazione di più dispositivi e l'interoperabilità con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="05fa5-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="05fa5-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) forniscono le stesse funzionalità di recinzione di Direct3D 12 per Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="05fa5-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="05fa5-112">Le recinzioni vengono usate per sincronizzare più dispositivi Direct3D11 e per l'interoperabilità tra Direct3D 11 e Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="05fa5-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="05fa5-113">Gli schermi sono supportati in Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="05fa5-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="05fa5-114">Supporto per la trama NV12 estesa</span><span class="sxs-lookup"><span data-stu-id="05fa5-114">Extended NV12 texture support</span></span>

<span data-ttu-id="05fa5-115">Le trame NV12 con funzionalità di acquisizione e codifica video supportano ora la condivisione.</span><span class="sxs-lookup"><span data-stu-id="05fa5-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="05fa5-116">I flag di trama D3D11 precedenti per la codifica e l'acquisizione video sono deprecati per NV12, in quanto verranno impostati continuamente per i nuovi driver.</span><span class="sxs-lookup"><span data-stu-id="05fa5-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="05fa5-117">Tali trame possono essere condivise non solo con D3D11, ma anche con D3D12.</span><span class="sxs-lookup"><span data-stu-id="05fa5-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="05fa5-118">In D3D12 non sono presenti nuovi flag che rappresentano queste funzionalità di trama.</span><span class="sxs-lookup"><span data-stu-id="05fa5-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="05fa5-119">Vedere l'impostazione booleana nei [**\_ dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="05fa5-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="05fa5-120">Caching dello shader</span><span class="sxs-lookup"><span data-stu-id="05fa5-120">Shader Caching</span></span>

<span data-ttu-id="05fa5-121">I driver possono supportare la memorizzazione nella cache shader gestita dal sistema operativo per le applicazioni Direct3D11 in Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="05fa5-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05fa5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05fa5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05fa5-123">Novità di Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="05fa5-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 