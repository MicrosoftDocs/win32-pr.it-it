---
description: Le costanti DXGI \_ PRESENT specificano le opzioni per la presentazione di fotogrammi nell'output.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84ce79d686aebd77e24a5be6facccd6fa4abd48e10bf15c07729a8ff6a0397bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796605"
---
# <a name="dxgi_present"></a>DXGI \_ PRESENT

Le **costanti DXGI \_ PRESENT** specificano le opzioni per la presentazione di fotogrammi nell'output.



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
<td style="text-align: left;">Presentare un frame da ogni buffer (a partire dal buffer corrente) all'output.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Presentare un frame dal buffer corrente all'output. Usare questo flag in modo che la presentazione possa usare la sincronizzazione verticale vuota anziché sequenziare i buffer nella catena nel modo consueto.<br/>
<blockquote>
[!Note]<br />
Se l'applicazione chiamante imposta la costante DXGI_PRESENT_DO_NOT_SEQUENCE alla prima operazione presente, ovvero quando non è presente alcun buffer corrente, il runtime ignora l'operazione corrente e non chiama il driver.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Non presentare il frame nell'output. Lo stato della catena di scambio verrà testato e verranno restituiti gli errori appropriati. DXGI_PRESENT_TEST è destinato all'uso solo quando si passa dallo stato di inattività; non usarlo per determinare quando passare allo stato di inattività perché in questo modo la catena di scambio non può uscire dalla modalità schermo intero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Specifica che il runtime scarterà i file in attesa in coda.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Specifica che il runtime avrà esito negativo per la presentazione ,ovvero non riuscirà una chiamata a <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) con il codice di errore <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> se il thread chiamante è bloccato. il runtime restituisce DXGI_ERROR_WAS_STILL_DRAWING anziché la sospensione fino a quando la dipendenza non viene risolta.<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Indica che il contenuto della presentazione verrà visualizzato solo nell'output specifico. Il contenuto non sarà visibile in altri output. Ad esempio, se l'utente tenta di spostare il contenuto video in un altro output, il contenuto video non sarà visibile. <br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8. <br/>
<blockquote>
[!Note]<br />
Questo flag deve essere usato solo con l'effetto <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">swap DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> o DXGI_SWAP_EFFECT_FLIP_DISCARD. L'uso di questo flag <em>con altri</em> effetti di scambio è deprecato e potrebbe non funzionare nelle versioni future di Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Indica che se la presentazione stereo deve essere ridotta a mono, viene usata la visualizzazione dell'occhio destro anziché quella a sinistra.<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Indica che la presentazione deve usare il buffer sinistro come buffer mono. Un'applicazione chiama il <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>metodo IDXGISwapChain1::IsTemporaryMonoSupported</strong></a> per determinare se una catena di scambio supporta &quot; mono &quot; temporaneo.<br/> <strong>Direct3D 11:</strong> Questo valore di enumerazione è supportato a partire da Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Questo flag deve essere impostato dalle app multimediali che attualmente usano una durata attuale personalizzata (frequenza di aggiornamento personalizzata). Vedere <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Questo valore è supportato a partire da Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Consentire lo tearing è un requisito di visualizzazione della frequenza di aggiornamento variabile.<br/> Le condizioni per l'DXGI_PRESENT_ALLOW_TEARING durante Present sono le seguenti:<br/>
<ul>
<li>La catena di scambio deve essere creata con il flag <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> di scambio.</li>
<li>L'intervallo di sincronizzazione passato <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>a Present</strong></a> <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>(o Present1)</strong></a>deve essere 0.</li>
<li>Il flag DXGI_PRESENT_ALLOW_TEARING non può essere usato in un'applicazione attualmente in modalità esclusiva a schermo intero (impostata chiamando <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState(TRUE)</strong></a>). Può essere usato solo in modalità finestra. Per usare questo flag nelle app Win32 a schermo intero, l'applicazione deve essere presente in una finestra senza bordo a schermo intero e disabilitare la commutazione automatica ALT+INVIO a schermo intero tramite <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory::MakeWindowAssociation</strong></a>. Le app UWP che entrano in modalità schermo intero chiamando sono finestre senza bordo a schermo intero e <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> possono usare il flag .</li>
</ul>
Se <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>si chiama Present</strong></a> <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>(o Present1)</strong></a>con questo flag e non vengono soddisfatte le condizioni precedenti, verrà restituito un DXGI_ERROR_INVALID_CALL errore all'applicazione chiamante.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Le opzioni di presentazione vengono fornite durante la chiamata [**IDXGISwapChain::P resent**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) o [**IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) I buffer vengono specificati nella descrizione della catena di scambio (vedere [**DXGI \_ SWAP \_ CHAIN \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI \_ SWAP CHAIN \_ \_ DESC1).**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)

