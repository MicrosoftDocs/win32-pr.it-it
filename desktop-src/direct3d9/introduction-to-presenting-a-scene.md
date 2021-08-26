---
description: Le API di presentazione sono un set di metodi che controllano lo stato del dispositivo che influisce su ciò che l'utente vede nel monitoraggio. Questi metodi includono l'impostazione delle modalità di visualizzazione e i metodi una sola volta per frame usati per presentare le immagini all'utente.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Introduzione alla presentazione di una scena (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9abf584bad1bfbbde2bbfa2e9281acf3ad2173403507e06bbdc2abc5f5edd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846551"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Introduzione alla presentazione di una scena (Direct3D 9)

Le API di presentazione sono un set di metodi che controllano lo stato del dispositivo che influisce su ciò che l'utente vede nel monitoraggio. Questi metodi includono l'impostazione delle modalità di visualizzazione e i metodi una sola volta per frame usati per presentare le immagini all'utente.

-   [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Per comprendere le API di presentazione, è necessaria familiarità con i termini seguenti.

-   front buffer. Rettangolo di memoria convertito dall'adattatore grafico e visualizzato nel monitor o in un altro dispositivo di output.
-   buffer nascosto. Superficie il cui contenuto può essere promosso al front buffer.
-   catena di scambio. Raccolta di buffer nascosto che possono essere presentati in serie al front buffer. In genere, una catena di scambio a schermo intero presenta le immagini successive con l'interfaccia DDI (Device Driver Interface) capovolta e una catena di scambio a finestre presenta le immagini con il blitting DDI.

Poiché Direct3D 9 ha una catena di scambio come proprietà del dispositivo, esiste sempre almeno una catena di scambio per ogni dispositivo. [**L'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) include un set di metodi che modificano la catena di scambio implicita e sono una copia dell'interfaccia della catena di scambio. Le applicazioni possono creare catene di scambio aggiuntive; Tuttavia, questa operazione non è necessaria per la tipica applicazione a finestra singola o a schermo intero.

Il front buffer non è esposto direttamente in Direct3D 9. Di conseguenza, le applicazioni non possono bloccare o eseguire il rendering nel front buffer. Per informazioni dettagliate, vedere [Accesso al front buffer a colori (Direct3D 9).](accessing-the-color-front-buffer.md)

> [!Note]  
> DirectX 7 ha fornito una serie di API di presentazione che sono state chiamate insieme. Un buon esempio è la sequenza IDirectDraw7::SetCooperativeLevel, IDirectDraw7::SetDisplayMode e IDirectDraw7::CreateSurface. Inoltre, i metodi IDirectDrawSurface7::Flip e IDirectDrawSurface7::Blt segnalavano il trasporto dei fotogrammi sottoposti a rendering al monitoraggio. Direct3D 9 comprime questi gruppi di API in due metodi principali, Reset e Present. Reimpostare i sottosum setCooperativeLevel, SetDisplayMode, CreateSurface e alcuni dei parametri da capovolgere. I sottossum presenti vengono capovolti e la presentazione usa blit.

 

Una chiamata a [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) rappresenta una reimpostazione implicita del dispositivo. L'API Direct3D 9 non ha alcuna nozione di superficie primaria. non è possibile creare un oggetto che rappresenta la superficie primaria. È considerato una proprietà interna del dispositivo.

Le rampe gamma sono associate a una catena di scambio e vengono manipolate con i metodi [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) e [**IDirect3DDevice9::SetGammaRamp.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 
