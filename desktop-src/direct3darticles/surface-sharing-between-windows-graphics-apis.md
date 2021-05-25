---
title: Condivisione della superficie tra LE API grafiche di Windows
description: Questo argomento offre una panoramica tecnica dell'interoperabilità tramite la condivisione di superfici tra LE API grafiche di Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343616"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="eb5c6-103">Condivisione della superficie tra LE API grafiche di Windows</span><span class="sxs-lookup"><span data-stu-id="eb5c6-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="eb5c6-104">Questo argomento offre una panoramica tecnica dell'interoperabilità tramite la condivisione di superfici tra LE API grafiche di Windows, tra cui Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="eb5c6-105">Se si ha già una conoscenza di queste API, questo documento consente di usare più API per il rendering sulla stessa superficie in un'applicazione progettata per i sistemi operativi Windows 7 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="eb5c6-106">Questo argomento fornisce anche linee guida per le procedure consigliate e puntatori a risorse aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="eb5c6-107">Per l'interoperabilità Direct2D e DirectWrite nel runtime DirectX 11.1, è possibile usare i [dispositivi Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts) e i contesti di dispositivo per eseguire il rendering direttamente nei dispositivi Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="eb5c6-108">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eb5c6-109">Introduzione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="eb5c6-110">Panoramica dell'interoperabilità delle API</span><span class="sxs-lookup"><span data-stu-id="eb5c6-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="eb5c6-111">Scenari di interoperabilità</span><span class="sxs-lookup"><span data-stu-id="eb5c6-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="eb5c6-112">Condivisione di dispositivi Direct3D 10.1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="eb5c6-113">Superfici condivise sincronizzate DXGI 1.1</span><span class="sxs-lookup"><span data-stu-id="eb5c6-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="eb5c6-114">Interoperabilità tra LE API basate su Direct3D 9Ex e DXGI</span><span class="sxs-lookup"><span data-stu-id="eb5c6-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="eb5c6-115">Conclusione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="eb5c6-116">Introduzione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-116">Introduction</span></span>

<span data-ttu-id="eb5c6-117">In questo documento l'interoperabilità dell'API grafica di Windows si riferisce alla condivisione della stessa superficie di rendering da parte di API diverse.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="eb5c6-118">Questo tipo di interoperabilità consente alle applicazioni di creare visualizzazioni accattivanti sfruttando più API grafiche di Windows e di semplificare la migrazione alle nuove tecnologie mantenendo la compatibilità con le API esistenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="eb5c6-119">In Windows 7 (e Windows Vista SP2 con Windows 7 Interop Pack, Vista 7IP), le API di rendering della grafica sono Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c e api Direct3D precedenti, nonché GDI e GDI+.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="eb5c6-120">Windows Imaging Component (WIC) e DirectWrite sono tecnologie correlate per l'elaborazione delle immagini e Direct2D esegue il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="eb5c6-121">L'API DirectX Video Acceleration (DXVA), basata su Direct3D 9c e Direct3D 9Ex, viene usata per l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="eb5c6-122">Con l'evolversi delle API grafiche di Windows verso l'essere basate su Direct3D, Microsoft sta investendo più impegno per garantire l'interoperabilità tra le API.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="eb5c6-123">Le API Direct3D appena sviluppate e le API di livello superiore basate su API Direct3D forniscono anche il supporto quando necessario per il bridging della compatibilità con le API meno recenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="eb5c6-124">Per illustrare, le applicazioni Direct2D possono usare Direct3D 10.1 condividendo un dispositivo Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="eb5c6-125">Inoltre, le API Direct3D 11, Direct2D e Direct3D 10.1 possono sfruttare tutti i vantaggi di DirectX Graphic Infrastructure (DXGI) 1.1, che abilita le superfici condivise sincronizzate che supportano completamente l'interoperabilità tra queste API.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="eb5c6-126">Le API basate su DXGI 1.1 interagisce con GDI e con GDI+ per associazione, ottenendo il contesto di dispositivo GDI da una superficie DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="eb5c6-127">Per altre informazioni, vedere la documentazione sull'interoperabilità DXGI e GDI disponibile in MSDN.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="eb5c6-128">La condivisione della superficie non sincronizzata è supportata dal runtime Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="eb5c6-129">Le applicazioni video basate su DXVA possono usare l'helper di interoperabilità Direct3D 9Ex e DXGI per l'interoperabilità DXVA basata su Direct3D 9Ex con Direct3D 11 per compute shader oppure possono interagire con Direct2D per il rendering del testo o i controlli 2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="eb5c6-130">WIC e DirectWrite interagisce anche con GDI, Direct2D e, per associazione, altre API Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="eb5c6-131">Direct3D 10.0, Direct3D 9c e i runtime Direct3D precedenti non supportano le superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="eb5c6-132">Le copie della memoria di sistema continueranno a essere usate per l'interoperabilità con le API basate su GDI o DXGI.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="eb5c6-133">Si noti che gli scenari di interoperabilità all'interno di questo documento fanno riferimento a più API grafiche per il rendering in una superficie di rendering condivisa, anziché nella stessa finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="eb5c6-134">La sincronizzazione per API separate che hanno come destinazione superfici diverse che vengono quindi composte nella stessa finestra non rientra nell'ambito di questo documento.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="eb5c6-135">Panoramica dell'interoperabilità delle API</span><span class="sxs-lookup"><span data-stu-id="eb5c6-135">API Interoperability Overview</span></span>

<span data-ttu-id="eb5c6-136">L'interoperabilità della condivisione della superficie delle API grafiche di Windows può essere descritta in termini di scenari da API ad API e dalla funzionalità di interoperabilità corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="eb5c6-137">A partire da Windows 7 e a partire da Windows Vista SP2 con 7IP, le nuove API e i runtime associati includono Direct2D e le tecnologie correlate: Direct3D 11 e DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="eb5c6-138">Le prestazioni di GDI sono state migliorate anche in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="eb5c6-139">Direct3D 10.1 è stato introdotto in Windows Vista SP1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="eb5c6-140">Il diagramma seguente illustra il supporto dell'interoperabilità tra le API.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-140">The following diagram shows the interoperability support between APIs.</span></span>

