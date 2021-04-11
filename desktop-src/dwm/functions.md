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
# <a name="dwm-functions"></a><span data-ttu-id="01711-107">Funzioni DWM</span><span class="sxs-lookup"><span data-stu-id="01711-107">DWM Functions</span></span>

<span data-ttu-id="01711-108">In questa sezione vengono fornite informazioni sulle funzioni di Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="01711-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01711-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="01711-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01711-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="01711-110">Topic</span></span></th>
<th><span data-ttu-id="01711-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01711-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01711-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-113">Questa funzione non è implementata.</span><span class="sxs-lookup"><span data-stu-id="01711-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-115">Routine della finestra predefinita per l'hit test di DWM nell'area non client.</span><span class="sxs-lookup"><span data-stu-id="01711-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="01711-116">È anche necessario assicurarsi che <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> venga chiamato per il messaggio di <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01711-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="01711-117">Se <strong>DwmDefWindowProc</strong> non viene chiamato per il messaggio di <strong>WM_NCMOUSELEAVE</strong> , DWM non rimuove l'evidenziazione dai pulsanti <strong>Ingrandisci</strong>, <strong>Riduci a icona</strong>e <strong>Chiudi</strong> quando il cursore esce dalla finestra.</span><span class="sxs-lookup"><span data-stu-id="01711-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-119">Questa funzione non è implementata.</span><span class="sxs-lookup"><span data-stu-id="01711-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-121">Abilita l'effetto sfocatura su una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="01711-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="01711-122">
<b>Nota</b> A partire da Windows 8, la chiamata a questa funzione non comporta un effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering di Windows.</span><span class="sxs-lookup"><span data-stu-id="01711-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-124">Abilita o Disabilita la composizione di DWM.</span><span class="sxs-lookup"><span data-stu-id="01711-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="01711-125">Questa funzione è deprecata a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01711-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="01711-126">DWM non può più essere disabilitato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="01711-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-128">Invia una notifica a DWM per acconsentire esplicitamente alla pianificazione del servizio di pianificazione classi multimediali (MMCSS) mentre il processo chiamante è attivo.</span><span class="sxs-lookup"><span data-stu-id="01711-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-130">Estende la cornice della finestra nell'area client.</span><span class="sxs-lookup"><span data-stu-id="01711-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-132">Genera una chiamata di scaricamento che blocca il chiamante fino al momento attuale, quando sono stati apportati tutti gli aggiornamenti della superficie Microsoft DirectX attualmente in attesa.</span><span class="sxs-lookup"><span data-stu-id="01711-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="01711-133">Questo compensa le situazioni molto complesse o i processi chiamante con priorità molto bassa.</span><span class="sxs-lookup"><span data-stu-id="01711-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-135">Recupera il colore corrente utilizzato per la composizione di vetro DWM.</span><span class="sxs-lookup"><span data-stu-id="01711-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="01711-136">Questo valore è basato sulla combinazione di colori corrente e può essere modificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="01711-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="01711-137">Le applicazioni possono restare in ascolto delle modifiche dei colori gestendo la notifica <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01711-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-139">Recupera le informazioni sulla tempistica di composizione corrente per una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="01711-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-141">Questa funzione non è implementata.</span><span class="sxs-lookup"><span data-stu-id="01711-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-143">Questa funzione non è implementata.</span><span class="sxs-lookup"><span data-stu-id="01711-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-145">Recupera gli attributi del trasporto.</span><span class="sxs-lookup"><span data-stu-id="01711-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="01711-147">
<strong>Nota</strong>  Questa funzione è disponibile pubblicamente, ma non funzionale, per Windows 10, versione 1803.</span><span class="sxs-lookup"><span data-stu-id="01711-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="01711-148">Verifica i requisiti necessari per ottenere le schede nella barra del titolo dell'applicazione per la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="01711-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-150">Recupera il valore corrente di un attributo specificato applicato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="01711-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-152">Chiamato da un'applicazione per indicare che tutte le bitmap iconiche fornite in precedenza da una finestra, sia le anteprime che le rappresentazioni di visualizzazione, devono essere aggiornate.</span><span class="sxs-lookup"><span data-stu-id="01711-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-154">Ottiene un valore che indica se la composizione di DWM è abilitata.</span><span class="sxs-lookup"><span data-stu-id="01711-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="01711-155">Le applicazioni nei computer che eseguono Windows 7 o versioni precedenti possono restare in ascolto delle modifiche dello stato di composizione gestendo la notifica <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01711-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-157">Modifica il numero di aggiornamenti del monitoraggio tramite i quali verrà visualizzato il frame precedente.</span><span class="sxs-lookup"><span data-stu-id="01711-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="01711-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="01711-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="01711-159">A partire da Windows 8.1, le chiamate a <strong>DwmModifyPreviousDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="01711-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-161">Recupera la dimensione di origine dell'anteprima di DWM.</span><span class="sxs-lookup"><span data-stu-id="01711-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>Funzionalità DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-163">Crea una relazione di anteprima DWM tra le finestre di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01711-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-165">Notifica a DWM che un contatto tocco è stato riconosciuto come gesto e che DWM deve creare commenti e suggerimenti per tale gesto.</span><span class="sxs-lookup"><span data-stu-id="01711-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-167">Imposta il numero di aggiornamenti del monitoraggio attraverso i quali visualizzare il frame presentato.</span><span class="sxs-lookup"><span data-stu-id="01711-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="01711-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="01711-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="01711-169">A partire da Windows 8.1, le chiamate a <strong>DwmSetDxFrameDuration</strong> restituiscono sempre E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="01711-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-171">Imposta una bitmap statica iconica per visualizzare un' <em>anteprima in tempo reale</em> , nota anche come <em>Anteprima</em>di una finestra o di una scheda. La barra delle applicazioni può usare questa bitmap per visualizzare un'anteprima a dimensione intera di una finestra o di una scheda.</span><span class="sxs-lookup"><span data-stu-id="01711-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-173">Imposta una bitmap statica iconica in una finestra o in una scheda da utilizzare come rappresentazione di anteprima.</span><span class="sxs-lookup"><span data-stu-id="01711-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="01711-174">La barra delle applicazioni può usare questa bitmap come destinazione del cambio di anteprima per la finestra o la scheda.</span><span class="sxs-lookup"><span data-stu-id="01711-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-176">Imposta i parametri presenti per la composizione del frame.</span><span class="sxs-lookup"><span data-stu-id="01711-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="01711-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="01711-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="01711-178">A partire da Windows 8.1, le chiamate a <strong>DwmSetPresentParameters</strong> restituiscono sempre E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="01711-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-180">Imposta il valore degli attributi di rendering non client per una finestra.</span><span class="sxs-lookup"><span data-stu-id="01711-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-182">Chiamato da un'applicazione o da un Framework per specificare il tipo di commenti e suggerimenti visivi da creare in risposta a un contatto tocco o penna particolare.</span><span class="sxs-lookup"><span data-stu-id="01711-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-184">Consente di inviare all'utente Commenti grafici sulle interazioni di tocco e trascinamento.</span><span class="sxs-lookup"><span data-stu-id="01711-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-186">Coordina le animazioni delle finestre degli strumenti con DWM.</span><span class="sxs-lookup"><span data-stu-id="01711-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01711-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-188">Rimuove una relazione di anteprima DWM creata dalla funzione <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>funzionalità DwmRegisterThumbnail</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01711-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01711-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="01711-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="01711-190">Aggiorna le proprietà per un'anteprima di DWM.</span><span class="sxs-lookup"><span data-stu-id="01711-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

