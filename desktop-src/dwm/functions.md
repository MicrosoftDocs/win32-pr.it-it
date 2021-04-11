---
title: Funzioni DWM
description: In questa sezione vengono fornite informazioni sulle funzioni di Gestione finestre desktop (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), funzioni
- DWM (Gestione finestre desktop), funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339431"
---
# <a name="dwm-functions"></a>Funzioni DWM

In questa sezione vengono fornite informazioni sulle funzioni di Gestione finestre desktop (DWM).

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
<td>Routine della finestra predefinita per l'hit test di DWM nell'area non client.<br/> È anche necessario assicurarsi che <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> venga chiamato per il messaggio di <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> . Se <strong>DwmDefWindowProc</strong> non viene chiamato per il messaggio di <strong>WM_NCMOUSELEAVE</strong> , DWM non rimuove l'evidenziazione dai pulsanti <strong>Ingrandisci</strong>, <strong>Riduci a icona</strong>e <strong>Chiudi</strong> quando il cursore esce dalla finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Questa funzione non è implementata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Abilita l'effetto sfocatura su una finestra specificata.<br/></td>
<b>Nota</b> A partire da Windows 8, la chiamata a questa funzione non comporta un effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering di Windows.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Abilita o Disabilita la composizione di DWM. <br/>
<blockquote>
[!Note]<br />
Questa funzione è deprecata a partire da Windows 8. DWM non può più essere disabilitato a livello di codice.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Invia una notifica a DWM per acconsentire esplicitamente alla pianificazione del servizio di pianificazione classi multimediali (MMCSS) mentre il processo chiamante è attivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Estende la cornice della finestra nell'area client.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Genera una chiamata di scaricamento che blocca il chiamante fino al momento attuale, quando sono stati apportati tutti gli aggiornamenti della superficie Microsoft DirectX attualmente in attesa. Questo compensa le situazioni molto complesse o i processi chiamante con priorità molto bassa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Recupera il colore corrente utilizzato per la composizione di vetro DWM. Questo valore è basato sulla combinazione di colori corrente e può essere modificato dall'utente. Le applicazioni possono restare in ascolto delle modifiche dei colori gestendo la notifica <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Recupera le informazioni sulla tempistica di composizione corrente per una finestra specificata.<br/></td>
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
<td>Recupera gli attributi del trasporto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Nota</strong>  Questa funzione è disponibile pubblicamente, ma non funzionale, per Windows 10, versione 1803.
</blockquote>
Verifica i requisiti necessari per ottenere le schede nella barra del titolo dell'applicazione per la finestra specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Recupera il valore corrente di un attributo specificato applicato a una finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Chiamato da un'applicazione per indicare che tutte le bitmap iconiche fornite in precedenza da una finestra, sia le anteprime che le rappresentazioni di visualizzazione, devono essere aggiornate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Ottiene un valore che indica se la composizione di DWM è abilitata. Le applicazioni nei computer che eseguono Windows 7 o versioni precedenti possono restare in ascolto delle modifiche dello stato di composizione gestendo la notifica <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Modifica il numero di aggiornamenti del monitoraggio tramite i quali verrà visualizzato il frame precedente. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> non è più supportato. A partire da Windows 8.1, le chiamate a <strong>DwmModifyPreviousDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Recupera la dimensione di origine dell'anteprima di DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>Funzionalità DwmRegisterThumbnail</strong></a><br/></td>
<td>Crea una relazione di anteprima DWM tra le finestre di origine e di destinazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Notifica a DWM che un contatto tocco è stato riconosciuto come gesto e che DWM deve creare commenti e suggerimenti per tale gesto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Imposta il numero di aggiornamenti del monitoraggio attraverso i quali visualizzare il frame presentato. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> non è più supportato. A partire da Windows 8.1, le chiamate a <strong>DwmSetDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Imposta una bitmap statica iconica per visualizzare un' <em>anteprima in tempo reale</em> , nota anche come <em>Anteprima</em>di una finestra o di una scheda. La barra delle applicazioni può usare questa bitmap per visualizzare un'anteprima a dimensione intera di una finestra o di una scheda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Imposta una bitmap statica iconica in una finestra o in una scheda da utilizzare come rappresentazione di anteprima. La barra delle applicazioni può usare questa bitmap come destinazione del cambio di anteprima per la finestra o la scheda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Imposta i parametri presenti per la composizione del frame. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> non è più supportato. A partire da Windows 8.1, le chiamate a <strong>DwmSetPresentParameters</strong> restituiscono sempre E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Imposta il valore degli attributi di rendering non client per una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Chiamato da un'applicazione o da un Framework per specificare il tipo di commenti e suggerimenti visivi da creare in risposta a un contatto tocco o penna particolare.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Consente di inviare all'utente Commenti grafici sulle interazioni di tocco e trascinamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Coordina le animazioni delle finestre degli strumenti con DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Rimuove una relazione di anteprima DWM creata dalla funzione <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>funzionalità DwmRegisterThumbnail</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Aggiorna le proprietà per un'anteprima di DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

