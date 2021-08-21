---
description: Il termine blit è abbreviazione di \# &0034;bit block transfer,&0034, ovvero il processo di trasferimento di blocchi di dati da una posizione in memoria a \# un'altra.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copia di superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d31d897bcb9e1a8fefa45a7770959ecb4121f807e4ca51d26ca7da5b5f5f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123378"
---
# <a name="copying-surfaces-direct3d-9"></a>Copia di superfici (Direct3D 9)

Il termine blit è l'abbreviazione di "trasferimento di blocchi di bit", ovvero il processo di trasferimento di blocchi di dati da una posizione in memoria a un'altra. L'interfaccia DDI (Device Driver Interface) di blitting continua a essere usata in Direct3D 9 come meccanismo principale per lo spostamento di rettangoli di pixel di grandi dimensioni per ogni frame, il meccanismo alla base del metodo [**IDirect3DDevice9::P resent**](/windows/desktop/api) orientato alla copia. Il trasporto della grafica nell'operazione blit viene eseguito dal [**metodo IDirect3DDevice9::UpdateTexture.**](/windows/desktop/api) La grafica può essere copiata anche in Direct3D 9 usando il metodo [**IDirect3DDevice9::UpdateSurface,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) che copia un subset rettangolare di pixel.

> [!Note]  
> Direct3D 9 offre funzioni D3DX che consentono di caricare grafica dai file, applicare la conversione dei colori e ridimensionare la grafica. Per altre informazioni sulle funzioni disponibili, vedere [Funzioni di trama in D3DX 9.](dx9-graphics-reference-d3dx-functions-texture.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
