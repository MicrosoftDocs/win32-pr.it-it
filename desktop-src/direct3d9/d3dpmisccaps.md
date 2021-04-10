---
description: Flag di funzionalità primitive del driver varie.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225732"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Flag di funzionalità primitive del driver varie.



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
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>Il dispositivo può abilitare e disabilitare la modifica del buffer di profondità sulle operazioni pixel.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Il driver non esegue l'abbattimento dei triangoli. Corrisponde al membro D3DCULL_NONE del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>Il driver supporta l'abbattimento di triangolo in senso orario attraverso lo stato D3DRS_CULLMODE. (Si applica solo alle primitive triangolari). Questo flag corrisponde al membro D3DCULL_CW del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>Il driver supporta l'eliminazione in senso antiorario tramite lo stato D3DRS_CULLMODE. (Si applica solo alle primitive triangolari). Questo flag corrisponde al membro D3DCULL_CCW del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>Il dispositivo supporta le Scritture per canale per il buffer dei colori della destinazione di rendering tramite lo stato D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>Il dispositivo Ritaglia correttamente i punti ridimensionati di dimensioni maggiori di 1,0 ai piani di ritaglio definiti dall'utente.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>I clip del dispositivo vengono ritagliate primitive dei vertici. Specificare D3DUSAGE_DONOTCLIP quando la pipeline non deve eseguire alcun ritaglio. In tal caso, potrebbe essere necessario eseguire il ritaglio software aggiuntivo in fase di estrazione, in modo che il buffer dei vertici si trovi nella memoria di sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>Il dispositivo supporta <a href="d3dta.md">D3DTA</a> per il registro temporaneo.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>Il dispositivo supporta operazioni di fusione alfa diverse da D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Dispositivo di riferimento che non esegue il rendering.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>Il dispositivo supporta maschere di scrittura indipendenti per più trame di elementi o più destinazioni di rendering.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>Il dispositivo supporta le costanti per fase. Vedere D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>Il dispositivo supporta la conversione a sRGB dopo la fusione. 
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
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>Il dispositivo supporta la nebbia separata e l'alfa speculare. Molti dispositivi usano il canale alfa speculare per archiviare il fattore di nebbia.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>Il dispositivo supporta impostazioni di Blend separate per il canale alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>Il dispositivo supporta profondità di bit diverse per più destinazioni di rendering.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>Il dispositivo supporta operazioni post-pixel shader per più destinazioni di rendering.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>I dispositivi bloccano il fattore di Blend di nebbia per vertice.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro PrimitiveMiscCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
