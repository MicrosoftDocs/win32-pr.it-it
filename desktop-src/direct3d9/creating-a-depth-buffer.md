---
description: Un buffer di profondità è una proprietà del dispositivo. Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura dei parametri D3DPRESENT, \_ come illustrato nell'esempio di codice seguente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Creazione di un buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126159"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Creazione di un buffer di profondità (Direct3D 9)

Un buffer di profondità è una proprietà del dispositivo. Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) , come illustrato nell'esempio di codice seguente.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Impostando il membro EnableAutoDepthStencil su **true**, si indica a Direct3D di gestire i buffer di profondità per l'applicazione. Si noti che AutoDepthStencilFormat deve essere impostato su un formato di buffer di profondità valido. Il \_ flag D3DFMT D16 specifica un buffer di profondità a 16 bit, se disponibile.

La chiamata seguente al metodo [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo che quindi crea un buffer di profondità.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



Il buffer di profondità viene impostato automaticamente come destinazione di rendering del dispositivo. Quando il dispositivo viene reimpostato, il buffer di profondità viene eliminato e ricreato automaticamente nelle nuove dimensioni.

Per creare una nuova superficie del buffer di profondità, usare il metodo [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Per impostare una nuova superficie del buffer di profondità per il dispositivo, usare il metodo [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .

Per usare il buffer di profondità nell'applicazione, è necessario abilitare il buffer di profondità. Per informazioni dettagliate, vedere [Abilitazione del buffer di profondità (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
