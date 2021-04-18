---
description: Direct3D 9 supporta le trame con tavolozza tramite un set di tavolozze di voci 256 associate all'oggetto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Tavolozze delle trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303974"
---
# <a name="texture-palettes-direct3d-9"></a>Tavolozze delle trame (Direct3D 9)

Direct3D 9 supporta le trame con tavolozza tramite un set di tavolozze di voci 256 associate all'oggetto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Una tavolozza viene resa corrente chiamando il metodo [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) . La tavolozza corrente viene usata per tradurre tutte le trame con tavolozza per tutte le fasi di trama attive. [**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) Aggiorna tutte le voci della tavolozza 256. Ogni voce è una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) nel formato D3DFMT \_ A8R8G8B8. Per impostazione predefinita, tutte le voci sono 0xFFFFFFFF.

Le tavolozze [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contengono un canale alfa. Questo canale alfa può essere usato quando \_ è impostato il flag di funzionalità del dispositivo ALPHAPALETTE D3DPTEXTURECAPS, che indica che il dispositivo supporta Alpha dalla tavolozza. Il canale alfa della tavolozza viene usato quando il formato della trama non ha un canale alfa. Se il dispositivo non supporta Alpha dalla tavolozza e il formato di trama non ha un canale alfa, viene usato il valore 0xFF per Alpha.

È disponibile un massimo di 65.536 tavolozze (0x0000FFFF). Poiché le risorse di memoria associate al set di tavolozze sono proporzionali al numero massimo di tavolozza a cui fa riferimento un'applicazione, utilizzare numeri di tavolozza contigui a partire da zero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
