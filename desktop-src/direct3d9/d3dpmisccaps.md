---
description: Flag di funzionalità primitive del driver vari.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee88ba03b3c0a6d51c0100b20768df4cbf632d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624537"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Flag di funzionalità primitive del driver vari.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>Il dispositivo può abilitare e disabilitare la modifica del buffer di profondità nelle operazioni in pixel.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Il driver non esegue l'culling del triangolo. Corrisponde al membro D3DCULL_NONE del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerato D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>Il driver supporta l'culling del triangolo in senso orario attraverso lo D3DRS_CULLMODE stato. Si applica solo alle primitive di triangolo. Questo flag corrisponde al D3DCULL_CW membro del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerato D3DCULL.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>Il driver supporta l'culling in senso antiorario attraverso lo D3DRS_CULLMODE stato. Si applica solo alle primitive di triangolo. Questo flag corrisponde al D3DCULL_CCW membro del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerato D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>Il dispositivo supporta le scritture per canale per il buffer dei colori di destinazione del rendering tramite lo D3DRS_COLORWRITEENABLE stato.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>Il dispositivo ritaglia correttamente i punti di ridimensionamento maggiori di 1,0 ai piani di ritaglio definiti dall'utente.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Clip del dispositivo dopo la trasformazione delle primitive dei vertici. Specificare D3DUSAGE_DONOTCLIP quando la pipeline non deve eseguire alcun ritaglio. In questo caso, potrebbe essere necessario eseguire un ritaglio software aggiuntivo in fase di disegno, che richiede che il vertex buffer sia nella memoria di sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>Il dispositivo supporta <a href="d3dta.md">D3DTA per</a> il registro temporaneo.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>Il dispositivo supporta operazioni di alpha blending diverse da D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Dispositivo di riferimento di cui non viene eseguito il rendering.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>Il dispositivo supporta maschere di scrittura indipendenti per più trame di elementi o più destinazioni di rendering.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>Il dispositivo supporta costanti per fase. Vedere D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>Il dispositivo supporta la conversione in sRGB dopo la fusione. 
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
<td>Il dispositivo supporta osa separata e alfa speculare. Molti dispositivi usano il canale alfa speculare per archiviare il fattore di nebbia.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>Il dispositivo supporta impostazioni di blend separate per il canale alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>Il dispositivo supporta diverse profondità di bit per più destinazioni di rendering.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>Il dispositivo supporta le operazioni post-pixel shader per più destinazioni di rendering.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Fattore di fusione della nebbia per vertice delle piascie del dispositivo.</td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dal membro PrimitiveMiscCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         |  Valore          |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
