---
description: Costanti di filtro delle trame.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343086"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Costanti di filtro delle trame.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>Il dispositivo supporta il filtro convoluzione monocromatica. Questo filtro è rappresentato dal D3DTEXF_CONVOLUTIONMONO del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>Il dispositivo supporta il filtro per campione di punti per fase per la ingrandimento delle trame. Il filtro di ingrandimento del campione di punti è rappresentato dal D3DTEXF_POINT del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Il dispositivo supporta il filtro di interpolazione bilineare per fase per ingrandire le mipmap. Il filtro mipmapping di interpolazione bilineare è rappresentato dal D3DTEXF_LINEAR del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Il dispositivo supporta il filtro anisotropo per fase per la ingrandimento delle trame. Il filtro di ingrandimento anisotropo è rappresentato dal D3DTEXF_ANISOTROPIC del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>Il dispositivo supporta il filtro dei campioni piramidali per fase per l'ingrandimento delle trame. Il filtro di ingrandimento piramidale è rappresentato dal D3DTEXF_PYRAMIDALQUAD membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Il dispositivo supporta il filtro quad gaussiano per fase per le trame di ingrandimento.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Il dispositivo supporta il filtro per campione di punti per fase per la minificazione delle trame. Il filtro di minificazione del campione di punti è rappresentato dal D3DTEXF_POINT membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Il dispositivo supporta il filtro lineare per fase per la minificazione delle trame. Il filtro di minificazione lineare è rappresentato dal D3DTEXF_LINEAR membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Il dispositivo supporta il filtro anisotropo per fase per la minificazione delle trame. Il filtro di minificazione anisotrop è rappresentato dal D3DTEXF_ANISOTROPIC membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Il dispositivo supporta il filtro dei campioni piramidali per fase per la minificazione delle trame.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Il dispositivo supporta il filtro quad gaussiano per fase per la minificazione delle trame.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Il dispositivo supporta il filtro per campione di punti per fase per le mipmap. Il filtro mipmapping di esempio di punti è rappresentato dal D3DTEXF_POINT membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>Il dispositivo supporta il filtro di interpolazione bilineare per fase per le mipmap. Il filtro mipmapping di interpolazione bilineare è rappresentato dal D3DTEXF_LINEAR del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dai membri TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni sulle costanti



|  Requisito                        | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
