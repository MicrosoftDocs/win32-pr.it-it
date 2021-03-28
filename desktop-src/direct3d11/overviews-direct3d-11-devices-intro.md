---
title: Introduzione a un dispositivo in Direct3D 11
description: Il modello a oggetti Direct3D 11 separa la creazione e la funzionalità di rendering delle risorse in un dispositivo e uno o più contesti; Questa separazione è progettata per semplificare il multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976050"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="2bfa2-103">Introduzione a un dispositivo in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2bfa2-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="2bfa2-104">Il modello a oggetti Direct3D 11 separa la creazione e la funzionalità di rendering delle risorse in un dispositivo e uno o più contesti; Questa separazione è progettata per semplificare il multithreading.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="2bfa2-105">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="2bfa2-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="2bfa2-106">Contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="2bfa2-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="2bfa2-107">Contesto immediato</span><span class="sxs-lookup"><span data-stu-id="2bfa2-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="2bfa2-108">Contesto posticipato</span><span class="sxs-lookup"><span data-stu-id="2bfa2-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="2bfa2-109">Considerazioni sul threading</span><span class="sxs-lookup"><span data-stu-id="2bfa2-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="2bfa2-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bfa2-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="2bfa2-111">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="2bfa2-111">Device</span></span>

<span data-ttu-id="2bfa2-112">Un dispositivo viene utilizzato per creare risorse ed enumerare le funzionalità di una scheda di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="2bfa2-113">In Direct3D 11 un dispositivo è rappresentato da un'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="2bfa2-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="2bfa2-114">Ogni applicazione deve avere almeno un dispositivo. la maggior parte delle applicazioni crea solo un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="2bfa2-115">Creare un dispositivo per uno dei driver hardware installati nel computer chiamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e specificare il tipo di driver con il flag del [**\_ \_ tipo di driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="2bfa2-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="2bfa2-116">Ogni dispositivo può usare uno o più contesti di dispositivo, a seconda delle funzionalità desiderate.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="2bfa2-117">Contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="2bfa2-117">Device Context</span></span>

<span data-ttu-id="2bfa2-118">Un contesto di dispositivo contiene la circostanza o l'impostazione in cui viene usato un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="2bfa2-119">In particolare, viene usato un contesto di dispositivo per impostare lo stato della pipeline e generare i comandi di rendering usando le risorse di proprietà di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="2bfa2-120">Direct3D 11 implementa due tipi di contesti di dispositivo, uno per il rendering immediato e l'altro per il rendering posticipato; entrambi i contesti sono rappresentati con un'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="2bfa2-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="2bfa2-121">Contesto immediato</span><span class="sxs-lookup"><span data-stu-id="2bfa2-121">Immediate Context</span></span>

<span data-ttu-id="2bfa2-122">Un contesto immediato viene sottoposta a rendering direttamente al driver.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="2bfa2-123">Ogni dispositivo ha un solo contesto immediato che può recuperare i dati dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="2bfa2-124">Un contesto immediato può essere usato per eseguire immediatamente il rendering o la riproduzione di un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="2bfa2-125">Esistono due modi per ottenere un contesto immediato:</span><span class="sxs-lookup"><span data-stu-id="2bfa2-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="2bfa2-126">Chiamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="2bfa2-127">Chiamando [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="2bfa2-128">Contesto posticipato</span><span class="sxs-lookup"><span data-stu-id="2bfa2-128">Deferred Context</span></span>

<span data-ttu-id="2bfa2-129">Un contesto posticipato registra i comandi GPU in un [elenco di comandi](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="2bfa2-130">Un contesto posticipato viene usato principalmente per il multithreading e non è necessario per un'applicazione a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="2bfa2-131">Un contesto posticipato viene in genere usato da un thread di lavoro anziché dal thread di rendering principale.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="2bfa2-132">Quando si crea un contesto posticipato, non eredita alcuno stato dal contesto immediato.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="2bfa2-133">Per ottenere un contesto posticipato, chiamare [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="2bfa2-134">Qualsiasi contesto, immediato o posticipato, può essere usato in qualsiasi thread, purché il contesto venga usato solo in un thread alla volta.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="2bfa2-135">Considerazioni sul threading</span><span class="sxs-lookup"><span data-stu-id="2bfa2-135">Threading Considerations</span></span>

<span data-ttu-id="2bfa2-136">Questa tabella evidenzia le differenze nel modello di threading in Direct3D 11 da versioni precedenti di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bfa2-137">Differenze tra Direct3D 11 e versioni precedenti di Direct3D:</span><span class="sxs-lookup"><span data-stu-id="2bfa2-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="2bfa2-138">Tutti i metodi dell'interfaccia <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> sono a thread libero, quindi è possibile che più thread chiamino contemporaneamente le funzioni.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="2bfa2-139">Tutte le interfacce derivate da <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>e così via) sono a thread libero.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="2bfa2-140">Direct3D 11 suddivide la creazione e il rendering delle risorse in due interfacce.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="2bfa2-141">Map, annullare, Begin, end e GetData sono implementati in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a> perché <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> definisce fortemente l'ordine delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="2bfa2-142">Le interfacce <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> e <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> implementano anche metodi per operazioni a thread libero.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="2bfa2-143">I metodi <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>sul ID3D11DeviceContext</strong></a> (ad eccezione di quelli esistenti in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) non sono a thread libero, ovvero richiedono un thread singolo.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="2bfa2-144">Solo un thread può chiamare in modo sicuro uno dei suoi metodi (disegni, copia, mappa e così via) alla volta.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="2bfa2-145">In generale, il threading libero riduce al minimo il numero di primitive di sincronizzazione utilizzate e la relativa durata.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="2bfa2-146">Tuttavia, un'applicazione che usa la sincronizzazione mantenuta per molto tempo può influito direttamente sulla quantità di concorrenza che un'applicazione può aspettarsi di raggiungere.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="2bfa2-147">I metodi dell'interfaccia ID3D10Device non sono progettati per essere a thread libero.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="2bfa2-148">ID3D10Device implementa tutte le funzionalità di creazione e rendering (come ID3D9Device in Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="2bfa2-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="2bfa2-149">Map e annullare sono implementate in interfacce derivate da ID3D10Resource, Begin, end e GetData sono implementate in interfacce derivate da ID3D10Asynchronous.</span><span class="sxs-lookup"><span data-stu-id="2bfa2-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2bfa2-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bfa2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bfa2-151">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="2bfa2-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