DXGI PRESENT RESTART è valido solo per catene di scambio di modelli flip \_ \_ e schermo intero. Le applicazioni possono usare DXGI PRESENT RESTART per eseguire il ripristino da problemi di riproduzione, nonché per eliminare le \_ \_ presentazioni in coda in precedenza. L'eliminazione di presentazioni in coda in precedenza è utile se tali presentazioni in coda sono scenari a finestre. In particolare, la presentazione in coda in precedenza potrebbe aver presupposto che la finestra abbia dimensioni precedenti, ovvero che si sia verificata un'operazione di ridimensionamento dopo l'invio.

DXGI PRESENT RESTRICT TO OUTPUT è valido solo per le catene di scambio che hanno specificato un output specifico per limitare il contenuto al momento della creazione di tali catene di scambio \_ \_ ( \_ \_ [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Se non è presente alcun output a cui limitare l'accesso, il flag non è valido.

DXGI PRESENT STEREO PREFER RIGHT indica che se il presente stereo deve essere ridotto a mono, è necessario usare l'occhio destro anziché \_ \_ \_ \_ l'occhio sinistro (predefinito). È possibile usare questo flag se un lato è di qualità superiore, ad esempio se la coppia stereo viene sintetizzata da un'immagine standard.

DXGI PRESENT STEREO TEMPORARY MONO indica che il \_ presente deve usare il buffer sinistro come buffer \_ \_ \_ mono. È possibile usare questo flag per evitare di aggiornare il buffer giusto quando un'applicazione temporaneamente non ha contenuto stereo. È consigliabile usare questo flag quando possibile perché consente un'ottimizzazione significativa da parte del sistema operativo e in alcuni casi può evitare artefatti di modifica della modalità visibile.

È consigliabile usare il flag DXGI PRESENT STEREO TEMPORARY MONO in preferenza per passare a una catena di scambio mono per la maggior parte delle applicazioni che si prevede useranno \_ \_ nuovamente \_ \_ stereo. È necessario bilanciare l'uso di questo flag nelle applicazioni con esecuzione estremamente lunga o che raramente visualizzano stereo rispetto allo svantaggio della memoria inutilizzata.

> [!Note]  
> Le applicazioni a schermo intero che passano a una catena di scambio mono causano una modifica della modalità che in genere ha elementi visibili (ad esempio, "flashing"). È tuttavia possibile che mono temporaneo non sia supportato per le catene di scambio a schermo intero.

 

I flag DXGI \_ PRESENT STEREO PREFER RIGHT e \_ \_ \_ DXGI \_ PRESENT STEREO TEMPORARY MONO si applicano solo alle catene di scambio \_ \_ \_ stereo. Se vengono usate quando si presentano catene di scambio mono, si verifica un'operazione non valida.

Se si usa il flag DXGI PRESENT STEREO TEMPORARY MONO quando si presenta una catena di scambio stereo che non supporta mono temporaneo, si verifica un errore, la catena di scambio non viene visualizzata e la presentazione restituisce \_ \_ \_ \_ [DXGI \_ ERROR \_ INVALID \_ CALL](dxgi-error.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
