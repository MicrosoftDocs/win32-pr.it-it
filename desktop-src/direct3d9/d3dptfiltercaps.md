---
description: Costanti di filtro della trama.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049276"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Costanti di filtro della trama.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>Il dispositivo supporta il filtro convoluzione monocromatico. Questo filtro è rappresentato dal membro D3DTEXF_CONVOLUTIONMONO del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> . 
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
<td>Il dispositivo supporta il filtro di esempio per punto per fase per le trame di ingrandimento. Il filtro di ingrandimento Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>Il dispositivo supporta il filtro di interpolazione bilineare per fase per ingrandire mipmap. Il filtro mapping MIP di interpolazione bilineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>Il dispositivo supporta il filtro anisotropico per fase per le trame di ingrandimento. Il filtro di ingrandimento anisotropico è rappresentato dal membro D3DTEXF_ANISOTROPIC del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>Il dispositivo supporta il filtro di esempio piramidale per fase per le trame di ingrandimento. Il filtro di ingrandimento piramidale è rappresentato dal membro D3DTEXF_PYRAMIDALQUAD del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>Il dispositivo supporta il filtraggio quadruplo per fase per fase per le trame di ingrandimento.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>Il dispositivo supporta l'applicazione di filtri di esempio per punto per fase per le trame minimizzazione. Il filtro minification Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>Il dispositivo supporta il filtro lineare per fase per le trame minimizzazione. Il filtro minification lineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>Il dispositivo supporta il filtro anisotropico per fase per le trame minimizzazione. Il filtro minification anisotropico è rappresentato dal membro D3DTEXF_ANISOTROPIC del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>Il dispositivo supporta il filtro di esempio piramidale per fase per le trame minimizzazione.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>Il dispositivo supporta il filtraggio quadruplo per fase per fase per le trame minimizzazione.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>Il dispositivo supporta l'applicazione di filtri di esempio per punto per fase per mipmap. Il filtro mapping MIP Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>Il dispositivo supporta il filtro di interpolazione bilineare per fase per mipmap. Il filtro mapping MIP di interpolazione bilineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dai membri TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
