---
description: Descrive la relazione tra la frequenza di aggiornamento dell'adapter e la frequenza con cui vengono completate le operazioni Present o Present. Questi valori fungono anche da valori flag per il campo PresentationIntervals di D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f3fd05609e86682b4524e68e985f03abac59f1dbd4537d1ffd683990ca371fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527591"
---
# <a name="d3dpresent"></a>D3DPRESENT

Descrive la relazione tra la frequenza di aggiornamento [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) dell'adapter e la frequenza con cui [**vengono**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) completate le operazioni Present o Present. Questi valori fungono anche da valori flag per il campo PresentationIntervals di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTFLIP"></span><span id="d3dpresent_donotflip"></span><dl> <dt><strong>D3DPRESENT_DONOTFLIP</strong></dt> </dl></td>
<td style="text-align: left;">Usare il front buffer come superficie di origine e di destinazione durante il rendering. È pianificata una sincronizzazione dei frame, ma la superficie visualizzata non cambia. Questo flag è disponibile solo quando l'applicazione è in modalità schermo intero e D3DSWAPEFFECT_FLIPEX è stato specificato. <br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Una presentazione non può essere pianificata da un dispositivo hal. Se questo flag è impostato in una chiamata a <a href="/windows/desktop/api"><strong>Present</strong></a>e l'hardware è occupato per l'elaborazione o l'attesa di un intervallo di sincronizzazione verticale, Present restituirà D3DERR_WASSTILLDRAWING per indicare che l'operazione di blit è incompleta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Riservato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE viene applicato a questa <a href="/windows/desktop/api"><strong>chiamata present.</strong></a> Questo flag può essere specificato solo quando si usa D3DSWAPEFFECT_FLIPEX. I comportamenti delle presentazioni a finestra e a schermo intero sono gli stessi. Ciò è particolarmente utile per le app multimediali che vogliono eliminare i fotogrammi rilevati in ritardo e presentare i fotogrammi successivi in fase di composizione. Se questo flag viene specificato in modo non corretto, verrà restituito un errore di parametro non valido. Quando vengono accodati D3DPRESENT_FORCEIMMEDIATEs frame consecutivi, viene visualizzato solo l'ultimo frame, sia per la presentazione a finestra che per la presentazione a schermo intero.<br/> Questo flag è disponibile in Direct3D 9Ex in Windows 7 o versioni successive.<br/> Quando si D3DSWAPEFFECT_FLIPEX, ogni frame presentato usando D3DPRESENT_INTERVAL_IMMEDIATE o D3DPRESENT_INTERVAL_FORCEIMMEDIATE eseguirà l'override dell'intervallo corrente del frame precedente. Ad esempio, se si accoderanno i fotogrammi seguenti usando gli effetti di scambio seguenti: frame A (D3DPRESENT_INTERVAL_ONE), frame B(D3DPRESENT_INTERVAL_ONE), frame C(D3DPRESENT_INTERVAL_ONE), frame D(D3DPRESENT_INTERVAL_FORCEIMMEDIATE), il frame D eseguirà l'override dell'intervallo corrente del frame C. I frame visualizzati per intervallo corrente sono frame A, frame B, (frame C sottoposto a override da) frame D.<br/> Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Questo equivale quasi a D3DPRESENT_INTERVAL_ONE. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">Il driver attenderà il periodo di retrace verticale (il runtime seguirà per &quot; &quot; evitare la rimozione). <a href="/windows/desktop/api"><strong>Le</strong></a> operazioni presenti non saranno interessate più frequentemente rispetto all'aggiornamento dello schermo. il runtime verrà completato al massimo un'operazione Present per ogni periodo di aggiornamento dell'adapter. Equivale all'uso di D3DSWAPEFFECT_COPYVSYNC in DirectX 8.1. Questa opzione è sempre disponibile sia per le catene di scambio a finestra che per le catene di scambio a schermo intero. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">Il driver attenderà il periodo di retrace verticale. <a href="/windows/desktop/api"><strong>Le</strong></a> operazioni presenti non saranno interessate più frequentemente di ogni secondo aggiornamento dello schermo. Controllare il limite PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9)</strong></a>per verificare se D3DPRESENT_INTERVAL_TWO è supportato dal driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">Il driver attenderà il periodo di retrace verticale. <a href="/windows/desktop/api"><strong>Le</strong></a> operazioni presenti non saranno interessate più frequentemente rispetto a ogni terzo aggiornamento dello schermo. Controllare il limite PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9)</strong></a>per verificare se D3DPRESENT_INTERVAL_THREE è supportato dal driver.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">Il driver attenderà il periodo di retrace verticale. <a href="/windows/desktop/api"><strong>Le</strong></a> operazioni presenti non saranno interessate più frequentemente di ogni quarto aggiornamento dello schermo. Controllare il membro PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9)</strong></a>per verificare se D3DPRESENT_INTERVAL_FOUR è supportato dal driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">Il runtime aggiorna immediatamente l'area client della finestra e potrebbe eseguire questa operazione più volte durante il periodo di aggiornamento dell'adapter. Equivale all'uso di D3DSWAPEFFECT_COPY in DirectX 8. <a href="/windows/desktop/api"><strong>Le operazioni</strong></a> presenti potrebbero essere interessate immediatamente. Questa opzione è sempre disponibile sia per le catene di scambio a finestra che per le catene di scambio a schermo intero. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">Il contenuto del buffer nascosto da presentare si trova nello spazio colore lineare. <br/>
<ul>
<li>La presentazione verrà convertita in modo implicito dallo spazio lineare a sRGB (gamma = 2,2). Questa è l'unica conversione supportata.</li>
<li>Poiché questo flag rappresenta una proprietà del contenuto del buffer nascosto, il flag può essere specificato durante una <a href="/windows/desktop/api"><strong>chiamata present.</strong></a> In altre parole, un'applicazione può presentare contenuto lineare in un frame e quindi passare al contenuto corretto nel successivo.</li>
<li>Questo flag viene ignorato quando la catena di scambio è a schermo intero. Si noti che questo flag è disponibile solo nella versione esplicita della catena di scambio di <a href="/windows/desktop/api"><strong>Present</strong></a>. Il <a href="/windows/desktop/api"><strong>metodo Present</strong></a> non accetta un parametro flags.</li>
<li>Questo flag viene sempre accettato, ma avrà effetto solo quando il driver espone >D3DCAPS3_LINEAR_TO_SRGB_PresentATION.</li>
<li>L'unico formato di buffer nascosto supportato è <a href="d3dformat.md">X8R8G8B8.</a></li>
</ul>
Vedere <a href="gamma.md">Catene di scambio con finestre</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Ritaglia il contenuto sottoposto a rendering nel monitor o nel dispositivo di destinazione dell'adattatore, visualizza le anteprime per il contenuto nella visualizzazione Flip3D e nelle anteprime della barra delle applicazioni in altri monitor. <br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/> Vedere <a href="/windows/desktop/dwm/dwm-overview">Gestione finestre desktop</a> per altri dettagli su questa funzionalità di Windows Vista. Se non si è in esecuzione in modalità composizione desktop, il flag offre lo stesso comportamento di <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>.<br/>
<blockquote>
[!Note]<br />
Questo flag deve essere usato solo con l'effetto swap D3DSWAPEFFECT_FLIPEX. L'uso di questo flag <em>con altri</em> effetti di scambio è deprecato e potrebbe non funzionare nelle versioni future Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Aggiorna la posizione di sovrapposizione o i dati della chiave di colore senza causare un capovolgimento effettivo e senza modificare la durata con cui viene visualizzata l'immagine.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Disattiva l'hardware di sovrapposizione.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Ridisegna i dati colorkey.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Commenti

