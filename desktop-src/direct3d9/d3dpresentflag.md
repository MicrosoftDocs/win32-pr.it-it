---
description: Costanti utilizzate da D3DPRESENT \_ PARAMETERS.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf3a8ad3a22f5104e4d4a78d3a01a29d07d757
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624557"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Costanti utilizzate da [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).



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
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Ritagliare un blit <a href="/windows/desktop/api"><strong>present</strong></a> in finestra nell'area client della finestra, all'interno dell'area dello schermo del monitor della scheda video che ha creato il dispositivo Direct3D. D3DPRESENTFLAG_DEVICECLIP non è valido con D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Impostare questo flag quando viene creata la catena di scambio o del dispositivo per abilitare l'eliminazione del buffer z. Se questo flag è impostato, il contenuto del buffer depth stencil non sarà valido dopo aver chiamato <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa. La rimozione dei dati z-buffer può aumentare le prestazioni e dipende dal driver. Il runtime di debug imposirà l'eliminazione cancellando il z-buffer su un valore costante dopo aver chiamato <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa.<br/> La rimozione dei dati z-buffer non è valida per tutti i formati bloccabili, D3DFMT_D16_LOCKABLE e D3DFMT_D32F_LOCKABLE. Qualsiasi uso di <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> che specifica un formato bloccabile e la rimozione del buffer z avrà esito negativo. Per altre informazioni sui formati, vedere <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Impostare questo flag se l'applicazione richiede la possibilità di bloccare direttamente il buffer nascosto. Si noti che i buffer non sono bloccabili a meno che l'applicazione non specifichi D3DPRESENTFLAG_LOCKABLE_BACKBUFFER quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>Reset</strong></a>. I buffer back bloccabili comportano un costo delle prestazioni per alcune configurazioni hardware grafiche. L'esecuzione di un'operazione di blocco (o l'uso di <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> per scrivere) sul buffer nascosto bloccabile riduce le prestazioni in molte schede. In questo caso, è consigliabile usare triangoli trame per spostare i dati nel buffer nascosto.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> In Direct3D9Ex questo flag non può essere impostato se D3DSWAPEFFECT è D3DSWAPEFFECT_FLIPEX, perché il modello flip consente al Gestione finestre desktop di accedere al buffer nascosto di un'applicazione. Una superficie condivisa tra processi non deve essere bloccata.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>I monitor ruotati vengono gestiti automaticamente con una copia rotante durante la presentazione, che non è molto efficiente. Questo flag indica che l'applicazione eseguirà la rotazione dello schermo. 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Le applicazioni possono ottenere la propria rotazione possibilmente usando una matrice di visualizzazione ruotata. I metodi <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> devono essere usati per trovare l'impostazione di rotazione corrente. I parametri Backbuffer Width e Height in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> devono usare l'orientamento orizzontale, mentre la struttura della modalità di visualizzazione a schermo intero deve essere la stessa di quella restituita da <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (ad esempio Larghezza e Altezza vengono scambiate quando vengono ruotate di 90 e 270 gradi).</p>
<p>Quando si usa Blocca sulle destinazioni di rendering ruotate, i presupposti dell'angolo superiore sinistro non sono più true, il SURFACE_DESC della destinazione di rendering rimarrà orizzontale (come implicito dai parametri di creazione) e la finestra GDI, le coordinate del mouse e tali coordinate devono essere tradotte correttamente quando vengono usate con la destinazione di rendering Direct3D e la scena.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Usare questo flag per specificare qualsiasi modalità di visualizzazione RAW enumerata dalla scheda di visualizzazione anche se Direct3D potrebbe aver indicato che la modalità non è valida. L'applicazione deve implementare questo comportamento in modo affidabile nel caso in cui la modalità desiderata non sia effettivamente valida. 
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
<td>Si tratta di un suggerimento per il driver che i buffer back conterranno dati video.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Specifica se la sovrimpressione è RGB a intervallo intero o RGB a intervallo limitato. L'impostazione di questo flag indica un intervallo RGB limitato. Nell'intervallo limitato RGB, l'intervallo RGB viene compresso in modo che 16:16:16 sia nero e 235:235:235 sia bianco.
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
<td>Specifica se la sovrimpressione è BT.601 o BT.709. L'impostazione di questo flag indica BT.709, per tv ad alta definizione (HDTV).
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
<td>Specifica se la sovrimpressione è YCbCr convenzionale o YCbCr estesa (xvYCC). L'impostazione di questo flag indica YCbCr esteso (xvYCC).
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
<td>L'impostazione di questo flag indica che lo swapchain contiene contenuto protetto e fa in modo che il runtime limiti automaticamente l'accesso al swapchain in modo che solo Desktop Windows Manager (DWM) possa usare lo swapchain.
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
<td>L'impostazione di questo flag indica che il driver deve limitare l'accesso a tutte le risorse condivise create per l'interazione DWM. Il chiamante deve creare un canale autenticato con il driver. Il driver deve quindi consentire l'accesso ai processi che tentano di aprire tali risorse condivise.
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



 

Queste costanti vengono usate da [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3d9types.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




