---
title: Impostare lo stato del dispositivo su pipeline dello shader a funzione fissa
description: In questa sezione vengono illustrate le differenze principali tra l'impostazione dello stato del dispositivo con la pipeline dello shader programmabile e a funzione fissa.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225503"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Impostare lo stato del dispositivo su pipeline dello shader a funzione fissa

In questa sezione vengono illustrate le differenze principali tra l'impostazione dello stato del dispositivo con la pipeline dello shader programmabile e a funzione fissa.

Ecco gli Stati del dispositivo che è possibile impostare solo per una pipeline a funzione fissa:

-   Trasformazione e illuminazione a funzione fissa: [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con D3DRS MODOOMBRA, D3DRS SPECULARENABLE, D3DRS Lighting, D3DRS ambient, D3DRS COLORVERTEX, D3DRS LOCALVIEWER, D3DRS NORMALIZENORMALS, D3DRS DIFFUSEMATERIALSOURCE, D3DRS SPECULARMATERIALSOURCE, D3DRS AMBIENTMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE, D3DRS VERTEXBLEND, D3DRS INDEXEDVERTEXBLENDENABLE, D3DRS TWEENFACTOR, IDirect3DDevice9: \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**: schiarenteable**](/windows/desktop/api), [**IDirect3DDevice9:: MultiplyTransform**](/windows/desktop/api), [**IDirect3DDevice9:: SetFVF**](/windows/desktop/api), [**IDirect3DDevice9:: selight**](/windows/desktop/api), [**IDirect3DDevice9:: sematerial**](/windows/desktop/api), [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
-   Funzione Fixed pixel shader: [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con D3DRS \_ TEXTUREFACTOR, [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Fog: [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con D3DRS \_ FOGENABLE, D3DRS FogColor \_ , D3DRS FOGTABLEMODE, D3DRS FOGSTART, D3DRS FOGEND, D3DRS FOGDENSITY \_ \_ \_ \_ , \_ \_ D3DRS RANGEFOGENABLE, D3DRS FOGVERTEXMODE

Ecco gli Stati di rendering del dispositivo che è possibile impostare con [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) per le pipeline di funzioni fisse e programmabili di shader:

-   Stato di destinazione di rendering: D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS COLORWRITEENABLE3 \_ , D3DRS \_ SRGBWRITEENABLE
-   Stato Depth: D3DRS \_ ZENABLE, D3DRS \_ ZWRITEENABLE, D3DRS \_ ZFUNC, D3DRS SLOPESCALEDEPTHBIAS \_ , D3DRS \_ DEPTHBIAS
-   Stato stencil: D3DRS STENCILENABLE, D3DRS STENCILFAIL, D3DRS STENCILZFAIL, D3DRS STENCILPASS, D3DRS STENCILFUNC, D3DRS STENCILREF, D3DRS STENCILMASK, D3DRS STENCILWRITEMASK, D3DRS TWOSIDEDSTENCILMODE, D3DRS \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ CCW \_ STENCILFAIL, D3DRS \_ CCW \_ STENCILZFAIL, D3DRS \_ CCW \_ STENCILPASS, D3DRS \_ CCW \_ STENCILFUNC
-   Fusione alfa: D3DRS \_ SRCBLEND, D3DRS \_ DESTBLEND, D3DRS \_ BLENDOP, D3DRS \_ \_ \_ \_ BLENDFACTOR, D3DRS SEPARATEALPHABLENDENABLE, D3DRS \_ SRCBLENDALPHA, D3DRS DESTBLENDALPHA, D3DRS BLENDOPALPHA
-   Test alfa: D3DRS \_ ALPHATESTENABLE, D3DRS \_ ALPHAREF, D3DRS \_ ALPHAFUNC
-   Stato rasterizzatore: D3DRS \_ FillMode, D3DRS \_ LASTPIXEL, D3DRS \_ DITHERENABLE (superfici a 16 bit)
-   Eliminazione: D3DRS \_ CULLMODE
-   Ritaglio: \_ ritaglio D3DRS, D3DRS \_ CLIPPLANEENABLE
-   Forbici: D3DRS \_ SCISSORTESTENABLE
-   Campionatori di trama: D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ D3DRS WRAP3, D3DRS WRAP4, D3DRS WRAP5, D3DRS WRAP6, D3DRS WRAP7, D3DRS WRAP8, D3DRS WRAP9, D3DRS WRAP10, D3DRS WRAP11, D3DRS WRAP12, D3DRS WRAP13, D3DRS WRAP14, D3DRS WRAP15,
-   Anti-aliasing: D3DRS \_ MULTISAMPLEANTIALIAS, D3DRS \_ MULTISAMPLEMASK, D3DRS \_ ANTIALIASEDLINEENABLE
-   Punti sprite: D3DRS \_ POINTSIZE, D3DRS \_ POINTSIZE \_ min, D3DRS POINTSPRITEENABLE, D3DRS POINTSIZE MAXD3DRS POINTSCALEENABLE \_ \_ \_ \_ , D3DRS \_ POINTSCALE \_ A, D3DRS POINTSCALE \_ \_ B, D3DRS \_ POINTSCALE \_ C
-   N-patch: D3DRS \_ PATCHEDGESTYLE, D3DRS POSITIONDEGREE, D3DRS NORMALDEGREE, D3DRS MINTESSELLATIONLEVEL, D3DRS MAXTESSELLATIONLEVEL, D3DRS \_ \_ \_ \_ \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z, D3DRS \_ ADAPTIVETESS \_ W, D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
