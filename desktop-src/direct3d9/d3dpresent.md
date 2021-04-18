---
description: Descrive la relazione tra la frequenza di aggiornamento dell'adapter e la frequenza con cui vengono completate le operazioni presenti o presenti. Questi valori vengono usati anche come valori di flag per il campo PresentationIntervals di D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b8bf496c8c8e10d50b23ad4f784634fb983d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322922"
---
# <a name="d3dpresent"></a>D3DPRESENT

Descrive la relazione tra la frequenza di aggiornamento dell'adapter e la frequenza con cui vengono completate le operazioni [**presenti**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) o [**presenti**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) . Questi valori vengono usati anche come valori di flag per il campo PresentationIntervals di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

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
<td style="text-align: left;">Usare il buffer anteriore come superficie di origine e di destinazione durante il rendering. È stata pianificata una sincronizzazione dei frame, ma la superficie visualizzata non cambia. Questo flag è disponibile solo quando l'applicazione è in modalità a schermo intero e D3DSWAPEFFECT_FLIPEX è stato specificato. <br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Una presentazione non può essere pianificata da un dispositivo Hal. Se questo flag è impostato in una chiamata a <a href="/windows/desktop/api"><strong>present</strong></a>e l'hardware è impegnato nell'elaborazione o in attesa di un intervallo di sincronizzazione verticale, present restituirà D3DERR_WASSTILLDRAWING per indicare che l'operazione blit è incompleta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Riservato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE viene applicata alla chiamata <a href="/windows/desktop/api"><strong>corrente</strong></a> . Questo flag può essere specificato solo quando si usa D3DSWAPEFFECT_FLIPEX. I comportamenti di presentazione a finestra e a schermo intero sono gli stessi. Questa operazione è particolarmente utile per le app multimediali che desiderano rimuovere i frame rilevati in ritardo e presentare i frame successivi al momento della composizione. Se questo flag non è specificato correttamente, verrà restituito un errore di parametro non valido. Quando più frame consecutivi con D3DPRESENT_FORCEIMMEDIATEs vengono accodati, viene visualizzato solo l'ultimo frame per la presentazione a finestra e a schermo intero.<br/> Questo flag è disponibile nei sistemi operativi Direct3D 9Ex in Windows 7 o versioni successive.<br/> Quando si usa D3DSWAPEFFECT_FLIPEX, ogni frame presentato usando D3DPRESENT_INTERVAL_IMMEDIATE o D3DPRESENT_INTERVAL_FORCEIMMEDIATE sostituirà l'intervallo presente del frame precedente. Se, ad esempio, si accodano i frame seguenti usando gli effetti di swapping seguenti: frame A (D3DPRESENT_INTERVAL_ONE), frame B (D3DPRESENT_INTERVAL_ONE), frame C (D3DPRESENT_INTERVAL_ONE), frame D (D3DPRESENT_INTERVAL_FORCEIMMEDIATE), frame D esegue l'override dell'intervallo attuale di frame C. I fotogrammi visualizzati per ogni intervallo sono il frame A, il frame B, (frame C sottoposto a override da) frame D.<br/> Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Questa operazione è quasi equivalente a D3DPRESENT_INTERVAL_ONE. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">Il driver resterà in attesa del periodo di ritraccia verticale (il runtime eseguirà il &quot; fascio &quot; di seguito per impedire lo strappo). Le operazioni <a href="/windows/desktop/api"><strong>presenti</strong></a> non saranno interessate più frequentemente dell'aggiornamento dello schermo; il runtime viene completato al massimo un'operazione presente per ogni periodo di aggiornamento della scheda. Equivale a usare D3DSWAPEFFECT_COPYVSYNC in DirectX 8,1. Questa opzione è sempre disponibile per le catene di scambio a schermo intero e a finestra. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">Il driver resterà in attesa del periodo di ritraccia verticale. Le operazioni <a href="/windows/desktop/api"><strong>presenti</strong></a> non saranno interessate più frequentemente di ogni secondo aggiornamento dello schermo. Controllare il limite di PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) per verificare se D3DPRESENT_INTERVAL_TWO è supportato dal driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">Il driver resterà in attesa del periodo di ritraccia verticale. Le operazioni <a href="/windows/desktop/api"><strong>presenti</strong></a> non saranno interessate più frequentemente di ogni terzo aggiornamento dello schermo. Controllare il limite di PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) per verificare se D3DPRESENT_INTERVAL_THREE è supportato dal driver.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">Il driver resterà in attesa del periodo di ritraccia verticale. Le operazioni <a href="/windows/desktop/api"><strong>presenti</strong></a> non saranno interessate più frequentemente di ogni quarto aggiornamento dello schermo. Controllare il membro PresentationIntervals (vedere <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) per verificare se D3DPRESENT_INTERVAL_FOUR è supportato dal driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">Il runtime aggiorna immediatamente l'area client della finestra e potrebbe eseguire questa operazione più volte durante il periodo di aggiornamento dell'adapter. Questa operazione equivale all'uso di D3DSWAPEFFECT_COPY in DirectX 8. Le operazioni <a href="/windows/desktop/api"><strong>presenti</strong></a> potrebbero essere interessate immediatamente. Questa opzione è sempre disponibile per le catene di scambio a schermo intero e a finestra. Vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">Il contenuto del buffer nascosto da presentare si trova nello spazio dei colori lineare. <br/>
<ul>
<li>La presentazione eseguirà la conversione implicita dallo spazio lineare a sRGB (gamma = 2,2). Questa è l'unica conversione supportata.</li>
<li>Poiché questo flag rappresenta una proprietà del contenuto del buffer nascosto, è possibile specificare il flag durante una chiamata <a href="/windows/desktop/api"><strong>corrente</strong></a> . In altre parole, un'applicazione può presentare contenuto lineare in un frame e quindi passare al contenuto corretto nella successiva.</li>
<li>Questo flag viene ignorato quando la catena di scambio è a schermo intero. Si noti che questo flag è disponibile solo nella versione della catena di scambio esplicita di <a href="/windows/desktop/api"><strong>present</strong></a>. Il metodo <a href="/windows/desktop/api"><strong>present</strong></a> non accetta un parametro flags.</li>
<li>Questo flag è sempre accettato, ma verrà applicato solo quando il driver espone >D3DCAPS3_LINEAR_TO_SRGB_PresentATION.</li>
<li>L'unico formato di buffer nascosto supportato è <a href="d3dformat.md">X8R8G8B8</a>.</li>
</ul>
Vedere <a href="gamma.md">catene di scambio con finestra</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Consente di ritagliare il contenuto di cui è stato eseguito il rendering nel monitor/dispositivo a cui è destinata la scheda, Mostra le anteprime per il contenuto nella visualizzazione Flip3D e nelle anteprime delle barre degli altri monitoraggi. <br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/> Per ulteriori informazioni su questa funzionalità di Windows Vista, vedere <a href="/windows/desktop/dwm/dwm-overview">Gestione finestre desktop</a> . Se non si esegue la modalità composizione desktop, il flag fornisce lo stesso comportamento del <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>.<br/>
<blockquote>
[!Note]<br />
Questo flag deve essere usato solo con effetto di scambio D3DSWAPEFFECT_FLIPEX. L'uso di questo flag con <em>altri</em> effetti di swap è deprecato e potrebbe non funzionare nelle versioni future di Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Aggiorna la posizione di sovrapposizione o i dati colorkey senza causare un capovolgimento effettivo e senza modificare la durata con cui viene visualizzata l'immagine.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Disattiva l'hardware sovrapposto.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Ridisegnato i dati colorkey.<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Commenti