![Diagramma del supporto dell'interoperabilità tra api grafiche di Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="eb5c6-142">In questo diagramma le frecce mostrano scenari di interoperabilità in cui la stessa superficie può essere accessibile dalle API connesse.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="eb5c6-143">Le frecce blu indicano i meccanismi di interoperabilità introdotti in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="eb5c6-144">Le frecce verdi indicano il supporto per l'interoperabilità per le nuove API o miglioramenti che consentono alle API meno recenti di interagire con le API più recenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="eb5c6-145">Ad esempio, le frecce verdi rappresentano la condivisione dei dispositivi, il supporto della superficie condivisa sincronizzata, l'helper di sincronizzazione Direct3D 9Ex/DXGI e l'ottenimento di un contesto di dispositivo GDI da una superficie compatibile.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="eb5c6-146">Scenari di interoperabilità</span><span class="sxs-lookup"><span data-stu-id="eb5c6-146">Interoperability Scenarios</span></span>

<span data-ttu-id="eb5c6-147">A partire da Windows 7 e Windows Vista 7IP, le offerte mainstream delle API grafiche di Windows supportano il rendering di più API nella stessa superficie DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="eb5c6-148">**Direct3D 11, Direct3D 10.1, Direct2D : interoperabilità tra loro**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="eb5c6-149">Le API Direct3D 11, Direct3D 10.1 e Direct2D (e le API correlate come DirectWrite e WIC) possono interagire tra loro usando la condivisione di dispositivi Direct3D 10.1 o superfici condivise sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="eb5c6-150">Condivisione di dispositivi Direct3D 10.1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="eb5c6-151">La condivisione dei dispositivi tra Direct2D e Direct3D 10.1 consente a un'applicazione di usare entrambe le API per eseguire il rendering in modo semplice ed efficiente sulla stessa superficie DXGI 1.1, usando lo stesso oggetto dispositivo Direct3D sottostante.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="eb5c6-152">Direct2D offre la possibilità di chiamare le API Direct2D usando un dispositivo Direct3D 10.1 esistente, sfruttando il fatto che Direct2D è basato sui runtime Direct3D 10.1 e DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="eb5c6-153">I frammenti di codice seguenti illustrano come Direct2D ottiene la destinazione di rendering del dispositivo Direct3D 10.1 da una superficie DXGI 1.1 associata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="eb5c6-154">La destinazione di rendering del dispositivo Direct3D 10.1 può eseguire chiamate di disegno Direct2D tra le API BeginDraw ed EndDraw.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="eb5c6-155">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-155">**Remarks**</span></span>

-   <span data-ttu-id="eb5c6-156">Il dispositivo Direct3D 10.1 associato deve supportare il formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="eb5c6-157">Il dispositivo è stato creato chiamando D3D10CreateDevice1 con il parametro D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="eb5c6-158">Il formato BGRA è supportato a partire dal livello di funzionalità 9.1 di Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="eb5c6-159">L'applicazione non deve creare più id2D1RenderTargets associati allo stesso dispositivo Direct3D10.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="eb5c6-160">Per ottenere prestazioni ottimali, tenere sempre presente almeno una risorsa, ad esempio trame o superfici associate al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="eb5c6-161">La condivisione dei dispositivi è adatta per l'utilizzo in-process a thread singolo di un dispositivo di rendering condiviso dalle API di rendering Direct3D 10.1 e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="eb5c6-162">Le superfici condivise sincronizzate consentono l'uso multi-thread, in-process e out-of-process di più dispositivi di rendering usati dalle API Direct3D 10.1, Direct2D e Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="eb5c6-163">Un altro metodo di interoperabilità di Direct3D 10.1 e Direct2D è l'uso di ID3D1RenderTarget::CreateSharedBitmap, che crea un oggetto ID2D1Bitmap da IDXGISurface.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="eb5c6-164">È possibile scrivere una scena Direct3D10.1 nella bitmap ed eseguirne il rendering con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="eb5c6-165">Per altre informazioni, vedere [Metodo ID2D1RenderTarget::CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="eb5c6-166">Rasterizzazione del software Direct2D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="eb5c6-167">La condivisione dei dispositivi con Direct3D 10.1 non è supportata quando si usa il renderer software Direct2D, ad esempio specificando D2D1 \_ RENDER TARGET USAGE FORCE SOFTWARE RENDERING in D2D1 RENDER TARGET USAGE durante la creazione di una destinazione di \_ \_ rendering \_ \_ \_ \_ \_ \_ Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="eb5c6-168">Direct2D può usare l'rasterizzazione software WARP10 per condividere il dispositivo con Direct3D 10 o Direct3D 11, ma le prestazioni diminuiscono significativamente.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="eb5c6-169">Superfici condivise sincronizzate DXGI 1.1</span><span class="sxs-lookup"><span data-stu-id="eb5c6-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="eb5c6-170">Le API Direct3D 11, Direct3D 10.1 e Direct2D usano tutte DXGI 1.1, che fornisce la funzionalità per sincronizzare la lettura e la scrittura nella stessa superficie di memoria video (DXGISurface1) da due o più dispositivi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="eb5c6-171">I dispositivi di rendering che usano superfici condivise sincronizzate possono essere dispositivi Direct3D 10.1 o Direct3D 11, ognuno in esecuzione nello stesso processo o tra processi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="eb5c6-172">Le applicazioni possono usare superfici condivise sincronizzate per interagire tra qualsiasi dispositivo basato su DXGI 1.1, ad esempio Direct3D 11 e Direct3D 10.1 o tra Direct3D 11 e Direct2D, ottenendo il dispositivo Direct3D 10.1 dall'oggetto di destinazione di rendering Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="eb5c6-173">Nelle API Direct3D 10.1 e versioni successive, per usare DXGI 1.1, assicurarsi che il dispositivo Direct3D sia creato usando un oggetto adattatore DXGI 1.1, enumerato dall'oggetto factory DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="eb5c6-174">Chiamare CreateDXGIFactory1 per creare l'oggetto IDXGIFactory1 ed EnumAdapters1 per enumerare l'oggetto IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="eb5c6-175">L'oggetto IDXGIAdapter1 deve essere passato come parte della chiamata D3D10CreateDevice o D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="eb5c6-176">Per altre informazioni sulle API DXGI 1.1, vedere la Guida alla [programmazione per DXGI.](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="eb5c6-177">API</span><span class="sxs-lookup"><span data-stu-id="eb5c6-177">APIs</span></span>

<span data-ttu-id="eb5c6-178">**RISORSA D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="eb5c6-179">Quando si crea la risorsa condivisa sincronizzata, impostare D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX in D3D10 \_ RESOURCE \_ MISC \_ FLAG.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="eb5c6-180">**RISORSA D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="eb5c6-181">Consente la sincronizzazione della risorsa creata usando le API IDXGIKeyedMutex::AcquireSync e ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="eb5c6-182">Le API Direct3D 10.1 di creazione di risorse seguenti che accettano tutti un parametro D3D10 RESOURCE MISC FLAG sono state estese per \_ \_ \_ supportare il nuovo flag.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="eb5c6-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="eb5c6-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="eb5c6-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="eb5c6-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="eb5c6-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="eb5c6-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="eb5c6-187">Se una delle funzioni elencate viene chiamata con il flag D3D10 RESOURCE MISC SHARED KEYEDMUTEX impostato, è possibile eseguire query sull'interfaccia restituita per un'interfaccia \_ \_ \_ IDXGIKeyedMutex, che implementa le API AcquireSync e ReleaseSync per sincronizzare l'accesso \_ alla superficie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="eb5c6-188">Il dispositivo che crea la superficie e qualsiasi altro dispositivo che apre la superficie (usando OpenSharedResource) è necessario per chiamare IDXGIKeyedMutex::AcquireSync prima di qualsiasi comando di rendering sulla superficie e IDXGIKeyedMutex::ReleaseSync al termine del rendering.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="eb5c6-189">I dispositivi WARP e REF non supportano le risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="eb5c6-190">Se si tenta di creare una risorsa con questo flag in un dispositivo WARP o REF, il metodo create restituirà un codice di errore E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="eb5c6-191">**INTERFACCIA IDXGIKEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="eb5c6-192">Una nuova interfaccia in DXGI 1.1, IDXGIKeyedMutex, rappresenta un mutex con chiave, che consente l'accesso esclusivo a una risorsa condivisa usata da più dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="eb5c6-193">Per la documentazione di riferimento su questa interfaccia e i relativi due metodi, AcquireSync e ReleaseSync, vedere [IDXGIKeyedMutex.](https://msdn.microsoft.com/library/ee421920(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="eb5c6-194">Esempio: Condivisione della superficie sincronizzata tra due dispositivi Direct3D 10.1</span><span class="sxs-lookup"><span data-stu-id="eb5c6-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="eb5c6-195">L'esempio seguente illustra la condivisione di una superficie tra due dispositivi Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="eb5c6-196">La superficie condivisa sincronizzata viene creata da un dispositivo Direct3D10.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="eb5c6-197">Lo stesso dispositivo Direct3D10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering dell'altro dispositivo chiamando ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="eb5c6-198">Quando non condivide la superficie condivisa sincronizzata con altri dispositivi Direct3D, l'autore può ottenere e rilasciare la superficie condivisa sincronizzata (per avviare e terminare il rendering) acquisendo e rilasciando usando lo stesso valore chiave.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="eb5c6-199">Il secondo dispositivo Direct3D10.1 può ottenere la superficie condivisa sincronizzata per il rendering chiamando AcquireSync, quindi rilasciando la superficie per il rendering del primo dispositivo chiamando ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="eb5c6-200">Si noti che il dispositivo 2 è in grado di acquisire la superficie condivisa sincronizzata usando lo stesso valore di chiave specificato nella chiamata a ReleaseSync dal dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="eb5c6-201">I dispositivi aggiuntivi che condividono la stessa superficie possono acquisire e rilasciare la superficie a turno usando chiavi aggiuntive, come illustrato nelle chiamate seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="eb5c6-202">Si noti che un'applicazione reale potrebbe sempre eseguire il rendering su una superficie intermedia che viene quindi copiata nella superficie condivisa per evitare che un dispositivo in attesa su un altro dispositivo che condivide la superficie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="eb5c6-203">Uso di superfici condivise sincronizzate con Direct2D e Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="eb5c6-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="eb5c6-204">Analogamente, per la condivisione tra le API Direct3D 11 e Direct3D 10.1, è possibile creare una superficie condivisa sincronizzata da un dispositivo API e condividerla con gli altri dispositivi API, in o fuori processo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="eb5c6-205">Le applicazioni che usano Direct2D possono condividere un dispositivo Direct3D 10.1 e usare una superficie condivisa sincronizzata per interagire con Direct3D 11 o altri dispositivi Direct3D 10.1, indipendentemente dal fatto che appartengano allo stesso processo o a processi diversi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="eb5c6-206">Tuttavia, per le applicazioni a thread singolo a processo singolo, la condivisione dei dispositivi è il metodo di interoperabilità più efficiente e ad alte prestazioni tra Direct2D e Direct3D 10 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="eb5c6-207">Rasterizzazione software</span><span class="sxs-lookup"><span data-stu-id="eb5c6-207">Software Rasterizer</span></span>

<span data-ttu-id="eb5c6-208">Le superfici condivise sincronizzate non sono supportate quando le applicazioni usano i rasterizzatori software Direct3D o Direct2D, inclusi il rasterizzatore di riferimento e WARP, anziché l'accelerazione hardware grafica.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="eb5c6-209">Interoperabilità tra LE API basate su Direct3D 9Ex e DXGI</span><span class="sxs-lookup"><span data-stu-id="eb5c6-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="eb5c6-210">Le API Direct3D 9Ex includevano la nozione di condivisione della superficie per consentire ad altre API di leggere dalla superficie condivisa.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="eb5c6-211">Per condividere la lettura e la scrittura in una superficie condivisa Direct3D 9Ex, è necessario aggiungere la sincronizzazione manuale all'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="eb5c6-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span><span class="sxs-lookup"><span data-stu-id="eb5c6-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="eb5c6-213">L'attività più fondamentale nell'interoperabilità Direct3D 9Ex e Direct3D 10 o 11 è il passaggio di una singola superficie dal primo dispositivo (dispositivo A) al secondo (dispositivo B) in modo che, quando il dispositivo B acquisisce un handle sulla superficie, il rendering del dispositivo A sia stato completato.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="eb5c6-214">Pertanto, il dispositivo B può usare questa superficie senza preoccuparsi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="eb5c6-215">Questo problema è molto simile al problema producer-consumer classico e questa discussione modella il problema in questo modo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="eb5c6-216">Il primo dispositivo che usa la superficie e quindi lo cesa è il producer (dispositivo A) e il dispositivo che inizialmente è in attesa è il consumer (dispositivo B).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="eb5c6-217">Qualsiasi applicazione reale è più sofisticata di questa e concatena più blocchi predefiniti producer-consumer per creare la funzionalità desiderata.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="eb5c6-218">I blocchi predefiniti producer-consumer vengono implementati nell'helper usando una coda di superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="eb5c6-219">Le superfici vengono accodati dal producer e accodati dal consumer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="eb5c6-220">L'helper introduce tre interfacce COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="eb5c6-221">High-Level panoramica dell'helper</span><span class="sxs-lookup"><span data-stu-id="eb5c6-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="eb5c6-222">L'oggetto ISurfaceQueue è il blocco predefinito per l'uso delle superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="eb5c6-223">Viene creato con un dispositivo Direct3D inizializzato e una descrizione per creare un numero fisso di superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="eb5c6-224">L'oggetto coda gestisce la creazione di risorse e l'apertura del codice.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="eb5c6-225">Il numero e il tipo di superfici sono fissi. Dopo aver creato le superfici, l'applicazione non può aggiungerle o rimuoverle.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="eb5c6-226">Ogni istanza dell'oggetto ISurfaceQueue fornisce una sorta di strada unidireale che può essere usata per inviare superfici dal dispositivo di produzione al dispositivo che li utilizza.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="eb5c6-227">È possibile usare più strade unidireali di questo tipo per abilitare scenari di condivisione della superficie tra dispositivi di applicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="eb5c6-228">**Durata creazione/oggetto**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="eb5c6-229">Esistono due modi per creare l'oggetto coda: tramite CreateSurfaceQueue o tramite il metodo Clone di ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="eb5c6-230">Poiché le interfacce sono oggetti COM, si applica la gestione della durata COM standard.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="eb5c6-231">**Modello producer/consumer**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="eb5c6-232">Accodamento (): il producer chiama questa funzione per indicare che è stata completata con la superficie, che ora può diventare disponibile per un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="eb5c6-233">Al ritorno da questa funzione, il dispositivo producer non ha più diritti per la superficie ed è non sicuro continuare a usarlo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="eb5c6-234">Dequeue (): il dispositivo che utilizza chiama questa funzione per ottenere una superficie condivisa.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="eb5c6-235">L'API garantisce che tutte le superfici accodati siano pronte per l'uso.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="eb5c6-236">**Metadata**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-236">**Metadata**</span></span>  
<span data-ttu-id="eb5c6-237">L'API supporta l'associazione di metadati alle superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="eb5c6-238">Enqueue() consente di specificare metadati aggiuntivi che verranno passati al dispositivo utilizzatore.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="eb5c6-239">I metadati devono essere inferiori al valore massimo noto al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="eb5c6-240">Dequeue() può facoltativamente passare un buffer e un puntatore alle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="eb5c6-241">La coda riempie il buffer con i metadati della chiamata enqueue corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="eb5c6-242">**Clonazione**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-242">**Cloning**</span></span>  
<span data-ttu-id="eb5c6-243">Ogni oggetto ISurfaceQueue risolve una sincronizzazione unidirezionale.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="eb5c6-244">Si presuppone che la maggior parte delle applicazioni che usano questa API userà un sistema chiuso.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="eb5c6-245">Il sistema chiuso più semplice con due dispositivi che inviano superfici avanti e indietro richiede due code.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="eb5c6-246">L'oggetto ISurfaceQueue ha un metodo Clone() per rendere possibile la creazione di più code che fanno tutte parte della stessa pipeline più grande.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="eb5c6-247">Clone crea un nuovo oggetto ISurfaceQueue da uno esistente e condivide tutte le risorse aperte tra di essi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="eb5c6-248">L'oggetto risultante ha esattamente le stesse superfici della coda di origine.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="eb5c6-249">Le code clonate possono avere dimensioni di metadati diverse l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="eb5c6-250">**Superfici**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-250">**Surfaces**</span></span>  
<span data-ttu-id="eb5c6-251">ISurfaceQueue è responsabile della creazione e della gestione delle superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="eb5c6-252">Non è valido accodare superfici arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="eb5c6-253">Inoltre, una superficie deve avere un solo "proprietario" attivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="eb5c6-254">Deve essere in una coda specifica o usata da un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="eb5c6-255">Non è valido che sia in più code o che i dispositivi continuino a usare la superficie dopo essere stati accodati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="eb5c6-256">Dettagli DELL'API</span><span class="sxs-lookup"><span data-stu-id="eb5c6-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="eb5c6-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="eb5c6-257">IsurfaceQueue</span></span>

<span data-ttu-id="eb5c6-258">La coda è responsabile della creazione e della gestione delle risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="eb5c6-259">Fornisce anche la funzionalità per concatenare più code usando Clone.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="eb5c6-260">La coda dispone di metodi che aprono il dispositivo di produzione e un dispositivo che lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="eb5c6-261">È possibile aprire solo uno di essi in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="eb5c6-262">La coda espone le API seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb5c6-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="eb5c6-263">API</span><span class="sxs-lookup"><span data-stu-id="eb5c6-263">API</span></span>                            | <span data-ttu-id="eb5c6-264">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb5c6-265">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="eb5c6-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="eb5c6-266">Crea un oggetto ISurfaceQueue (la coda "radice").</span><span class="sxs-lookup"><span data-stu-id="eb5c6-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="eb5c6-267">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="eb5c6-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="eb5c6-268">Restituisce un'interfaccia per il dispositivo che utilizza la coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="eb5c6-269">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="eb5c6-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="eb5c6-270">Restituisce un'interfaccia per il dispositivo di produzione da accodare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="eb5c6-271">ISurfaceQueue::Clone</span><span class="sxs-lookup"><span data-stu-id="eb5c6-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="eb5c6-272">Crea un oggetto ISurfaceQueue che condivide le superfici con l'oggetto coda radice.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="eb5c6-273">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-273">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="eb5c6-274">**Members**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-274">**Members**</span></span>  

<span data-ttu-id="eb5c6-275">**Width**, **Height**  Le dimensioni delle superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="eb5c6-276">Tutte le superfici condivise devono avere le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="eb5c6-277">**Formato** Formato delle superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="eb5c6-278">Tutte le superfici condivise devono avere lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="eb5c6-279">I formati validi dipendono dai dispositivi che verranno usati, perché coppie diverse di dispositivi possono condividere tipi di formato diversi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="eb5c6-280">**NumSurfaces**  Numero di superfici che fanno parte della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="eb5c6-281">Si tratta di un numero fisso.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-281">This is a fixed number.</span></span>  
 <span data-ttu-id="eb5c6-282">**MetaDataSize**  Dimensione massima del buffer dei metadati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="eb5c6-283">**Flag**  Flag per controllare il comportamento della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="eb5c6-284">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="eb5c6-285">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-285">**Parameters**</span></span>

 <span data-ttu-id="eb5c6-286">*pDesc* \[ in \]  Descrizione della coda della superficie condivisa da creare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="eb5c6-287">*pDevice* \[ in \]  Il dispositivo da usare per creare le superfici condivise.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="eb5c6-288">Si tratta di un parametro esplicito a causa di una funzionalità in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="eb5c6-289">Per le superfici condivise tra Direct3D 9 e Direct3D 10, le superfici devono essere create con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="eb5c6-290">*ppQueue* \[ out \]  In caso di restituzione, contiene un puntatore all'oggetto ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="eb5c6-291">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-291">**Return Values**</span></span>

<span data-ttu-id="eb5c6-292">Se *pDevice non* è in grado di condividere le risorse, questa funzione restituisce DXGI \_ ERROR INVALID \_ \_ CALL.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="eb5c6-293">Questa funzione crea le risorse.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-293">This function creates the resources.</span></span> <span data-ttu-id="eb5c6-294">Se non riesce, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-294">If it fails, it returns an error.</span></span> <span data-ttu-id="eb5c6-295">Se ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="eb5c6-296">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-296">**Remarks**</span></span>

<span data-ttu-id="eb5c6-297">La creazione dell'oggetto coda crea anche tutte le superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="eb5c6-298">Si presuppone che tutte le superfici siano destinazioni di rendering 2D e verranno create con i flag D3D10 BIND RENDER TARGET e \_ \_ \_ D3D10 BIND SHADER RESOURCE impostati \_ \_ (o i flag \_ equivalenti per i diversi runtime).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="eb5c6-299">Lo sviluppatore può specificare un flag che indica se la coda sarà accessibile da più thread.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="eb5c6-300">Se non è impostato alcun flag (**Flags** == 0), la coda verrà usata da più thread.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="eb5c6-301">Lo sviluppatore può specificare l'accesso a thread singolo, che disattiva il codice di sincronizzazione e offre un miglioramento delle prestazioni per questi casi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="eb5c6-302">Ogni coda clonata ha un proprio flag, pertanto è possibile che diverse code nel sistema abbia controlli di sincronizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="eb5c6-303">**Aprire un producer**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="eb5c6-304">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-304">**Parameters**</span></span>  

<span data-ttu-id="eb5c6-305">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="eb5c6-306">Dispositivo producer che accoda le superfici alla coda di superficie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="eb5c6-307">*ppProducer* \[ out \] Restituisce un oggetto all'interfaccia producer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="eb5c6-308">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-308">**Return Values**</span></span>

<span data-ttu-id="eb5c6-309">Se il dispositivo non è in grado di condividere le superfici, restituisce ERRORE DXGI \_ \_ CHIAMATA NON \_ VALIDA.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="eb5c6-310">**Aprire un consumer**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="eb5c6-311">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-311">**Parameters**</span></span>  
 <span data-ttu-id="eb5c6-312">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="eb5c6-313">Dispositivo consumer che consente di accodare le superfici dalla coda di superficie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="eb5c6-314">*ppConsumer* \[ out \]  Restituisce un oggetto all'interfaccia del consumer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="eb5c6-315">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-315">**Return Values**</span></span>

<span data-ttu-id="eb5c6-316">Se il dispositivo non è in grado di condividere le superfici, restituisce ERRORE DXGI \_ \_ CHIAMATA NON \_ VALIDA.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="eb5c6-317">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-317">**Remarks**</span></span>

<span data-ttu-id="eb5c6-318">Questa funzione apre tutte le superfici nella coda per il dispositivo di input e le memorizza nella cache.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="eb5c6-319">Le chiamate successive a Dequeue verranno semplicemente memorizzate nella cache e non sarà necessario riaprire le superfici ogni volta.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="eb5c6-320">Clonazione di un oggetto IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="eb5c6-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="eb5c6-321">**I** **membri MetaDataSize** **e Flags** hanno lo stesso comportamento di CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="eb5c6-322">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-322">**Parameters**</span></span>

<span data-ttu-id="eb5c6-323">*pDesc* \[ in \] uno struct che fornisce una descrizione dell'oggetto Clone da creare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="eb5c6-324">Questo parametro deve essere inizializzato.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="eb5c6-325">*ppQueue* \[ out \] Restituisce l'oggetto inizializzato.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="eb5c6-326">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-326">**Remarks**</span></span>

<span data-ttu-id="eb5c6-327">È possibile clonare da qualsiasi oggetto coda esistente, anche se non è la radice.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="eb5c6-328">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="eb5c6-328">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="eb5c6-329">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-329">**Parameters**</span></span>  
<span data-ttu-id="eb5c6-330">*id* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-330">*id* \[in\]</span></span>  
<span data-ttu-id="eb5c6-331">REFIID di una superficie 2D del dispositivo che consuma.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="eb5c6-332">Per un dispositivo IDirect3DDevice9, REFIID deve essere \_ \_ uuidof(IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="eb5c6-333">Per un dispositivo ID3D10, REFIID deve essere \_ \_ uuidof(ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="eb5c6-334">Per un dispositivo ID3D11, REFIID deve essere \_ \_ uuidof(ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="eb5c6-335">*ppSurface* \[ out \] Restituisce un puntatore alla superficie.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="eb5c6-336">*pBuffer* \[ in, out Un parametro facoltativo e se non NULL, in caso di restituzione, contiene i metadati passati \] nella chiamata di accodamento corrispondente. </span><span class="sxs-lookup"><span data-stu-id="eb5c6-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="eb5c6-337">*pBufferSize* \[ in, out \] Le dimensioni di *pBuffer*, in byte.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="eb5c6-338">Restituisce il numero di byte restituiti in *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="eb5c6-339">Se la chiamata di accodamento non ha fornito metadati, *pBuffer* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="eb5c6-340">*dwTimeout* \[ in \] Specifica un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="eb5c6-341">Per altre informazioni, vedere Note.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="eb5c6-342">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-342">**Return Values**</span></span>

<span data-ttu-id="eb5c6-343">Questa funzione può restituire WAIT TIMEOUT se viene specificato un valore di timeout e \_ la funzione non restituisce prima del valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="eb5c6-344">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-344">See Remarks.</span></span> <span data-ttu-id="eb5c6-345">Se non sono disponibili superfici, la funzione restituisce con *ppSurface* impostato su **NULL,** *pBufferSize* impostato su 0 e il valore restituito è 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).</span><span class="sxs-lookup"><span data-stu-id="eb5c6-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="eb5c6-346">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-346">**Remarks**</span></span>

<span data-ttu-id="eb5c6-347">Questa API può bloccarsi se la coda è vuota.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="eb5c6-348">Il *parametro dwTimeout* funziona in modo identico alle API di sincronizzazione di Windows, ad esempio WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="eb5c6-349">Per un comportamento non bloccante, usare un timeout di 0.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="eb5c6-350">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="eb5c6-350">ISurfaceProducer</span></span>

<span data-ttu-id="eb5c6-351">Questa interfaccia fornisce due metodi che consentono all'app di accodare superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="eb5c6-352">Dopo l'accodamento di una superficie, il puntatore di superficie non è più valido e non è sicuro da usare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="eb5c6-353">L'unica azione che l'applicazione deve eseguire con il puntatore è rilasciarla.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="eb5c6-354">Metodo</span><span class="sxs-lookup"><span data-stu-id="eb5c6-354">Method</span></span>                          | <span data-ttu-id="eb5c6-355">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5c6-356">ISurfaceProducer::Enqueue</span><span class="sxs-lookup"><span data-stu-id="eb5c6-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="eb5c6-357">Accoda una superficie all'oggetto coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="eb5c6-358">Al termine della chiamata, il producer viene eseguito con la superficie e la superficie è pronta per un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="eb5c6-359">ISurfaceProducer::Flush</span><span class="sxs-lookup"><span data-stu-id="eb5c6-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="eb5c6-360">Utilizzato se le applicazioni devono avere un comportamento non bloccante.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="eb5c6-361">Per ulteriori informazioni, vedere Note.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="eb5c6-362">**Enqueue**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="eb5c6-363">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-363">**Parameters**</span></span>  
<span data-ttu-id="eb5c6-364">*pSurface* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="eb5c6-365">La superficie del dispositivo di produzione che deve essere accodata.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="eb5c6-366">Questa superficie deve essere una superficie disaccodata dalla stessa rete di accodamento.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="eb5c6-367">*pBuffer* \[ in \] Parametro facoltativo, usato per passare i metadati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="eb5c6-368">Deve puntare ai dati che verranno passati alla chiamata di annullamento della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="eb5c6-369">*BufferSize* \[ in \] Dimensioni di *pBuffer*, in byte.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="eb5c6-370">*Flag* \[ in \] Parametro facoltativo che controlla il comportamento di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="eb5c6-371">L'unico flag è SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="eb5c6-372">Vedere la sezione Osservazioni per Flush.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-372">See the Remarks for Flush.</span></span> <span data-ttu-id="eb5c6-373">Se non viene passato alcun flag (*Flags* == 0), viene usato il comportamento di blocco predefinito.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="eb5c6-374">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-374">**Return Values**</span></span>

<span data-ttu-id="eb5c6-375">Questa funzione può restituire DXGI ERROR WAS STILL DRAWING se viene usato un \_ flag SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="eb5c6-376">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-376">**Remarks**</span></span>

-   <span data-ttu-id="eb5c6-377">Questa funzione inserisce la superficie nella coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="eb5c6-378">Se l'applicazione non specifica SURFACE QUEUE FLAG DO NOT WAIT, questa funzione è bloccata e esegue una sincronizzazione GPU-CPU per garantire che tutto il rendering sulla superficie \_ \_ \_ \_ \_ accodata sia completo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="eb5c6-379">Se questa funzione ha esito positivo, sarà disponibile una superficie per la deaccodazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="eb5c6-380">Se si vuole un comportamento non bloccante, usare il flag DO \_ NOT \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="eb5c6-381">Per informazioni dettagliate, vedere Flush().</span><span class="sxs-lookup"><span data-stu-id="eb5c6-381">See Flush() for details.</span></span>
-   <span data-ttu-id="eb5c6-382">In base alle regole di conteggio dei riferimenti COM, la superficie restituita da Dequeue sarà AddRef(), quindi l'applicazione non deve eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="eb5c6-383">Dopo aver chiamato Enqueue, l'applicazione deve rilasciare la superficie perché non la usa più.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="eb5c6-384">**Svuotamento**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="eb5c6-385">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-385">**Parameters**</span></span>  
<span data-ttu-id="eb5c6-386">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="eb5c6-387">L'unico flag è SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="eb5c6-388">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-388">See Remarks.</span></span> <span data-ttu-id="eb5c6-389">*nSurfaces* \[ out \] Restituisce il numero di superfici ancora in sospeso e non scaricate.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="eb5c6-390">**Valori restituiti**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-390">**Return Values**</span></span>

<span data-ttu-id="eb5c6-391">Questa funzione può restituire DXGI ERROR WAS STILL DRAWING se viene usato il \_ flag SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="eb5c6-392">Questa funzione restituisce S \_ OK se le superfici sono state scaricate correttamente.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="eb5c6-393">Questa funzione restituisce DXGI \_ ERROR WAS STILL DRAWING solo se non sono state \_ \_ \_ scaricate superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="eb5c6-394">Insieme, il valore restituito *e nSurfaces* indicano all'applicazione quali operazioni sono state eseguite e se è rimasto del lavoro da eseguire.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="eb5c6-395">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-395">**Remarks**</span></span>

<span data-ttu-id="eb5c6-396">Lo scaricamento è significativo solo se la chiamata precedente all'accodamento ha usato il flag DO NOT WAIT; in caso contrario, sarà \_ \_ un'operazione no-op.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="eb5c6-397">Se la chiamata all'accodamento usa il flag DO NOT WAIT, l'accodamento viene restituito immediatamente e la sincronizzazione \_ \_ GPU-CPU non è garantita.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="eb5c6-398">La superficie è ancora considerata accodata, il dispositivo di produzione non può continuare a usarlo, ma non è disponibile per la rimozione della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="eb5c6-399">Per provare a eseguire il commit della superficie per la deaccodazione, è necessario chiamare Flush.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="eb5c6-400">Lo scaricamento tenta di eseguire il commit di tutte le superfici attualmente accodate.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="eb5c6-401">Se non viene passato alcun flag a Flush, blocca e cancella l'intera coda, preparando tutte le superfici in essa presenti per la rimozione dalla coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="eb5c6-402">Se viene usato il flag DO NOT WAIT, la coda controlla le superfici per verificare se una di esse è pronta. Questo passaggio non \_ \_ è bloccante.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="eb5c6-403">Le superfici che hanno completato la sincronizzazione GPU-CPU saranno pronte per il dispositivo consumer.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="eb5c6-404">Le superfici ancora in sospeso non saranno interessate.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="eb5c6-405">La funzione restituisce il numero di superfici che devono ancora essere scaricate.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="eb5c6-406">Lo scaricamento non interrompe la semantica della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="eb5c6-407">L'API garantisce che venga eseguito il commit delle superfici accodati prima delle superfici accodati in un secondo momento, indipendentemente dal momento in cui viene eseguita la sincronizzazione GPU-CPU.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="eb5c6-408">Helper di interoperabilità Direct3D 9Ex e DXGI: come usare</span><span class="sxs-lookup"><span data-stu-id="eb5c6-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="eb5c6-409">Si prevede che la maggior parte dei casi di utilizzo coinvolgono due dispositivi che condividono una serie di superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="eb5c6-410">Poiché questo è anche lo scenario più semplice, questo documento descrive in dettaglio come usare le API per raggiungere questo obiettivo, illustra una variante non bloccante e termina con una breve sezione sull'inizializzazione per tre dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="eb5c6-411">Due dispositivi</span><span class="sxs-lookup"><span data-stu-id="eb5c6-411">Two Devices</span></span>

<span data-ttu-id="eb5c6-412">L'applicazione di esempio che usa questo helper può usare Direct3D 9Ex e Direct3D 11 insieme.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="eb5c6-413">L'applicazione può elaborare il contenuto con entrambi i dispositivi e presentare il contenuto usando Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="eb5c6-414">L'elaborazione può significare il rendering del contenuto, la decodifica di video, l'esecuzione di compute shader e così via.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="eb5c6-415">Per ogni frame, l'applicazione verrà prima elaborata con Direct3D 11, quindi verrà elaborata con Direct3D 9 e infine presente con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="eb5c6-416">Inoltre, l'elaborazione con Direct3D 11 produrrà alcuni metadati che direct3D 9 presente dovrà utilizzare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="eb5c6-417">Questa sezione illustra l'utilizzo dell'helper in tre parti che corrispondono a questa sequenza: inizializzazione, ciclo principale e pulizia.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="eb5c6-418">**Inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-418">**Initialization**</span></span>  
<span data-ttu-id="eb5c6-419">L'inizializzazione prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb5c6-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="eb5c6-420">Inizializzare entrambi i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="eb5c6-421">Creare la coda radice: m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="eb5c6-422">Clonare dalla coda radice: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="eb5c6-423">Chiamare OpenProducer/OpenConsumer in entrambe le code.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="eb5c6-424">I nomi delle code usano i numeri 9 e 11 per indicare quale API è il producer e quale consumer: **m \_**_producer_*_to_*_consumer_*_Queue_*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="eb5c6-425">Di conseguenza, m 11to9Queue indica una coda per cui il dispositivo Direct3D 11 produce superfici utilizzate dal dispositivo \_ Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="eb5c6-426">Analogamente, m 9to11Queue indica una coda per cui Direct3D 9 produce superfici utilizzate da \_ Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="eb5c6-427">La coda radice è inizialmente piena e tutte le code clonate sono inizialmente vuote.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="eb5c6-428">Questo non deve essere un problema per l'applicazione, ad eccezione del primo ciclo delle code e delle code e della disponibilità dei metadati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="eb5c6-429">Se una coda richiede metadati ma non ne è stato impostato alcuno (perché inizialmente non è presente alcun elemento o l'accodamento non ha impostato alcun valore), la coda visualizza che non è stato ricevuto alcun metadati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="eb5c6-430">**Inizializzare entrambi i dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="eb5c6-431">**Creare la coda radice.**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="eb5c6-432">Questo passaggio crea anche le superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-432">This step also creates the surfaces.</span></span> <span data-ttu-id="eb5c6-433">Le restrizioni relative alle dimensioni e al formato sono identiche alla creazione di qualsiasi risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="eb5c6-434">Le dimensioni del buffer dei metadati sono fisse in fase di creazione e in questo caso si passerà semplicemente un UINT.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="eb5c6-435">La coda deve essere creata con un numero fisso di superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="eb5c6-436">Le prestazioni variano a seconda dello scenario.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="eb5c6-437">La presenza di più superfici aumenta le probabilità che i dispositivi siano occupati.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="eb5c6-438">Ad esempio, se è presente una sola superficie, non sarà presente alcuna parallelizzazione tra i due dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="eb5c6-439">D'altra parte, l'aumento del numero di superfici aumenta il footprint di memoria, con un possibile peggioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="eb5c6-440">In questo esempio vengono utilizzate due superfici.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-440">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="eb5c6-441">**Clonare la coda radice.**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="eb5c6-442">Ogni coda clonata deve usare le stesse superfici, ma può avere dimensioni del buffer di metadati diverse e flag diversi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="eb5c6-443">In questo caso, non sono presenti metadati da Direct3D 9 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="eb5c6-444">**Aprire i dispositivi producer e consumer.**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="eb5c6-445">L'applicazione deve eseguire questo passaggio prima di chiamare Enqueue e Dequeue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="eb5c6-446">L'apertura di un producer e di un consumer restituisce interfacce che contengono le API di accodamento/annullamento della coda.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="eb5c6-447">**Ciclo Main**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-447">**Main Loop**</span></span>  
<span data-ttu-id="eb5c6-448">L'utilizzo della coda è modellato in base al problema producer/consumer classico.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="eb5c6-449">Si pensi a questo dal punto di vista dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="eb5c6-450">Ogni dispositivo deve eseguire questi passaggi: rimozione dalla coda per ottenere una superficie dalla coda di utilizzo, elaborazione in superficie e quindi accodamento nella coda di produzione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="eb5c6-451">Per il dispositivo Direct3D 11, l'utilizzo di Direct3D 9 è quasi identico.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="eb5c6-452">**Pulizia**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-452">**Cleaning Up**</span></span>  
<span data-ttu-id="eb5c6-453">Questo passaggio è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-453">This step is very straightforward.</span></span> <span data-ttu-id="eb5c6-454">Oltre ai normali passaggi per la pulizia delle API Direct3D, l'applicazione deve rilasciare le interfacce COM restituite.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="eb5c6-455">Uso non bloccante</span><span class="sxs-lookup"><span data-stu-id="eb5c6-455">Non-Blocking Use</span></span>

<span data-ttu-id="eb5c6-456">L'esempio precedente ha senso per un caso di utilizzo multithreading in cui ogni dispositivo ha un proprio thread.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="eb5c6-457">L'esempio usa le versioni di blocco delle API: INFINITE per il timeout e nessun flag da accodare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="eb5c6-458">Se si vuole usare l'helper in modo non bloccante, è necessario apportare solo alcune modifiche.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="eb5c6-459">Questa sezione illustra l'uso non bloccante con entrambi i dispositivi in un unico thread.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="eb5c6-460">**Inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-460">**Initialization**</span></span>  
<span data-ttu-id="eb5c6-461">L'inizializzazione è identica ad eccezione dei flag .</span><span class="sxs-lookup"><span data-stu-id="eb5c6-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="eb5c6-462">Poiché l'applicazione è a thread singolo, usare tale flag per la creazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="eb5c6-463">In questo modo viene disattivata parte del codice di sincronizzazione, che potrebbe migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="eb5c6-464">L'apertura dei dispositivi producer e consumer è la stessa dell'esempio di blocco.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="eb5c6-465">**Uso della coda**</span><span class="sxs-lookup"><span data-stu-id="eb5c6-465">**Using the Queue**</span></span>  
<span data-ttu-id="eb5c6-466">Esistono molti modi per usare la coda in modo non bloccante con diverse caratteristiche delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="eb5c6-467">L'esempio seguente è semplice, ma presenta prestazioni scarse a causa di un numero eccessivo di operazioni di rotazione e polling.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="eb5c6-468">Nonostante questi problemi, l'esempio mostra come usare l'helper.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="eb5c6-469">L'approccio consiste nel restare costantemente in un ciclo e dequeue, elaborare, accodare e scaricare.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="eb5c6-470">Se uno dei passaggi ha esito negativo perché la risorsa non è disponibile, l'applicazione prova semplicemente a eseguire di nuovo il ciclo successivo.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="eb5c6-471">Una soluzione più complessa potrebbe controllare il valore restituito dalla coda e dallo scaricamento per determinare se è necessario lo scaricamento.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="eb5c6-472">Tre dispositivi</span><span class="sxs-lookup"><span data-stu-id="eb5c6-472">Three Devices</span></span>

<span data-ttu-id="eb5c6-473">Estendere gli esempi precedenti per coprire più dispositivi è semplice.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="eb5c6-474">Il codice seguente esegue l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-474">The following code performs the initialization.</span></span> <span data-ttu-id="eb5c6-475">Dopo aver creato gli oggetti Producer/Consumer, il codice per usarli è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="eb5c6-476">In questo esempio sono disponibili tre dispositivi e quindi tre code.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="eb5c6-477">Le superfici fluire da Direct3D 9 a Direct3D 10 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="eb5c6-478">Come accennato in precedenza, la clonazione funziona allo stesso modo, indipendentemente dalla coda clonata.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="eb5c6-479">Ad esempio, la seconda chiamata Clone potrebbe essere stata rimossa dall'oggetto m \_ 9to10Queue.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="eb5c6-480">Conclusione</span><span class="sxs-lookup"><span data-stu-id="eb5c6-480">Conclusion</span></span>

<span data-ttu-id="eb5c6-481">È possibile creare soluzioni che usano l'interoperabilità per usare la potenza di più API DirectX.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="eb5c6-482">L'interoperabilità dell'API grafica di Windows offre ora un common surface management runtime DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="eb5c6-483">Questo runtime abilita il supporto della condivisione della superficie sincronizzata all'interno delle API appena sviluppate, ad esempio Direct3D 11, Direct3D 10.1 e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="eb5c6-484">I miglioramenti dell'interoperabilità tra le nuove API e le API esistenti migliorano la migrazione delle applicazioni e la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="eb5c6-485">Le API consumer Direct3D 9Ex e DXGI 1.1 possono interagire, come illustrato con il meccanismo di sincronizzazione fornito tramite codice helper di esempio in MSDN Code Gallery.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 