La modalità finestra supporta D3DPRESENT \_ INTERVAL \_ DEFAULT, D3DPRESENT \_ INTERVAL IMMEDIATE e \_ D3DPRESENT \_ INTERVAL \_ ONE. D3DPRESENT \_ INTERVAL DEFAULT e D3DPRESENT INTERVAL ONE sono quasi \_ equivalenti (vedere le informazioni \_ relative alla risoluzione del timer di \_ seguito). Le prestazioni sono simili a COPY VSYNC, in quanto è presente un solo oggetto per frame e impediscono la rimozione di \_ travi. Al contrario, D3DPRESENT INTERVAL IMMEDIATE tenterà di \_ fornire una \_ frequenza di presentazione illimitata.

La modalità schermo intero supporta un utilizzo simile a quello della modalità a finestre supportando D3DPRESENT INTERVAL IMMEDIATE indipendentemente dalla frequenza di aggiornamento o \_ \_ dall'effetto di scambio. D3DPRESENT INTERVAL DEFAULT usa la risoluzione predefinita del timer di sistema, mentre \_ \_ D3DPRESENT INTERVAL ONE chiama \_ \_ [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) per migliorare la risoluzione del timer di sistema. Ciò migliora la qualità della sincronizzazione verticale, ma usa un tempo di elaborazione leggermente superiore. Entrambi i parametri tentano di eseguire la sincronizzazione in verticale.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
