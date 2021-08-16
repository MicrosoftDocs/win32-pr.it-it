---
title: Funzioni DWM
description: Questa sezione contiene informazioni sulle funzioni Gestione finestre desktop (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gestione finestre desktop (DWM), informazioni di riferimento
- DWM (Gestione finestre desktop),informazioni di riferimento
- Gestione finestre desktop (DWM), funzioni
- DWM (Gestione finestre desktop),funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8c1db28571fde16cf0fe0f9068f5bd650d31f637776c7bcc00717ab3043997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503306"
---
# <a name="dwm-functions"></a>Funzioni DWM

Questa sezione contiene informazioni sulle funzioni Gestione finestre desktop (DWM).

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br/></td>
<td>Questa funzione non è implementata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Procedura della finestra predefinita per l'hit testing DWM all'interno dell'area non client.<br/> È anche necessario assicurarsi che <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> sia chiamato per il <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> messaggio. Se <strong>DwmDefWindowProc</strong> non viene chiamato per il messaggio <strong>WM_NCMOUSELEAVE,</strong> DWM non rimuove <strong></strong>l'evidenziazione dai pulsanti Ingrandisci <strong>,</strong>Riduci a icona e Chiudi quando il cursore esce dalla finestra. <strong></strong><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Questa funzione non è implementata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Abilita l'effetto sfocatura su una finestra specificata.<br/></td>
<b>Nota</b> A partire Windows 8, la chiamata a questa funzione non comporta l'effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering delle finestre.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Abilita o disabilita la composizione DWM. <br/>
<blockquote>
[!Note]<br />
Questa funzione è deprecata a Windows 8. DWM non può più essere disabilitato a livello di codice.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Notifica al DWM di acconsentire esplicitamente o meno alla pianificazione di MmcSS (Multimedia Class Schedule Service) mentre il processo chiamante è attivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Estende la cornice della finestra nell'area client.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Esegue una chiamata di scaricamento che blocca il chiamante fino al momento successivo, quando sono stati evasi tutti gli aggiornamenti della superficie di Microsoft DirectX attualmente in sospeso. Ciò compensa scene molto complesse o processi chiamanti con priorità molto bassa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Recupera il colore corrente utilizzato per la composizione del cristallo DWM. Questo valore è basato sulla combinazione colori corrente e può essere modificato dall'utente. Le applicazioni possono restare in ascolto delle modifiche di colore gestendo <a href="wm-dwmcolorizationcolorchanged.md"><strong>la WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notifica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Recupera le informazioni sull'intervallo di composizione corrente per una finestra specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>Questa funzione non è implementata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>Questa funzione non è implementata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>Recupera gli attributi di trasporto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Nota</strong>  Questa funzione è disponibile pubblicamente, ma non funzionante, Windows 10 versione 1803.
</blockquote>
Controlla i requisiti necessari per ottenere le schede nella barra del titolo dell'applicazione per la finestra specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Recupera il valore corrente di un attributo specificato applicato a una finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Chiamato da un'applicazione per indicare che tutte le bitmap in miniatura fornite in precedenza da una finestra, sia anteprime che rappresentazioni di anteprima, devono essere aggiornate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Ottiene un valore che indica se la composizione DWM è abilitata. Le applicazioni nei computer che eseguono Windows 7 o versioni precedenti possono restare in ascolto delle modifiche dello stato di composizione gestendo la <a href="wm-dwmcompositionchanged.md"><strong>notifica WM_DWMCOMPOSITIONCHANGED</strong></a> composizione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Modifica il numero di aggiornamenti del monitoraggio attraverso i quali verrà visualizzato il frame precedente. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> non è più supportato. A partire Windows 8.1, le chiamate a <strong>DwmModifyPreviousDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Recupera le dimensioni di origine dell'anteprima DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Crea una relazione di anteprima DWM tra le finestre di destinazione e di origine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Notifica a DWM che un contatto tocco è stato riconosciuto come movimento e che DWM deve inviare commenti e suggerimenti per tale movimento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Imposta il numero di aggiornamenti del monitoraggio tramite i quali visualizzare il frame presentato. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> non è più supportato. A partire Windows 8.1, le chiamate a <strong>DwmSetDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Imposta una bitmap statica e bitmap per visualizzare <em>un'anteprima</em> live (nota anche come anteprima <em>di</em>anteprima) di una finestra o di una scheda. La barra delle applicazioni può usare questa bitmap per visualizzare un'anteprima a dimensione intera di una finestra o di una scheda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Imposta una bitmap statica in una finestra o una scheda da usare come rappresentazione di anteprima. La barra delle applicazioni può usare questa bitmap come destinazione del cambio di anteprima per la finestra o la scheda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Imposta i parametri presenti per la composizione dei fotogrammi. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> non è più supportato. A partire Windows 8.1, le chiamate a <strong>DwmSetPresentParameters</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Imposta il valore degli attributi di rendering non client per una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Chiamato da un'app o un framework per specificare il tipo di feedback visivo da disegnare in risposta a un particolare contatto tocco o penna.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Abilita il feedback grafico delle interazioni tramite tocco e trascinamento per l'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Coordina le animazioni delle finestre degli strumenti con DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Rimuove una relazione di anteprima DWM creata dalla <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>funzione DwmRegisterThumbnail.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Aggiorna le proprietà per un'anteprima DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

