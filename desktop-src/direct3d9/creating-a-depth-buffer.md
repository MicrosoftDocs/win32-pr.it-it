---
description: Un buffer di profondità è una proprietà del dispositivo. Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura D3DPRESENT PARAMETERS, come \_ illustrato nell'esempio di codice seguente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Creazione di un buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527923"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Creazione di un buffer di profondità (Direct3D 9)

Un buffer di profondità è una proprietà del dispositivo. Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura [**D3DPRESENT \_ PARAMETERS,**](d3dpresent-parameters.md) come illustrato nell'esempio di codice seguente.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Impostando il membro EnableAutoDepthStencil su **TRUE,** si indica a Direct3D di gestire i buffer di profondità per l'applicazione. Si noti che AutoDepthStencilFormat deve essere impostato su un formato di buffer di profondità valido. Il flag D3DFMT D16 specifica un buffer di profondità \_ a 16 bit, se disponibile.

La chiamata seguente al [**metodo IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo che crea quindi un buffer di profondità.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



Il buffer di profondità viene impostato automaticamente come destinazione di rendering del dispositivo. Quando il dispositivo viene reimpostato, il buffer di profondità viene eliminato automaticamente e ri-creato con le nuove dimensioni.

Per creare una nuova superficie del buffer di profondità, usare il [**metodo IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

Per impostare una nuova superficie di buffer di profondità per il dispositivo, usare il metodo [**IDirect3DDevice9::SetDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)

Per usare il buffer di profondità nell'applicazione, è necessario abilitare il buffer di profondità. Per informazioni dettagliate, vedere [Abilitazione del buffering di profondità (Direct3D 9).](enabling-depth-buffering.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
