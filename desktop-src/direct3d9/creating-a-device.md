---
description: Per creare un dispositivo Direct3D, creare innanzitutto un oggetto Direct3D (vedere Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Creazione di un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304548"
---
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="60c01-103">Creazione di un dispositivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="60c01-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="60c01-104">Per creare un dispositivo Direct3D, creare innanzitutto un oggetto Direct3D (vedere [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="60c01-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="60c01-105">Tutti i dispositivi di rendering creati da un oggetto Direct3D condividono le stesse risorse fisiche.</span><span class="sxs-lookup"><span data-stu-id="60c01-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="60c01-106">Se si creano più dispositivi di rendering da un singolo oggetto Direct3D, verranno ricorrenti sanzioni per le prestazioni estreme perché condividono lo stesso hardware.</span><span class="sxs-lookup"><span data-stu-id="60c01-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="60c01-107">Per prima cosa, inizializzare i valori per la struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) usata per creare il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="60c01-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="60c01-108">Nell'esempio di codice seguente viene specificata un'applicazione a finestra in cui il buffer nascosto viene copiato nel buffer anteriore durante un'operazione di sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="60c01-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="60c01-109">Successivamente, creare il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="60c01-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="60c01-110">La chiamata [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) seguente specifica l'adattatore predefinito, un dispositivo HAL (Hardware Abstraction Layer) e l'elaborazione di vertici software.</span><span class="sxs-lookup"><span data-stu-id="60c01-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="60c01-111">Si noti che una chiamata per creare, rilasciare o reimpostare il dispositivo deve essere eseguita solo sullo stesso thread della routine della finestra della finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="60c01-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="60c01-112">Dopo aver creato il dispositivo, impostarne lo stato.</span><span class="sxs-lookup"><span data-stu-id="60c01-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60c01-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60c01-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60c01-114">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="60c01-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
