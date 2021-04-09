---
title: Informazioni di riferimento sull'acquisizione video
description: Informazioni di riferimento sull'acquisizione video
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video per Windows (VFW), Guida di riferimento all'acquisizione video
- VFW (video per Windows), Guida di riferimento all'acquisizione video
- AVICap, riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044312"
---
# <a name="video-capture-reference"></a><span data-ttu-id="d8cc3-106">Informazioni di riferimento sull'acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8cc3-106">Video Capture Reference</span></span>

<span data-ttu-id="d8cc3-107">In questa sezione vengono descritte le funzioni, le strutture, i messaggi e le macro associati alla classe della finestra AVICap.</span><span class="sxs-lookup"><span data-stu-id="d8cc3-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="d8cc3-108">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d8cc3-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="d8cc3-109">Operazioni di acquisizione di base</span><span class="sxs-lookup"><span data-stu-id="d8cc3-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="d8cc3-110">**capCreateCaptureWindow**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="d8cc3-111">**interruzione di WM \_ Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="d8cc3-112">**\_ \_ connessione driver WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="d8cc3-113">**\_sequenza Cap \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="d8cc3-114">**arresto di WM \_ Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="d8cc3-115">Acquisisci Windows</span><span class="sxs-lookup"><span data-stu-id="d8cc3-115">Capture Windows</span></span>

-   [<span data-ttu-id="d8cc3-116">**CAPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="d8cc3-117">**capGetDriverDescription**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="d8cc3-118">**\_ \_ connessione driver WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="d8cc3-119">**\_disconnessione \_ driver WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="d8cc3-120">**\_stato di \_ get \_ Cap WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="d8cc3-121">Driver di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d8cc3-121">Capture Drivers</span></span>

-   [<span data-ttu-id="d8cc3-122">**CAPDRIVERCAPS**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="d8cc3-123">**\_ \_ \_ Caps Get driver \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="d8cc3-124">**\_ \_ \_ nome Get driver WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="d8cc3-125">**\_versione del \_ driver WM Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="d8cc3-126">**WM \_ Cap \_ get \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="d8cc3-127">**WM \_ Cap \_ get \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="d8cc3-128">**\_set di estremità WM \_ \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="d8cc3-129">**\_set di estremità WM \_ \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="d8cc3-130">Modalità anteprima e sovrapposizione driver di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d8cc3-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="d8cc3-131">**\_ \_ sovrimpressione set Cap WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="d8cc3-132">**\_ \_ Anteprima set WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="d8cc3-133">**\_set di estremità WM \_ \_ PREVIEWRATE**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="d8cc3-134">**\_scala del \_ set di estremità WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="d8cc3-135">**\_scorrimento del \_ set di estremità WM \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="d8cc3-136">Finestre di dialogo di acquisizione del video del driver</span><span class="sxs-lookup"><span data-stu-id="d8cc3-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="d8cc3-137">**VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="d8cc3-138">**VIDEODISPLAY di WM \_ Cap \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="d8cc3-139">**VIDEOFORMAT di WM \_ Cap \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="d8cc3-140">**VIDEOSOURCE di WM \_ Cap \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="d8cc3-141">Formato audio</span><span class="sxs-lookup"><span data-stu-id="d8cc3-141">Audio Format</span></span>

-   [<span data-ttu-id="d8cc3-142">**WM \_ Cap \_ get \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="d8cc3-143">**\_set di estremità WM \_ \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="d8cc3-144">Impostazioni acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8cc3-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="d8cc3-145">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="d8cc3-146">**\_configurazione della sequenza WM Cap \_ get \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="d8cc3-147">**\_configurazione della \_ sequenza di set \_ \_ di WM Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="d8cc3-148">Acquisisci file e buffer</span><span class="sxs-lookup"><span data-stu-id="d8cc3-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="d8cc3-149">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="d8cc3-150">**\_ \_ ALLOCA file WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="d8cc3-151">**file \_ di \_ \_ acquisizione Get \_ file \_ di WM Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="d8cc3-152">**\_ \_ SaveAs file di WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="d8cc3-153">**\_file di \_ acquisizione del set di file WM Cap \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="d8cc3-154">Usando direttamente i dati di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d8cc3-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="d8cc3-155">**\_sequenza Cap \_ WM \_ nofile**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="d8cc3-156">Acquisisci dal dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="d8cc3-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="d8cc3-157">**SET di WM \_ Cap \_ set \_ MCI \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="d8cc3-158">Acquisizione frame manuale</span><span class="sxs-lookup"><span data-stu-id="d8cc3-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="d8cc3-159">**\_ \_ singolo frame WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="d8cc3-160">**\_ \_ \_ chiusura singolo frame \_ WM Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="d8cc3-161">**\_apertura del \_ singolo \_ frame WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="d8cc3-162">Acquisizione di Still-Image</span><span class="sxs-lookup"><span data-stu-id="d8cc3-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="d8cc3-163">**copia di modifica di WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="d8cc3-164">**\_ \_ SAVEDIB file WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="d8cc3-165">**\_frame di \_ cattura WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="d8cc3-166">**\_NOSTOP \_ frame di cattura WM Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="d8cc3-167">Opzioni di acquisizione avanzate</span><span class="sxs-lookup"><span data-stu-id="d8cc3-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="d8cc3-168">**\_set di \_ file WM Cap \_ \_ INFOCHUNK**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="d8cc3-169">**WM \_ Cap \_ ottenere \_ \_ i dati utente**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="d8cc3-170">**\_set di \_ \_ dati utente \_ di WM Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="d8cc3-171">Utilizzo delle tavolozze</span><span class="sxs-lookup"><span data-stu-id="d8cc3-171">Working with Palettes</span></span>

-   [<span data-ttu-id="d8cc3-172">**copia di modifica di WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="d8cc3-173">**CREAZIONE di un PAL di WM \_ Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="d8cc3-174">**WM \_ Cap \_ PAL \_ MANUALCREATE**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="d8cc3-175">**PAL di WM \_ Cap \_ \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="d8cc3-176">**di WM \_ Cap \_ PAL \_ Incolla**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="d8cc3-177">**\_ \_ salvataggio PAL WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="d8cc3-178">Cedendo ad altre applicazioni</span><span class="sxs-lookup"><span data-stu-id="d8cc3-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="d8cc3-179">**\_configurazione della sequenza WM Cap \_ get \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="d8cc3-180">**\_rendimento di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="d8cc3-181">**\_configurazione della \_ sequenza di set \_ \_ di WM Cap**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="d8cc3-182">Funzioni di callback AVICap</span><span class="sxs-lookup"><span data-stu-id="d8cc3-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="d8cc3-183">**capControlCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="d8cc3-184">**capErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="d8cc3-185">**capStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="d8cc3-186">**capVideoStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="d8cc3-187">**capWaveStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="d8cc3-188">**capYieldCallback**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="d8cc3-189">**\_CAPCONTROL di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="d8cc3-190">**\_errore di \_ callback del set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="d8cc3-191">**\_frame di \_ \_ callback \_ per set di estremità WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="d8cc3-192">**\_stato di \_ callback per set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="d8cc3-193">**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="d8cc3-194">**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="d8cc3-195">**\_rendimento di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d8cc3-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="d8cc3-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8cc3-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8cc3-197">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8cc3-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




