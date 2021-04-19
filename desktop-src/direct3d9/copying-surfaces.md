---
description: Il termine blit è la sintassi abbreviata per &\# 0034; trasferimento di blocchi di bit &\# 0034, ovvero il processo di trasferimento di blocchi di dati da una posizione in memoria a un'altra.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copia di superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305110"
---
# <a name="copying-surfaces-direct3d-9"></a>Copia di superfici (Direct3D 9)

Il termine blit è la sintassi abbreviata per "bit Block Transfer", che è il processo di trasferimento di blocchi di dati da una posizione in memoria a un'altra. L'interfaccia DDI (Device Driver Interface) blitting continua a essere usata in Direct3D 9 come meccanismo principale per lo spostando rettangoli di grandi dimensioni di pixel in base ai singoli fotogrammi, il meccanismo dietro il metodo [**IDirect3DDevice9::P**](/windows/desktop/api) reinviato. Il trasporto di artwork nell'operazione blit viene eseguito dal metodo [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) . Le immagini possono anche essere copiate in Direct3D 9 usando il metodo [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , che copia un subset rettangolare di pixel.

> [!Note]  
> Direct3D 9 fornisce funzioni D3DX che consentono di caricare immagini da file, applicare la conversione dei colori e ridimensionare le immagini. Per altre informazioni sulle funzioni disponibili, vedere [funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9:: StretchRect**
</dt> </dl>

 

 