La modalità finestra supporta l'intervallo di D3DPRESENT \_ \_ predefinito, l' \_ intervallo D3DPRESENT \_ immediato e l'intervallo di D3DPRESENT \_ \_ . \_ \_ Il valore predefinito dell'intervallo di D3DPRESENT e l'intervallo di D3DPRESENT \_ \_ sono quasi equivalenti. vedere le informazioni relative alla risoluzione del timer riportata di seguito. Eseguono in modo analogo \_ la copia di VSync in quanto è presente un solo presente per fotogramma e impediscono lo strappo con Beam-after. Al contrario, D3DPRESENT \_ interval \_ immediate tenterà di fornire una frequenza di presentazione illimitata.

La modalità a schermo intero supporta un utilizzo simile come modalità a finestra, grazie \_ al supporto dell'intervallo di D3DPRESENT \_ immediato indipendentemente dalla frequenza di aggiornamento o dall'effetto di scambio. D3DPRESENT \_ interval \_ default usa la risoluzione predefinita del timer di sistema, mentre l' \_ intervallo D3DPRESENT \_ uno chiama [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) per migliorare la risoluzione del timer di sistema. Ciò migliora la qualità della sincronizzazione verticale, ma utilizza un tempo di elaborazione leggermente superiore. Entrambi i parametri tentano di eseguire la sincronizzazione verticalmente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
