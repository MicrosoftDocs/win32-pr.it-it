---
description: Le API di presentazione sono un set di metodi che controllano lo stato del dispositivo che influiscono sulle informazioni visualizzate dall'utente sul monitoraggio. Questi metodi includono l'impostazione delle modalità di visualizzazione e i metodi una volta per fotogramma usati per presentare le immagini all'utente.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Introduzione alla presentazione di una scena (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d909f2d7fcc04cd58c27c7598ca8f826b27f48a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341841"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Introduzione alla presentazione di una scena (Direct3D 9)

Le API di presentazione sono un set di metodi che controllano lo stato del dispositivo che influiscono sulle informazioni visualizzate dall'utente sul monitoraggio. Questi metodi includono l'impostazione delle modalità di visualizzazione e i metodi una volta per fotogramma usati per presentare le immagini all'utente.

-   [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9:: GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9:: GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Per comprendere le API di presentazione, è necessario conoscere i termini seguenti.

-   buffer anteriore. Un rettangolo di memoria convertito dalla scheda grafica e visualizzato sul monitor o su un altro dispositivo di output.
-   buffer nascosto. Una superficie il cui contenuto può essere innalzato al buffer anteriore.
-   catena di scambio. Raccolta di buffer back che possono essere presentati in modo seriale al buffer anteriore. In genere, una catena di scambio a schermo intero presenta le immagini successive con l'interfaccia DDI (flipping Device Driver Interface) e una catena di scambio a finestra presenta immagini con l'DDI blitting.

Poiché Direct3D 9 ha una catena di scambio come proprietà del dispositivo, è sempre presente almeno una catena di scambio per ogni dispositivo. L'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) dispone di un set di metodi che modificano la catena di scambio implicita e sono una copia dell'interfaccia della catena di scambio. Le applicazioni possono creare catene di scambio aggiuntive. Tuttavia, questa operazione non è necessaria per la tipica finestra singola o applicazione a schermo intero.

Il buffer anteriore non è esposto direttamente in Direct3D 9. Di conseguenza, le applicazioni non possono bloccare o eseguire il rendering nel buffer anteriore. Per informazioni dettagliate, vedere [accessing the color front buffer (Direct3D 9)](accessing-the-color-front-buffer.md).

> [!Note]  
> DirectX 7 forniva numerose API di presentazione che erano state richiamate insieme. Un esempio valido è la sequenza IDirectDraw7:: SetCooperativeLevel, IDirectDraw7:: SetDisplayMode e IDirectDraw7:: CreateSurface. Inoltre, i metodi IDirectDrawSurface7:: Flip e IDirectDrawSurface7:: BLT segnalavano il trasporto di frame di cui è stato eseguito il rendering sul monitor. Direct3D 9 comprime questi gruppi di API in due metodi principali, reset e present. Reimpostare sussume SetCooperativeLevel, SetDisplayMode, CreateSurface e alcuni parametri da capovolgere. Present sussume Flip e la presentazione USA blit.

 

Una chiamata a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) rappresenta una reimpostazione implicita del dispositivo. L'API Direct3D 9 non ha alcuna nozione di superficie primaria; non è possibile creare un oggetto che rappresenta l'area primaria. Viene considerato una proprietà interna del dispositivo.

Le rampe gamma sono associate a una catena di scambio e vengono modificate con i metodi [**IDirect3DDevice9:: GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) e [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 
