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
# <a name="creating-a-device-direct3d-9"></a>Creazione di un dispositivo (Direct3D 9)

Per creare un dispositivo Direct3D, creare innanzitutto un oggetto Direct3D (vedere [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Tutti i dispositivi di rendering creati da un oggetto Direct3D condividono le stesse risorse fisiche. Se si creano più dispositivi di rendering da un singolo oggetto Direct3D, verranno ricorrenti sanzioni per le prestazioni estreme perché condividono lo stesso hardware.

Per prima cosa, inizializzare i valori per la struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) usata per creare il dispositivo Direct3D. Nell'esempio di codice seguente viene specificata un'applicazione a finestra in cui il buffer nascosto viene copiato nel buffer anteriore durante un'operazione di sincronizzazione verticale.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Successivamente, creare il dispositivo Direct3D. La chiamata [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) seguente specifica l'adattatore predefinito, un dispositivo HAL (Hardware Abstraction Layer) e l'elaborazione di vertici software.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Si noti che una chiamata per creare, rilasciare o reimpostare il dispositivo deve essere eseguita solo sullo stesso thread della routine della finestra della finestra attiva.

Dopo aver creato il dispositivo, impostarne lo stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
