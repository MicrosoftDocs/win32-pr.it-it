---
description: Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, anche se le superfici possono esistere nella memoria di sistema. Le superfici sono gestite dall'interfaccia IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superfici Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529320673eca39cf4b9afdb96377295d595191fd79cd81c316b258841d82ae6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988201"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Superfici Direct3D (Direct3D 9)

Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, anche se le superfici possono esistere nella memoria di sistema. Le superfici sono gestite [**dall'interfaccia IDirect3DSurface9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)

-   Front Buffer. Rettangolo di memoria convertito dall'adattatore grafico e visualizzato sul monitor. In Direct3D un'applicazione non scrive mai direttamente nel front buffer.
-   Buffer nascosto. Rettangolo di memoria in cui un'applicazione può scrivere direttamente. Il buffer nascosto non viene mai visualizzato direttamente sul monitor.
-   Capovolgimento delle superfici. Processo di spostamento del buffer nascosto nel front buffer.
-   Catena di scambio. Raccolta di uno o più buffer nascosto che possono essere presentati in serie al front buffer.

## <a name="getting-a-surface"></a>Recupero di una superficie

Creare una superficie chiamando uno di questi metodi:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

I formati di superficie determinano il modo in cui vengono interpretati i dati per ogni pixel nella memoria di superficie. Direct3D usa il [membro D3DFORMAT](d3dformat.md) della [**struttura D3DSURFACE \_ DESC**](d3dsurface-desc.md) per descrivere il formato della superficie. È possibile recuperare il formato di una superficie esistente chiamando il [**metodo GetDesc.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)

Dopo aver creato una superficie, è possibile ottenere un puntatore chiamando uno di questi metodi:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

[**L'interfaccia IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) consente di accedere indirettamente alla memoria tramite [**il metodo UpdateSurface.**](/windows/desktop/api) Questo metodo consente di copiare un'area rettangolare di pixel da **un'interfaccia IDirect3DSurface9** a un'altra **interfaccia IDirect3DSurface9.** L'interfaccia surface include anche metodi per accedere direttamente alla memoria di visualizzazione. Ad esempio, è possibile usare il [**metodo LockRect**](/windows/desktop/api) per bloccare un'area rettangolare della memoria di visualizzazione. È importante chiamare [**UnlockRect dopo**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) aver finito di lavorare con l'area rettangolare bloccata sulla superficie.

## <a name="additional-surface-topics"></a>Argomenti aggiuntivi su Surface

Altre informazioni su come usare le superfici con uno di questi argomenti:

-   [Formati surface (Direct3D 9)](surface-formats.md)
-   [Che cos'è una catena di scambio? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Larghezza e passo (Direct3D 9)](width-vs--pitch.md)
-   [Capovolgimento delle superfici (Direct3D 9)](flipping-surfaces.md)
-   [Capovolgimento pagina e buffering indietro (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copia su superfici (Direct3D 9)](copying-to-surfaces.md)
-   [Copia di superfici (Direct3D 9)](copying-surfaces.md)
-   [Accesso diretto a Surface Memory (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Private Surface Data (Direct3D 9)](private-surface-data.md)
-   [Controlli Gamma (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
