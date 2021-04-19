---
title: Riferimento a MCI
description: Riferimento a MCI
ms.assetid: e7cedfc2-ce01-481c-a431-c93c97d45baf
keywords:
- Riferimento a MCI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cc54f69e714960d189567e759cf4b254275807
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322015"
---
# <a name="mci-reference"></a><span data-ttu-id="420ca-104">Riferimento a MCI</span><span class="sxs-lookup"><span data-stu-id="420ca-104">MCI Reference</span></span>

<span data-ttu-id="420ca-105">Questa sezione elenca le funzioni, le strutture, i messaggi, le macro, i comandi e le stringhe di comando di MCI, documentati in [riferimenti multimediali](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="420ca-105">This section lists the MCI functions, structures, messages, macros, commands, and command strings, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="420ca-106">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="420ca-106">These elements are grouped as follows.</span></span>

## <a name="notifications"></a><span data-ttu-id="420ca-107">Notifiche</span><span class="sxs-lookup"><span data-stu-id="420ca-107">Notifications</span></span>

-   [<span data-ttu-id="420ca-108">**\_MCINOTIFY mm**</span><span class="sxs-lookup"><span data-stu-id="420ca-108">**MM\_MCINOTIFY**</span></span>](mm-mcinotify.md)
-   [<span data-ttu-id="420ca-109">**\_MCISIGNAL mm**</span><span class="sxs-lookup"><span data-stu-id="420ca-109">**MM\_MCISIGNAL**</span></span>](mm-mcisignal.md)

## <a name="getting-information"></a><span data-ttu-id="420ca-110">Recupero informazioni</span><span class="sxs-lookup"><span data-stu-id="420ca-110">Getting Information</span></span>

-   <span data-ttu-id="420ca-111">[**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-111">[**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-112">[**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-112">[**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-113">[**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-113">[**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-114">[**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-114">[**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))</span></span>

## <a name="sending-commands"></a><span data-ttu-id="420ca-115">Invio di comandi</span><span class="sxs-lookup"><span data-stu-id="420ca-115">Sending Commands</span></span>

-   <span data-ttu-id="420ca-116">[**mciExecute**](/previous-versions//dd757154(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-116">[**mciExecute**](/previous-versions//dd757154(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-117">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-117">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>

## <a name="time-formats"></a><span data-ttu-id="420ca-119">Formati di ora</span><span class="sxs-lookup"><span data-stu-id="420ca-119">Time Formats</span></span>

-   [<span data-ttu-id="420ca-120">**ora di MCI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-120">**MCI\_HMS\_HOUR**</span></span>](mci-hms-hour.md)
-   [<span data-ttu-id="420ca-121">**\_minuto dell'ottavo MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-121">**MCI\_HMS\_MINUTE**</span></span>](mci-hms-minute.md)
-   [<span data-ttu-id="420ca-122">**\_secondo MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-122">**MCI\_HMS\_SECOND**</span></span>](mci-hms-second.md)
-   [<span data-ttu-id="420ca-123">**MCI \_ make \_ HMS**</span><span class="sxs-lookup"><span data-stu-id="420ca-123">**MCI\_MAKE\_HMS**</span></span>](mci-make-hms.md)
-   [<span data-ttu-id="420ca-124">**MCI \_ make \_ MSF**</span><span class="sxs-lookup"><span data-stu-id="420ca-124">**MCI\_MAKE\_MSF**</span></span>](mci-make-msf.md)
-   [<span data-ttu-id="420ca-125">**MCI \_ make \_ TMSF**</span><span class="sxs-lookup"><span data-stu-id="420ca-125">**MCI\_MAKE\_TMSF**</span></span>](mci-make-tmsf.md)
-   <span data-ttu-id="420ca-126">[**\_frame MSF di MCI \_**](/previous-versions//dd743438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-126">[**MCI\_MSF\_FRAME**](/previous-versions//dd743438(v=vs.85))</span></span>
-   [<span data-ttu-id="420ca-127">**\_minuto MSF di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-127">**MCI\_MSF\_MINUTE**</span></span>](mci-msf-minute.md)
-   [<span data-ttu-id="420ca-128">**\_secondo MSF di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-128">**MCI\_MSF\_SECOND**</span></span>](mci-msf-second.md)
-   [<span data-ttu-id="420ca-129">**\_frame TMSF \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-129">**MCI\_TMSF\_FRAME**</span></span>](mci-tmsf-frame.md)
-   [<span data-ttu-id="420ca-130">**\_TMSF \_ minuto MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-130">**MCI\_TMSF\_MINUTE**</span></span>](mci-tmsf-minute.md)
-   [<span data-ttu-id="420ca-131">**\_secondo TMSF \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-131">**MCI\_TMSF\_SECOND**</span></span>](mci-tmsf-second.md)
-   [<span data-ttu-id="420ca-132">**\_traccia TMSF \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-132">**MCI\_TMSF\_TRACK**</span></span>](mci-tmsf-track.md)

## <a name="yield-procedures"></a><span data-ttu-id="420ca-133">Procedure yield</span><span class="sxs-lookup"><span data-stu-id="420ca-133">Yield Procedures</span></span>

-   <span data-ttu-id="420ca-134">[**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-134">[**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-135">[**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-135">[**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))</span></span>

## <a name="configuring-a-device"></a><span data-ttu-id="420ca-136">Configurazione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="420ca-136">Configuring a Device</span></span>

-   [<span data-ttu-id="420ca-137">**interruzione**</span><span class="sxs-lookup"><span data-stu-id="420ca-137">**break**</span></span>](break.md)
-   [<span data-ttu-id="420ca-138">**configurare**</span><span class="sxs-lookup"><span data-stu-id="420ca-138">**configure**</span></span>](configure.md)
-   [<span data-ttu-id="420ca-139">fuga</span><span class="sxs-lookup"><span data-stu-id="420ca-139">escape</span></span>](escape.md)
-   [<span data-ttu-id="420ca-140">**Indice**</span><span class="sxs-lookup"><span data-stu-id="420ca-140">**index**</span></span>](./windows-multimedia-start-page.md)
-   [<span data-ttu-id="420ca-141">**\_interruzioni MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-141">**MCI\_BREAK**</span></span>](mci-break.md)
-   [<span data-ttu-id="420ca-142">**\_parametri break \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-142">**MCI\_BREAK\_PARMS**</span></span>](mci-break-parms.md)
-   [<span data-ttu-id="420ca-143">**configurazione di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-143">**MCI\_CONFIGURE**</span></span>](mci-configure.md)
-   [<span data-ttu-id="420ca-144">**MCI \_ DGV \_ set \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-144">**MCI\_DGV\_SET\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)
-   [<span data-ttu-id="420ca-145">**\_parametri DGV \_ di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-145">**MCI\_DGV\_SETAUDIO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)
-   [<span data-ttu-id="420ca-146">**parametri DGV di MCI- \_ \_ video \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-146">**MCI\_DGV\_SETVIDEO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)
-   [<span data-ttu-id="420ca-147">**\_escape MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-147">**MCI\_ESCAPE**</span></span>](mci-escape.md)
-   [<span data-ttu-id="420ca-148">**\_Indice MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-148">**MCI\_INDEX**</span></span>](mci-index.md)
-   [<span data-ttu-id="420ca-149">**\_ \_ set \_ parametri di MCI Seq**</span><span class="sxs-lookup"><span data-stu-id="420ca-149">**MCI\_SEQ\_SET\_PARMS**</span></span>](mci-seq-set-parms.md)
-   [<span data-ttu-id="420ca-150">**SET di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-150">**MCI\_SET**</span></span>](mci-set.md)
-   [<span data-ttu-id="420ca-151">**\_set \_ parametri di MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-151">**MCI\_SET\_PARMS**</span></span>](mci-set-parms.md)
-   [<span data-ttu-id="420ca-152">**sefonica MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-152">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
-   [<span data-ttu-id="420ca-153">**\_codice temporale MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-153">**MCI\_SETTIMECODE**</span></span>](mci-settimecode.md)
-   [<span data-ttu-id="420ca-154">**\_SEtuner MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-154">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
-   [<span data-ttu-id="420ca-155">**VIDEO su MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-155">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
-   [<span data-ttu-id="420ca-156">**\_rotazione MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-156">**MCI\_SPIN**</span></span>](mci-spin.md)
-   [<span data-ttu-id="420ca-157">**\_set VCR di MCI \_ \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-157">**MCI\_VCR\_SET\_PARMS**</span></span>](mci-vcr-set-parms.md)
-   [<span data-ttu-id="420ca-158">**parametri di MCI \_ VCR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-158">**MCI\_VCR\_SETAUDIO\_PARMS**</span></span>](mci-vcr-setaudio-parms.md)
-   [<span data-ttu-id="420ca-159">**\_parametri MCI VCR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-159">**MCI\_VCR\_SETTUNER\_PARMS**</span></span>](mci-vcr-settuner-parms.md)
-   [<span data-ttu-id="420ca-160">**\_ \_ video parametri MCI VCR \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-160">**MCI\_VCR\_SETVIDEO\_PARMS**</span></span>](mci-vcr-setvideo-parms.md)
-   [<span data-ttu-id="420ca-161">**\_parametri di \_ escape MCI VD \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-161">**MCI\_VD\_ESCAPE\_PARMS**</span></span>](mci-vd-escape-parms.md)
-   [<span data-ttu-id="420ca-162">**\_set di Wave MCI \_ \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-162">**MCI\_WAVE\_SET\_PARMS**</span></span>](mci-wave-set-parms.md)
-   [<span data-ttu-id="420ca-163">**set**</span><span class="sxs-lookup"><span data-stu-id="420ca-163">**set**</span></span>](set.md)
-   [<span data-ttu-id="420ca-164">**SetAudio**</span><span class="sxs-lookup"><span data-stu-id="420ca-164">**setaudio**</span></span>](setaudio.md)
-   [<span data-ttu-id="420ca-165">**codice temporale**</span><span class="sxs-lookup"><span data-stu-id="420ca-165">**settimecode**</span></span>](settimecode.md)
-   [<span data-ttu-id="420ca-166">**setuner**</span><span class="sxs-lookup"><span data-stu-id="420ca-166">**settuner**</span></span>](settuner.md)
-   [<span data-ttu-id="420ca-167">**video**</span><span class="sxs-lookup"><span data-stu-id="420ca-167">**setvideo**</span></span>](setvideo.md)
-   [<span data-ttu-id="420ca-168">**selezione**</span><span class="sxs-lookup"><span data-stu-id="420ca-168">**spin**</span></span>](spin.md)

## <a name="controlling-playback"></a><span data-ttu-id="420ca-169">Controllo della riproduzione</span><span class="sxs-lookup"><span data-stu-id="420ca-169">Controlling Playback</span></span>

-   [<span data-ttu-id="420ca-170">**congelare**</span><span class="sxs-lookup"><span data-stu-id="420ca-170">**freeze**</span></span>](freeze.md)
-   [<span data-ttu-id="420ca-171">**carico**</span><span class="sxs-lookup"><span data-stu-id="420ca-171">**load**</span></span>](load.md)
-   [<span data-ttu-id="420ca-172">**\_ \_ parametri blocco DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-172">**MCI\_DGV\_FREEZE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)
-   <span data-ttu-id="420ca-173">[**\_parametri DGV \_ Load \_ MCI**](/previous-versions//dd743391(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-173">[**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-174">[**\_DGV di \_ sospensione MCI \_ parametri**](/previous-versions//dd743395(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-174">[**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-175">[**\_parametri DGV \_ Play \_ MCI**](/previous-versions//dd743396(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-175">[**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-176">[**\_parametri DGV per MCI \_ Resume \_**](/previous-versions//dd743403(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-176">[**MCI\_DGV\_RESUME\_PARMS**](/previous-versions//dd743403(v=vs.85))</span></span>
-   <span data-ttu-id="420ca-177">[**\_DGV MCI \_ \_ parametri stop**](/previous-versions//dd743411(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-177">[**MCI\_DGV\_STOP\_PARMS**](/previous-versions//dd743411(v=vs.85))</span></span>
-   [<span data-ttu-id="420ca-178">**\_blocco MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-178">**MCI\_FREEZE**</span></span>](mci-freeze.md)
-   [<span data-ttu-id="420ca-179">**\_carico MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-179">**MCI\_LOAD**</span></span>](mci-load.md)
-   [<span data-ttu-id="420ca-180">**\_parametri Load \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-180">**MCI\_LOAD\_PARMS**</span></span>](mci-load-parms.md)
-   [<span data-ttu-id="420ca-181">**\_parametri OVLY \_ Load \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-181">**MCI\_OVLY\_LOAD\_PARMS**</span></span>](mci-ovly-load-parms.md)
-   [<span data-ttu-id="420ca-182">**\_pausa MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-182">**MCI\_PAUSE**</span></span>](mci-pause.md)
-   [<span data-ttu-id="420ca-183">**\_riproduzione MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-183">**MCI\_PLAY**</span></span>](mci-play.md)
-   [<span data-ttu-id="420ca-184">**parametri di MCI \_ Play \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-184">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
-   [<span data-ttu-id="420ca-185">**\_ripresa MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-185">**MCI\_RESUME**</span></span>](mci-resume.md)
-   [<span data-ttu-id="420ca-186">**\_arresto MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-186">**MCI\_STOP**</span></span>](mci-stop.md)
-   [<span data-ttu-id="420ca-187">**\_Sblocca MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-187">**MCI\_UNFREEZE**</span></span>](mci-unfreeze.md)
-   [<span data-ttu-id="420ca-188">**\_parametri VCR \_ Play di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-188">**MCI\_VCR\_PLAY\_PARMS**</span></span>](mci-vcr-play-parms.md)
-   [<span data-ttu-id="420ca-189">**MCI \_ VD \_ Play \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-189">**MCI\_VD\_PLAY\_PARMS**</span></span>](mci-vd-play-parms.md)
-   [<span data-ttu-id="420ca-190">**pause**</span><span class="sxs-lookup"><span data-stu-id="420ca-190">**pause**</span></span>](pause.md)
-   [<span data-ttu-id="420ca-191">**Play**</span><span class="sxs-lookup"><span data-stu-id="420ca-191">**play**</span></span>](play.md)
-   [<span data-ttu-id="420ca-192">**riprendere**</span><span class="sxs-lookup"><span data-stu-id="420ca-192">**resume**</span></span>](resume.md)
-   [<span data-ttu-id="420ca-193">**arrestare**</span><span class="sxs-lookup"><span data-stu-id="420ca-193">**stop**</span></span>](stop.md)
-   [<span data-ttu-id="420ca-194">**Sblocca**</span><span class="sxs-lookup"><span data-stu-id="420ca-194">**unfreeze**</span></span>](unfreeze.md)

## <a name="controlling-the-position"></a><span data-ttu-id="420ca-195">Controllo della posizione</span><span class="sxs-lookup"><span data-stu-id="420ca-195">Controlling the Position</span></span>

-   [<span data-ttu-id="420ca-196">**segnale**</span><span class="sxs-lookup"><span data-stu-id="420ca-196">**cue**</span></span>](cue.md)
-   [<span data-ttu-id="420ca-197">**contrassegnare**</span><span class="sxs-lookup"><span data-stu-id="420ca-197">**mark**</span></span>](mark.md)
-   [<span data-ttu-id="420ca-198">**\_cue MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-198">**MCI\_CUE**</span></span>](mci-cue.md)
-   [<span data-ttu-id="420ca-199">**\_ \_ parametri cue DGV di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-199">**MCI\_DGV\_CUE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)
-   [<span data-ttu-id="420ca-200">**\_ \_ parametri segnale DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-200">**MCI\_DGV\_SIGNAL\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)
-   [<span data-ttu-id="420ca-201">**\_ \_ parametri passaggio DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-201">**MCI\_DGV\_STEP\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms)
-   [<span data-ttu-id="420ca-202">**\_contrassegno MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-202">**MCI\_MARK**</span></span>](mci-mark.md)
-   [<span data-ttu-id="420ca-203">**\_ricerca MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-203">**MCI\_SEEK**</span></span>](mci-seek.md)
-   [<span data-ttu-id="420ca-204">**\_parametri di ricerca MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-204">**MCI\_SEEK\_PARMS**</span></span>](mci-seek-parms.md)
-   [<span data-ttu-id="420ca-205">**\_segnale MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-205">**MCI\_SIGNAL**</span></span>](mci-signal.md)
-   [<span data-ttu-id="420ca-206">**\_passaggio MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-206">**MCI\_STEP**</span></span>](mci-step.md)
-   [<span data-ttu-id="420ca-207">**\_ \_ parametri cue VCR di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-207">**MCI\_VCR\_CUE\_PARMS**</span></span>](mci-vcr-cue-parms.md)
-   [<span data-ttu-id="420ca-208">**parametri di MCI \_ VCR \_ Seek \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-208">**MCI\_VCR\_SEEK\_PARMS**</span></span>](mci-vcr-seek-parms.md)
-   [<span data-ttu-id="420ca-209">**\_ \_ passaggio parametri del VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-209">**MCI\_VCR\_STEP\_PARMS**</span></span>](mci-vcr-step-parms.md)
-   [<span data-ttu-id="420ca-210">**\_ \_ passaggio parametri MCI \_ VD**</span><span class="sxs-lookup"><span data-stu-id="420ca-210">**MCI\_VD\_STEP\_PARMS**</span></span>](mci-vd-step-parms.md)
-   [<span data-ttu-id="420ca-211">**cercare**</span><span class="sxs-lookup"><span data-stu-id="420ca-211">**seek**</span></span>](seek.md)
-   [<span data-ttu-id="420ca-212">**signal**</span><span class="sxs-lookup"><span data-stu-id="420ca-212">**signal**</span></span>](signal.md)
-   [<span data-ttu-id="420ca-213">**passo**</span><span class="sxs-lookup"><span data-stu-id="420ca-213">**step**</span></span>](step.md)

## <a name="editing"></a><span data-ttu-id="420ca-214">In fase di modifica</span><span class="sxs-lookup"><span data-stu-id="420ca-214">Editing</span></span>

-   [<span data-ttu-id="420ca-215">**copy**</span><span class="sxs-lookup"><span data-stu-id="420ca-215">**copy**</span></span>](copy.md)
-   [<span data-ttu-id="420ca-216">**tagliare**</span><span class="sxs-lookup"><span data-stu-id="420ca-216">**cut**</span></span>](cut.md)
-   [<span data-ttu-id="420ca-217">**eliminare**</span><span class="sxs-lookup"><span data-stu-id="420ca-217">**delete**</span></span>](delete.md)
-   [<span data-ttu-id="420ca-218">**\_copia MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-218">**MCI\_COPY**</span></span>](mci-copy.md)
-   [<span data-ttu-id="420ca-219">**\_taglia MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-219">**MCI\_CUT**</span></span>](mci-cut.md)
-   [<span data-ttu-id="420ca-220">**eliminazione di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-220">**MCI\_DELETE**</span></span>](mci-delete.md)
-   [<span data-ttu-id="420ca-221">**\_parametri DGV \_ Copia \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-221">**MCI\_DGV\_COPY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)
-   [<span data-ttu-id="420ca-222">**\_parametri DGV \_ Cut di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-222">**MCI\_DGV\_CUT\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)
-   [<span data-ttu-id="420ca-223">**\_parametri DGV \_ Delete \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-223">**MCI\_DGV\_DELETE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)
-   [<span data-ttu-id="420ca-224">**\_parametri DGV \_ Incolla \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-224">**MCI\_DGV\_PASTE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)
-   [<span data-ttu-id="420ca-225">**\_Incolla MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-225">**MCI\_PASTE**</span></span>](mci-paste.md)
-   [<span data-ttu-id="420ca-226">**\_annullamento MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-226">**MCI\_UNDO**</span></span>](mci-undo.md)
-   [<span data-ttu-id="420ca-227">**\_parametri di \_ eliminazione dell'onda MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-227">**MCI\_WAVE\_DELETE\_PARMS**</span></span>](mci-wave-delete-parms.md)
-   [<span data-ttu-id="420ca-228">**Incolla**</span><span class="sxs-lookup"><span data-stu-id="420ca-228">**paste**</span></span>](paste.md)
-   [<span data-ttu-id="420ca-229">**annullamento**</span><span class="sxs-lookup"><span data-stu-id="420ca-229">**undo**</span></span>](undo.md)

## <a name="miscellaneous"></a><span data-ttu-id="420ca-230">Varie</span><span class="sxs-lookup"><span data-stu-id="420ca-230">Miscellaneous</span></span>

-   [<span data-ttu-id="420ca-231">**\_parametri generico \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-231">**MCI\_GENERIC\_PARMS**</span></span>](mci-generic-parms.md)

## <a name="opening-and-closing"></a><span data-ttu-id="420ca-232">Apertura e chiusura</span><span class="sxs-lookup"><span data-stu-id="420ca-232">Opening and Closing</span></span>

-   [<span data-ttu-id="420ca-233">**vicino**</span><span class="sxs-lookup"><span data-stu-id="420ca-233">**close**</span></span>](close.md)
-   [<span data-ttu-id="420ca-234">**\_chiusura MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-234">**MCI\_CLOSE**</span></span>](mci-close.md)
-   [<span data-ttu-id="420ca-235">**MCI \_ DGV \_ Open \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-235">**MCI\_DGV\_OPEN\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)
-   [<span data-ttu-id="420ca-236">**\_aperto MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-236">**MCI\_OPEN**</span></span>](mci-open.md)
-   [<span data-ttu-id="420ca-237">**\_parametri aperto \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-237">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
-   [<span data-ttu-id="420ca-238">**MCI \_ OVLY \_ Open \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-238">**MCI\_OVLY\_OPEN\_PARMS**</span></span>](mci-ovly-open-parms.md)
-   [<span data-ttu-id="420ca-239">**\_parametri Wave MCI \_ aperto \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-239">**MCI\_WAVE\_OPEN\_PARMS**</span></span>](mci-wave-open-parms.md)
-   [<span data-ttu-id="420ca-240">**aprire**</span><span class="sxs-lookup"><span data-stu-id="420ca-240">**open**</span></span>](open.md)

## <a name="realizing-a-palette"></a><span data-ttu-id="420ca-241">Realizzazione di una tavolozza</span><span class="sxs-lookup"><span data-stu-id="420ca-241">Realizing a Palette</span></span>

-   [<span data-ttu-id="420ca-242">**realizzazione di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-242">**MCI\_REALIZE**</span></span>](mci-realize.md)
-   [<span data-ttu-id="420ca-243">**tenere presente**</span><span class="sxs-lookup"><span data-stu-id="420ca-243">**realize**</span></span>](realize.md)

## <a name="repainting-a-frame"></a><span data-ttu-id="420ca-244">Ridisegnare un frame</span><span class="sxs-lookup"><span data-stu-id="420ca-244">Repainting a Frame</span></span>

-   [<span data-ttu-id="420ca-245">**\_ \_ aggiornamento \_ parametri di MCI DGV**</span><span class="sxs-lookup"><span data-stu-id="420ca-245">**MCI\_DGV\_UPDATE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)
-   [<span data-ttu-id="420ca-246">**aggiornamento di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-246">**MCI\_UPDATE**</span></span>](mci-update.md)
-   [<span data-ttu-id="420ca-247">**aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="420ca-247">**update**</span></span>](update.md)

## <a name="retrieving-information"></a><span data-ttu-id="420ca-248">Recupero di informazioni</span><span class="sxs-lookup"><span data-stu-id="420ca-248">Retrieving Information</span></span>

-   [<span data-ttu-id="420ca-249">**funzionalità**</span><span class="sxs-lookup"><span data-stu-id="420ca-249">**capability**</span></span>](capability.md)
-   [<span data-ttu-id="420ca-250">**informazioni**</span><span class="sxs-lookup"><span data-stu-id="420ca-250">**info**</span></span>](info.md)
-   [<span data-ttu-id="420ca-251">**list**</span><span class="sxs-lookup"><span data-stu-id="420ca-251">**list**</span></span>](list.md)
-   [<span data-ttu-id="420ca-252">**\_parametri DGV \_ info \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-252">**MCI\_DGV\_INFO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)
-   [<span data-ttu-id="420ca-253">**\_ \_ parametri elenco DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-253">**MCI\_DGV\_LIST\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)
-   [<span data-ttu-id="420ca-254">**\_ \_ parametri stato DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-254">**MCI\_DGV\_STATUS\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)
-   [<span data-ttu-id="420ca-255">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-255">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
-   [<span data-ttu-id="420ca-256">**\_parametri GETDEVCAPS \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-256">**MCI\_GETDEVCAPS\_PARMS**</span></span>](mci-getdevcaps-parms.md)
-   [<span data-ttu-id="420ca-257">**\_informazioni MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-257">**MCI\_INFO**</span></span>](mci-info.md)
-   [<span data-ttu-id="420ca-258">**\_parametri info \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-258">**MCI\_INFO\_PARMS**</span></span>](mci-info-parms.md)
-   [<span data-ttu-id="420ca-259">**\_elenco MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-259">**MCI\_LIST**</span></span>](mci-list.md)
-   [<span data-ttu-id="420ca-260">**\_stato MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-260">**MCI\_STATUS**</span></span>](mci-status.md)
-   [<span data-ttu-id="420ca-261">**\_parametri stato \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-261">**MCI\_STATUS\_PARMS**</span></span>](mci-status-parms.md)
-   [<span data-ttu-id="420ca-262">**\_sysinfo MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-262">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
-   [<span data-ttu-id="420ca-263">**parametri di MCI \_ sysinfo \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-263">**MCI\_SYSINFO\_PARMS**</span></span>](mci-sysinfo-parms.md)
-   [<span data-ttu-id="420ca-264">**\_ \_ parametri elenco VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-264">**MCI\_VCR\_LIST\_PARMS**</span></span>](mci-vcr-list-parms.md)
-   [<span data-ttu-id="420ca-265">**\_ \_ parametri stato VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-265">**MCI\_VCR\_STATUS\_PARMS**</span></span>](mci-vcr-status-parms.md)
-   [<span data-ttu-id="420ca-266">**stato**</span><span class="sxs-lookup"><span data-stu-id="420ca-266">**status**</span></span>](status.md)
-   [<span data-ttu-id="420ca-267">sysinfo</span><span class="sxs-lookup"><span data-stu-id="420ca-267">sysinfo</span></span>](sysinfo.md)

## <a name="saving"></a><span data-ttu-id="420ca-268">Saving</span><span class="sxs-lookup"><span data-stu-id="420ca-268">Saving</span></span>

-   [<span data-ttu-id="420ca-269">**\_ \_ parametri record DGV \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-269">**MCI\_DGV\_RECORD\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)
-   [<span data-ttu-id="420ca-270">**\_parametri DGV per il \_ salvataggio di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-270">**MCI\_DGV\_SAVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)
-   <span data-ttu-id="420ca-271">[**\_parametri OVLY per il \_ salvataggio di MCI \_**](/previous-versions//dd743447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-271">[**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85))</span></span>
-   [<span data-ttu-id="420ca-272">**\_record MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-272">**MCI\_RECORD**</span></span>](mci-record.md)
-   [<span data-ttu-id="420ca-273">**\_record MCI \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-273">**MCI\_RECORD\_PARMS**</span></span>](mci-record-parms.md)
-   [<span data-ttu-id="420ca-274">**salvataggio di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-274">**MCI\_SAVE**</span></span>](mci-save.md)
-   [<span data-ttu-id="420ca-275">**\_Salva \_ parametri di MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-275">**MCI\_SAVE\_PARMS**</span></span>](mci-save-parms.md)
-   [<span data-ttu-id="420ca-276">**\_record VCR \_ MCI \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-276">**MCI\_VCR\_RECORD\_PARMS**</span></span>](mci-vcr-record-parms.md)
-   [<span data-ttu-id="420ca-277">**record**</span><span class="sxs-lookup"><span data-stu-id="420ca-277">**record**</span></span>](record.md)
-   [<span data-ttu-id="420ca-278">**salvare**</span><span class="sxs-lookup"><span data-stu-id="420ca-278">**save**</span></span>](save.md)

## <a name="video-control"></a><span data-ttu-id="420ca-279">Controllo video</span><span class="sxs-lookup"><span data-stu-id="420ca-279">Video Control</span></span>

-   [<span data-ttu-id="420ca-280">**catturare**</span><span class="sxs-lookup"><span data-stu-id="420ca-280">**capture**</span></span>](capture.md)
-   [<span data-ttu-id="420ca-281">**acquisizione di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-281">**MCI\_CAPTURE**</span></span>](mci-capture.md)
-   [<span data-ttu-id="420ca-282">**\_ \_ parametri monitoraggio MCI \_ DGV**</span><span class="sxs-lookup"><span data-stu-id="420ca-282">**MCI\_DGV\_MONITOR\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)
-   [<span data-ttu-id="420ca-283">**MCI \_ DGV \_ Quality \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-283">**MCI\_DGV\_QUALITY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)
-   [<span data-ttu-id="420ca-284">**\_ \_ parametri Reserve DGV di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-284">**MCI\_DGV\_RESERVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)
-   [<span data-ttu-id="420ca-285">**\_parametri DGV \_ RESTOre MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-285">**MCI\_DGV\_RESTORE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)
-   [<span data-ttu-id="420ca-286">**\_monitoraggio MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-286">**MCI\_MONITOR**</span></span>](mci-monitor.md)
-   [<span data-ttu-id="420ca-287">**\_qualità MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-287">**MCI\_QUALITY**</span></span>](mci-quality.md)
-   [<span data-ttu-id="420ca-288">**\_riserva MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-288">**MCI\_RESERVE**</span></span>](mci-reserve.md)
-   [<span data-ttu-id="420ca-289">**ripristino di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="420ca-289">**MCI\_RESTORE**</span></span>](mci-restore.md)
-   [<span data-ttu-id="420ca-290">**monitoraggio**</span><span class="sxs-lookup"><span data-stu-id="420ca-290">**monitor**</span></span>](monitor.md)
-   [<span data-ttu-id="420ca-291">**qualità**</span><span class="sxs-lookup"><span data-stu-id="420ca-291">**quality**</span></span>](quality.md)
-   [<span data-ttu-id="420ca-292">**riserva**</span><span class="sxs-lookup"><span data-stu-id="420ca-292">**reserve**</span></span>](reserve.md)
-   [<span data-ttu-id="420ca-293">**ripristino**</span><span class="sxs-lookup"><span data-stu-id="420ca-293">**restore**</span></span>](restore.md)

## <a name="window-or-display-rectangles"></a><span data-ttu-id="420ca-294">Rettangoli di finestra o di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="420ca-294">Window or Display Rectangles</span></span>

-   <span data-ttu-id="420ca-295">[**\_parametri DGV \_ put di MCI \_**](/previous-versions//dd743397(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="420ca-295">[**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85))</span></span>
-   [<span data-ttu-id="420ca-296">**MCI \_ DGV \_ Rect \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-296">**MCI\_DGV\_RECT\_PARMS**</span></span>](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)
-   [<span data-ttu-id="420ca-297">**\_parametri DGV \_ finestra \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-297">**MCI\_DGV\_WINDOW\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)
-   [<span data-ttu-id="420ca-298">**MCI \_ OVLY \_ Rect \_ parametri**</span><span class="sxs-lookup"><span data-stu-id="420ca-298">**MCI\_OVLY\_RECT\_PARMS**</span></span>](mci-ovly-rect-parms.md)
-   [<span data-ttu-id="420ca-299">**\_parametri OVLY \_ finestra \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-299">**MCI\_OVLY\_WINDOW\_PARMS**</span></span>](mci-ovly-window-parms.md)
-   [<span data-ttu-id="420ca-300">**\_put MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-300">**MCI\_PUT**</span></span>](mci-put.md)
-   [<span data-ttu-id="420ca-301">**MCI \_ dove**</span><span class="sxs-lookup"><span data-stu-id="420ca-301">**MCI\_WHERE**</span></span>](mci-where.md)
-   [<span data-ttu-id="420ca-302">**\_finestra MCI**</span><span class="sxs-lookup"><span data-stu-id="420ca-302">**MCI\_WINDOW**</span></span>](mci-window.md)
-   [<span data-ttu-id="420ca-303">**mettere**</span><span class="sxs-lookup"><span data-stu-id="420ca-303">**put**</span></span>](put.md)
-   [<span data-ttu-id="420ca-304">**dove**</span><span class="sxs-lookup"><span data-stu-id="420ca-304">**where**</span></span>](where.md)
-   [<span data-ttu-id="420ca-305">**finestra**</span><span class="sxs-lookup"><span data-stu-id="420ca-305">**window**</span></span>](window.md)

## <a name="related-topics"></a><span data-ttu-id="420ca-306">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="420ca-306">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="420ca-307">MCI</span><span class="sxs-lookup"><span data-stu-id="420ca-307">MCI</span></span>](mci.md)
</dt> </dl>

 

 