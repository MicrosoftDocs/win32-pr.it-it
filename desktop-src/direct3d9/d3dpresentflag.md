---
description: Costanti utilizzate dai parametri D3DPRESENT \_ .
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304792"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Costanti utilizzate dai [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).



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
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Ritagliare un blit <a href="/windows/desktop/api"><strong>presente</strong></a> nella finestra dell'area client della finestra, all'interno dell'area dello schermo del monitor della scheda video che ha creato il dispositivo Direct3D. D3DPRESENTFLAG_DEVICECLIP non è valido con D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Impostare questo flag quando si crea il dispositivo o la catena di scambio per abilitare l'eliminazione del buffer z. Se questo flag è impostato, il contenuto del buffer depth stencil non sarà valido dopo la chiamata a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa. L'eliminazione dei dati del buffer z può migliorare le prestazioni e dipende dal driver. Il runtime di debug imporrà l'eliminazione deselezionando il buffer z su un valore costante dopo la chiamata di <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa.<br/> L'eliminazione dei dati del buffer z non è valida per tutti i formati bloccabili, D3DFMT_D16_LOCKABLE e D3DFMT_D32F_LOCKABLE. Qualsiasi uso di <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> che specifica un formato bloccabile e l'eliminazione del buffer z avrà esito negativo. Per ulteriori informazioni sui formati, vedere <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Impostare questo flag se l'applicazione richiede la possibilità di bloccare direttamente il buffer nascosto. Si noti che i buffer indietro non sono bloccabili, a meno che l'applicazione non specifichi D3DPRESENTFLAG_LOCKABLE_BACKBUFFER quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>Reset</strong></a>. I buffer back bloccabili comportano un costo in termini di prestazioni in alcune configurazioni hardware grafiche. L'esecuzione di un'operazione di blocco (o l'utilizzo di <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> per la scrittura) sul buffer nascosto blocca le prestazioni in molte schede. In questo caso, è consigliabile usare triangoli con trama per spostare i dati nel buffer nascosto.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> In Direct3D9Ex non è possibile impostare questo flag se il D3DSWAPEFFECT è D3DSWAPEFFECT_FLIPEX, perché il modello Flip consente al Gestione finestre desktop di accedere al buffer nascosto di un'applicazione. Una superficie condivisa tra processi non deve essere bloccata.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>I monitoraggi ruotati vengono gestiti automaticamente con una copia girevole durante la presentazione, operazione non molto efficiente. Questo flag indica che l'applicazione eseguirà la rotazione dello schermo. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Le applicazioni possono ottenere la propria rotazione possibilmente utilizzando una matrice di viste ruotata. I metodi <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> devono essere utilizzati per individuare l'impostazione di rotazione corrente. I parametri della larghezza e dell'altezza del buffer in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> devono usare l'orientamento orizzontale, mentre la struttura della modalità di visualizzazione a schermo intero deve corrispondere a quella restituita da <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> , ad esempio la larghezza e l'altezza vengono scambiate quando si ruotano 90 e 270 gradi.</p>
<p>Quando si usa il blocco su destinazioni di rendering ruotate, i presupposti dell'angolo superiore sinistro non sono più contenuta true, la destinazione di rendering SURFACE_DESC rimarrà orizzontale (in base a quanto previsto dai parametri di creazione) e la finestra GDI, le coordinate del mouse e tale necessità di essere convertite correttamente quando vengono usate con la destinazione e la scena di rendering Direct3D.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Utilizzare questo flag per specificare qualsiasi modalità di visualizzazione non ELABORAta enumerata dalla scheda video anche se Direct3D potrebbe indicare che la modalità non è valida. L'applicazione deve implementare questa operazione in modo affidabile, nel caso in cui la modalità desiderata non sia effettivamente valida. 
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
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Si tratta di un suggerimento per il driver che i buffer indietro conterranno dati video.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Specifica se la sovrimpressione è di intervallo completo RGB o RGB a intervalli limitati. L'impostazione di questo flag indica un intervallo limitato di RGB. In RGB con intervallo limitato, l'intervallo RGB viene compresso in modo che 16:16:16 sia nero e 235:235:235 sia bianco.
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Specifica se la sovrimpressione è BT. 601 o BT. 709. L'impostazione di questo flag indica BT. 709 per la TV ad alta definizione (HDTV).
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Specifica se la sovrimpressione è YCbCr convenzionale o YCbCr esteso (xvYCC). L'impostazione di questo flag indica YCbCr esteso (xvYCC).
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
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>L'impostazione di questo flag indica che il presentazione catena contiene contenuto protetto e fa in modo che il runtime limiti l'accesso al presentazione catena in modo che solo il desktop di Windows Manager (DWM) possa usare presentazione catena.
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>L'impostazione di questo flag indica che il driver deve limitare l'accesso alle risorse condivise create per l'interazione con DWM. Il chiamante deve creare un canale autenticato con il driver. Il driver deve quindi consentire l'accesso ai processi che tentano di aprire tali risorse condivise.
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Queste costanti vengono usate dai [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




