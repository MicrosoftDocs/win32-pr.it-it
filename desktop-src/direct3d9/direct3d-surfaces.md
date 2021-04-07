---
description: Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema. Le superfici vengono gestite dall'interfaccia IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superfici Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745399"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Superfici Direct3D (Direct3D 9)

Una superficie rappresenta un'area lineare della memoria di visualizzazione e in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema. Le superfici vengono gestite dall'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .

-   Buffer anteriore. Un rettangolo di memoria convertito dalla scheda grafica e visualizzato sul monitor. In Direct3D un'applicazione non scrive mai direttamente nel buffer anteriore.
-   Buffer nascosto. Un rettangolo di memoria in cui un'applicazione può scrivere direttamente. Il buffer nascosto non viene mai visualizzato direttamente sul monitor.
-   Capovolgimento di superfici. Processo di trasferimento del buffer nascosto nel buffer anteriore.
-   Catena di scambio. Raccolta di uno o più buffer back che possono essere presentati in modo seriale al buffer anteriore.

## <a name="getting-a-surface"></a>Recupero di una superficie

Creare una superficie chiamando uno di questi metodi:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

I formati di superficie determinano come vengono interpretati i dati per ogni pixel nella memoria di superficie. Direct3D usa il membro [D3DFORMAT](d3dformat.md) della struttura [**D3DSURFACE \_ desc**](d3dsurface-desc.md) per descrivere il formato della superficie. È possibile recuperare il formato di una superficie esistente chiamando il metodo [**getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .

Una volta creata una superficie, è possibile ottenere un puntatore chiamando uno di questi metodi:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

L'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) consente di accedere indirettamente alla memoria tramite il metodo [**UpdateSurface**](/windows/desktop/api) . Questo metodo consente di copiare un'area rettangolare di pixel da un'interfaccia **IDirect3DSurface9** a un'altra interfaccia **IDirect3DSurface9** . L'interfaccia Surface dispone inoltre di metodi per accedere direttamente alla memoria di visualizzazione. Ad esempio, è possibile usare il metodo [**LockRect**](/windows/desktop/api) per bloccare un'area rettangolare della memoria di visualizzazione. È importante chiamare [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) dopo aver terminato di utilizzare l'area rettangolare bloccata sulla superficie.

## <a name="additional-surface-topics"></a>Argomenti aggiuntivi sull'area

Scopri di più su come usare le superfici con uno di questi argomenti:

-   [Formati di superficie (Direct3D 9)](surface-formats.md)
-   [Che cos'è una catena di scambio? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Spessore rispetto a pitch (Direct3D 9)](width-vs--pitch.md)
-   [Capovolgimento di superfici (Direct3D 9)](flipping-surfaces.md)
-   [Capovolgimento della pagina e buffering indietro (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copia in superfici (Direct3D 9)](copying-to-surfaces.md)
-   [Copia di superfici (Direct3D 9)](copying-surfaces.md)
-   [Accesso diretto alla memoria di Surface (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Dati della superficie privata (Direct3D 9)](private-surface-data.md)
-   [Controlli gamma (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
