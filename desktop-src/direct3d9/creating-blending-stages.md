---
description: Una fase di fusione è un set di operazioni di trama e i relativi argomenti che definiscono il modo in cui vengono combinate le trame.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Creazione di fasi di fusione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126882"
---
# <a name="creating-blending-stages-direct3d-9"></a>Creazione di fasi di fusione (Direct3D 9)

Una fase di fusione è un set di operazioni di trama e i relativi argomenti che definiscono il modo in cui vengono combinate le trame. Quando si crea una fase di fusione, le applicazioni C++ richiamano il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . La prima chiamata specifica l'operazione eseguita. Due chiamate aggiuntive definiscono gli argomenti a cui viene applicata l'operazione. Nell'esempio di codice seguente viene illustrata la creazione di una fase di Blend.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



I dati Texel nelle trame contengono valori di colore e alfa. Le applicazioni possono definire operazioni separate per i valori di colore e alfa in una singola fase di fusione. Ogni operazione, colore e alfa ha i propri argomenti. Per informazioni dettagliate, vedere [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Sebbene non faccia parte dell'API Direct3D, è possibile inserire le macro seguenti nell'applicazione per abbreviare il codice necessario per la creazione di fasi di blending delle trame.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> </dl>

 

 
