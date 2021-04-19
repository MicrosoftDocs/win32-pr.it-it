---
description: Flag capacità driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305052"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Flag capacità driver.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Indica che il dispositivo può rispettare lo stato di rendering D3DRS_ALPHABLENDENABLE in modalità schermo intero, mentre si utilizza l'effetto di swapping FLIP o scarto. Questo vale solo quando gli Stati D3DRS_SRCBLEND o D3DRS_DESTBLEND sono impostati su uno dei seguenti elementi:
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>Il dispositivo può accelerare una copia di memoria dalla memoria di sistema alla memoria video locale. Questo limite garantisce che le chiamate a <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> saranno accelerate dall'hardware. Se questo limite è assente, queste chiamate riusciranno ma saranno più lente.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>Il dispositivo può accelerare una copia di memoria dalla memoria video locale alla memoria di sistema. Questo limite garantisce che le chiamate di <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> saranno accelerate dall'hardware. Se questo limite è assente, la chiamata avrà esito positivo ma sarà più lenta.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>Il driver di visualizzazione supporta l'interfaccia DDI DXVA-HD. Per altre informazioni su DXVA-HD DDI, vedere <a href="https://msdn.microsoft.com/library/dd835176.aspx">elaborazione High-Definition video</a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>Indica che il dispositivo può eseguire la correzione gamma da un buffer nascosto a finestra (contenente contenuto lineare) a un desktop sRGB.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Riservati non utilizzato.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro D3CAPS3 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




