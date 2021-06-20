---
description: Vedere un elenco di flag di funzionalità del driver D3DCAPS3. Include le definizioni, i valori e le descrizioni con collegamenti alle API.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408264"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Flag di funzionalità del driver.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Indica che il dispositivo può rispettare lo stato D3DRS_ALPHABLENDENABLE rendering in modalità schermo intero quando si usa l'effetto di scambio FLIP o DISCARD. Questo vale solo quando gli D3DRS_SRCBLEND o D3DRS_DESTBLEND sono impostati su uno dei valori seguenti:
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
<td>Il dispositivo può accelerare una copia della memoria dalla memoria di sistema alla memoria video locale. Questo limite garantisce che le <a href="/windows/desktop/api"><strong>chiamate UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>e UpdateTexture</strong></a> saranno accelerate dall'hardware. Se questo limite è assente, queste chiamate avranno esito positivo ma saranno più lente.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>Il dispositivo può accelerare una copia della memoria dalla memoria video locale alla memoria di sistema. Questo limite garantisce che le <a href="/windows/desktop/api"><strong>chiamate GetRenderTargetData</strong></a> saranno accelerate dall'hardware. Se questo limite è assente, questa chiamata avrà esito positivo ma sarà più lenta.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>Il driver video supporta DXVA-HD DDI. Per altre informazioni su DXVA-HD DDI, vedere Processing High-Definition Video (Elaborazione <a href="https://msdn.microsoft.com/library/dd835176.aspx">di High-Definition video).</a><br/> 
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
<td>Indica che il dispositivo può eseguire la correzione gamma da un buffer nascosto con finestra (contenente contenuto lineare) a un desktop sRGB.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Riservato; non utilizzato.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro D3CAPS3 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni sulle costanti



|  Requisito                        | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




