---
title: Livelli software
description: Il runtime di Direct3D 11 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516804"
---
# <a name="software-layers"></a><span data-ttu-id="a1e4c-104">Livelli software</span><span class="sxs-lookup"><span data-stu-id="a1e4c-104">Software Layers</span></span>

<span data-ttu-id="a1e4c-105">Il runtime di Direct3D 11 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="a1e4c-106">In questa sezione vengono descritte le funzionalità di ogni livello.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="a1e4c-107">Come regola generale, i livelli aggiungono funzionalità, ma non modificano il comportamento esistente.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="a1e4c-108">Le funzioni di base, ad esempio, avranno gli stessi valori restituiti indipendentemente dal livello di debug di cui viene creata un'istanza, sebbene sia possibile fornire un output di debug aggiuntivo se viene creata un'istanza del livello debug.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="a1e4c-109">Per creare livelli quando viene creato un dispositivo, chiamare [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e fornire uno o più valori di [**\_ flag di creazione del \_ dispositivo \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .</span><span class="sxs-lookup"><span data-stu-id="a1e4c-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="a1e4c-110">Direct3D 11 fornisce i livelli di runtime seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1e4c-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="a1e4c-111">Livello principale</span><span class="sxs-lookup"><span data-stu-id="a1e4c-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="a1e4c-112">Livello di debug</span><span class="sxs-lookup"><span data-stu-id="a1e4c-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="a1e4c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1e4c-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="a1e4c-114">Livello principale</span><span class="sxs-lookup"><span data-stu-id="a1e4c-114">Core Layer</span></span>

<span data-ttu-id="a1e4c-115">Il livello principale esiste per impostazione predefinita. fornire un mapping molto sottile tra l'API e il driver di dispositivo, riducendo al minimo l'overhead per le chiamate ad alta frequenza.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="a1e4c-116">Poiché il livello principale è essenziale per le prestazioni, viene eseguita solo la convalida critica.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="a1e4c-117">I livelli rimanenti sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="a1e4c-118">Livello di debug</span><span class="sxs-lookup"><span data-stu-id="a1e4c-118">Debug Layer</span></span>

<span data-ttu-id="a1e4c-119">Il livello di debug fornisce la convalida estesa di parametri e coerenza, ad esempio la convalida del collegamento shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione delle descrizioni degli errori.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="a1e4c-120">Per creare un dispositivo che supporta il livello di debug, è necessario installare DirectX SDK (per ottenere D3D11SDKLayers.dll), quindi specificare il flag di debug per la creazione di un **\_ \_ dispositivo \_ d3d11** quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o la funzione [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) .</span><span class="sxs-lookup"><span data-stu-id="a1e4c-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="a1e4c-121">Se si esegue l'applicazione con il livello di debug abilitato, l'applicazione sarà sostanzialmente più lenta.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="a1e4c-122">Tuttavia, per assicurarsi che l'applicazione sia pulita da errori e avvisi prima della spedizione, utilizzare il livello debug.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="a1e4c-123">Per altre informazioni, vedere [uso del livello di debug per eseguire il debug delle app](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="a1e4c-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="a1e4c-124">Per Windows 7 con aggiornamento della piattaforma per Windows 7 (KB2670838) o Windows 8. x, per creare un dispositivo che supporta il livello di debug, installare Windows Software Development Kit (SDK) per Windows 8. x per ottenere D3D11 \_1SDKLayers.dll.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="a1e4c-125">Per Windows 10, per creare un dispositivo che supporta il livello di debug, abilitare la funzionalità facoltativa "strumenti di grafica".</span><span class="sxs-lookup"><span data-stu-id="a1e4c-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="a1e4c-126">Passare al pannello impostazioni, in sistema, app & funzionalità, Gestisci funzionalità facoltative, aggiungere una funzionalità, quindi cercare "strumenti di grafica".</span><span class="sxs-lookup"><span data-stu-id="a1e4c-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="a1e4c-127">Per informazioni su come eseguire il debug di app DirectX in modalità remota, vedere [debug di app DirectX in modalità remota](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="a1e4c-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="a1e4c-128">In alternativa, è possibile abilitare o disabilitare il flag di debug usando il [Pannello di controllo DirectX](/previous-versions//bb219725(v=vs.85)) incluso in DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="a1e4c-129">Quando il livello di debug elenca le perdite di memoria, viene restituito un elenco di puntatori dell'interfaccia oggetto insieme ai relativi nomi descrittivi.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="a1e4c-130">Il nome descrittivo predefinito è " &lt; senza nome &gt; ".</span><span class="sxs-lookup"><span data-stu-id="a1e4c-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="a1e4c-131">È possibile impostare il nome descrittivo usando il metodo [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e il GUID **WKPDID \_ D3DDebugObjectName** in D3Dcommon. h.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="a1e4c-132">Ad esempio, per assegnare un nome a pTexture con il nome SDKLayer mytexture.jpg, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="a1e4c-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="a1e4c-133">In genere, è necessario compilare queste chiamate fuori dalla versione di produzione.</span><span class="sxs-lookup"><span data-stu-id="a1e4c-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1e4c-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1e4c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e4c-135">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="a1e4c-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 