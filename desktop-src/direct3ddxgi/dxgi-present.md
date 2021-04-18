---
description: Le \_ costanti DXGI presenti specificano le opzioni per la presentazione dei frame nell'output.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322516"
---
# <a name="dxgi_present"></a>DXGI \_ presente

Le costanti **DXGI \_ presenti** specificano le opzioni per la presentazione dei frame nell'output.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">Presentare un frame da ogni buffer (a partire dal buffer corrente) nell'output.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Presentare un frame dal buffer corrente all'output. Usare questo flag in modo che la presentazione possa usare la sincronizzazione vuota verticale anziché sequenziare i buffer nella catena nel modo consueto.<br/>
<blockquote>
[!Note]<br />
Se l'applicazione chiamante imposta la costante DXGI_PRESENT_DO_NOT_SEQUENCE sulla prima operazione presente (ovvero, quando non è presente alcun buffer corrente), il runtime ignora tale operazione e non chiama il driver.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Non presentare il frame all'output. Lo stato della catena di scambio verrà testato e verranno restituiti gli errori appropriati. DXGI_PRESENT_TEST deve essere utilizzato solo quando si passa dallo stato di inattività; non usarlo per determinare quando passare allo stato inattivo perché questa operazione può lasciare la catena di scambio non in grado di uscire dalla modalità schermo intero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Specifica che il runtime eliminerà i presentamenti in coda in attesa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Specifica che il runtime non riuscirà a eseguire la presentazione, ovvero non riesce una chiamata a <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>, con il codice di errore <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> se il thread chiamante è bloccato. il runtime restituisce DXGI_ERROR_WAS_STILL_DRAWING anziché rimanere in sospensione fino a quando la dipendenza non viene risolta.<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Indica che il contenuto della presentazione verrà visualizzato solo nell'output specifico. Il contenuto non sarà visibile in altri output. Ad esempio, se l'utente tenta di rilocare il contenuto video in un altro output, il contenuto video non sarà visibile. <br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8. <br/>
<blockquote>
[!Note]<br />
Questo flag deve essere usato solo con effetto di scambio <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> o DXGI_SWAP_EFFECT_FLIP_DISCARD. L'uso di questo flag con <em>altri</em> effetti di swap è deprecato e potrebbe non funzionare nelle versioni future di Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Indica che se lo stereo presente deve essere ridotto a mono, viene usata la visualizzazione a destra anziché la visualizzazione a sinistra.<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Indica che la presentazione deve usare il buffer sinistro come buffer mono. Un'applicazione chiama il metodo <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1:: IsTemporaryMonoSupported</strong></a> per determinare se una catena di scambio supporta &quot; mono temporaneo &quot; .<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Questo flag deve essere impostato da app multimediali che attualmente usano una durata presente personalizzata (frequenza di aggiornamento personalizzata). Vedere <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Questo valore è supportato a partire da Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Consentire lo strappo è un requisito di visualizzazione frequenza di aggiornamento variabili.<br/> Le condizioni per l'utilizzo di DXGI_PRESENT_ALLOW_TEARING durante la presente sono le seguenti:<br/>
<ul>
<li>La catena di scambio deve essere creata con il flag <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> .</li>
<li>L'intervallo di sincronizzazione passato a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>present</strong></a> (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) deve essere 0.</li>
<li>Impossibile utilizzare il flag di DXGI_PRESENT_ALLOW_TEARING in un'applicazione attualmente in modalità esclusiva a schermo intero (impostata chiamando <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState (true)</strong></a>). Può essere usato solo in modalità finestra. Per usare questo flag nelle app Win32 a schermo intero, l'applicazione deve essere presente in una finestra senza bordi a schermo intero e disabilitare il cambio automatico ALT + INVIO a schermo intero con <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory:: MakeWindowAssociation</strong></a>. Le app UWP che entrano in modalità a schermo intero chiamando <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> sono finestre senza bordi a schermo intero e possono usare il flag.</li>
</ul>
Se si chiama <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>present</strong></a> (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) con questo flag e non si soddisfano le condizioni precedenti, verrà restituito un errore di DXGI_ERROR_INVALID_CALL all'applicazione chiamante.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Le opzioni di presentazione vengono fornite durante la chiamata di [**IDXGISwapChain::P**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) reinviata o [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . I buffer sono specificati nella descrizione della catena di scambio (vedere [**DXGI \_ swap \_ Chain \_ desc**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI \_ swap \_ Chain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

DXGI \_ present \_ Restart è valido solo per le catene di scambio flip-model e a schermo intero. Le applicazioni possono usare DXGI \_ present \_ Restart per il ripristino da problemi di riproduzione, oltre a rimuovere le presentazioni accodate in precedenza. L'eliminazione di presentazioni in coda in precedenza è utile se le presentazioni in coda sono scenari con finestra. In particolare, la presentazione accodata in precedenza potrebbe avere presupposto che la finestra abbia una dimensione precedente, ovvero un'operazione di ridimensionamento eseguita dopo l'invio.

DXGI \_ \_ \_ \_ è valido solo per le catene di scambio che hanno specificato un determinato output per limitare il contenuto quando sono state create le catene di scambio ([**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Se non è presente alcun output da limitare, il flag non è valido.

DXGI \_ presenta lo stereo \_ \_ preferenziale \_ right indica che se lo stereo presente deve essere ridotto a mono, è consigliabile usare l'occhio destro anziché l'occhio sinistro (impostazione predefinita). È possibile utilizzare questo flag se un lato è di qualità superiore, ad esempio se la coppia stereo viene sintetizzata da un'immagine standard.

DXGI \_ present \_ stereo \_ Temporary \_ mono indica che il presente deve usare il buffer a sinistra come buffer mono. È possibile utilizzare questo flag per evitare di aggiornare il buffer corretto quando un'applicazione non dispone temporaneamente di contenuto stereo. È consigliabile usare questo flag quando possibile perché consente un'ottimizzazione significativa da parte del sistema operativo e, in alcuni casi, può evitare gli artefatti di modifica della modalità visibile.

Per \_ \_ \_ \_ la maggior parte delle applicazioni che si prevede di usare nuovamente lo stereo, è consigliabile usare il flag mono temporaneo stereo DXGI presente in preferenza per passare a una catena di scambio mono. È necessario bilanciare l'utilizzo di questo flag nelle applicazioni con esecuzione estremamente prolungata o che raramente visualizzano lo stereo dallo svantaggio della memoria inutilizzata.

> [!Note]  
> Le applicazioni a schermo intero che passano a una catena di scambio mono provocano una modifica della modalità che in genere presenta elementi visibili, ad esempio "lampeggiante". Tuttavia, la mono temporanea potrebbe non essere supportata per le catene di scambio a schermo intero.

 

Il DXGI \_ presente \_ stereo \_ preferisce \_ right e DXGI \_ i \_ \_ flag mono temporanei stereo sono \_ applicabili solo alle catene di scambio stereo. Se vengono usati quando si presentano catene di scambio mono, si verifica un'operazione non valida.

Se si usa il \_ flag DXGI presente \_ stereo \_ temporaneo \_ mono quando si presenta una catena di scambio stereo che non supporta mono temporaneo, si verifica un errore, la catena di scambio non viene visualizzata e la presentazione restituisce l' [ \_ errore DXGI \_ \_ chiamata non valida](dxgi-error.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
