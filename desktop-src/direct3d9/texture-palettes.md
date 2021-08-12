---
description: Direct3D 9 supporta trame con tavolozza tramite un set di 256 tavolozze di immissione associate all'oggetto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Tavolozze di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755abb638ab1dd94e25edd98b2daef5e65d5a54cca7baf21a74e7d06173eed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291166"
---
# <a name="texture-palettes-direct3d-9"></a>Tavolozze di trama (Direct3D 9)

Direct3D 9 supporta trame con tavolozza tramite un set di 256 tavolozze di immissione associate [**all'oggetto IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Una tavolozza viene resa corrente chiamando il [**metodo IDirect3DDevice9::SetCurrentTexturePalette.**](/windows/desktop/api) La tavolozza corrente viene usata per la traduzione di tutte le trame con tavolozza per tutte le fasi attive della trama. [**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) aggiorna tutte le 256 voci di una tavolozza. Ogni voce è una [**struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) nel formato D3DFMT \_ A8R8G8B8. Per impostazione predefinita, tutte le voci 0xFFFFFFFF.

Le [**tavolozze IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contengono un canale alfa. Questo canale alfa può essere usato quando è impostato il flag di funzionalità del dispositivo D3DPTEXTURECAPS ALPHAPALETTE, a indicare che il dispositivo supporta alfa \_ dalla tavolozza. Il canale alfa della tavolozza viene usato quando il formato della trama non ha un canale alfa. Se il dispositivo non supporta alfa dalla tavolozza e il formato della trama non ha un canale alfa, viene usato il valore 0xFF per alfa.

È disponibile un massimo di 65.536 (0x0000FFFF) tavolozze. Poiché le risorse di memoria associate al set di tavolozze sono proporzionali al numero massimo di tavolozza a cui fa riferimento un'applicazione, usare numeri di tavolozza contigui a partire da zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base di texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
