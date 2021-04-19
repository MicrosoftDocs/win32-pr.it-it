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
# <a name="mci-reference"></a>Riferimento a MCI

Questa sezione elenca le funzioni, le strutture, i messaggi, le macro, i comandi e le stringhe di comando di MCI, documentati in [riferimenti multimediali](multimedia-reference.md). Questi elementi vengono raggruppati come indicato di seguito.

## <a name="notifications"></a>Notifiche

-   [**\_MCINOTIFY mm**](mm-mcinotify.md)
-   [**\_MCISIGNAL mm**](mm-mcisignal.md)

## <a name="getting-information"></a>Recupero informazioni

-   [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))
-   [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))
-   [**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))
-   [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))

## <a name="sending-commands"></a>Invio di comandi

-   [**mciExecute**](/previous-versions//dd757154(v=vs.85))
-   [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
-   [**mciSendString**](/previous-versions//dd757161(v=vs.85))

## <a name="time-formats"></a>Formati di ora

-   [**ora di MCI \_ \_**](mci-hms-hour.md)
-   [**\_minuto dell'ottavo MCI \_**](mci-hms-minute.md)
-   [**\_secondo MCI \_**](mci-hms-second.md)
-   [**MCI \_ make \_ HMS**](mci-make-hms.md)
-   [**MCI \_ make \_ MSF**](mci-make-msf.md)
-   [**MCI \_ make \_ TMSF**](mci-make-tmsf.md)
-   [**\_frame MSF di MCI \_**](/previous-versions//dd743438(v=vs.85))
-   [**\_minuto MSF di MCI \_**](mci-msf-minute.md)
-   [**\_secondo MSF di MCI \_**](mci-msf-second.md)
-   [**\_frame TMSF \_ MCI**](mci-tmsf-frame.md)
-   [**\_TMSF \_ minuto MCI**](mci-tmsf-minute.md)
-   [**\_secondo TMSF \_ MCI**](mci-tmsf-second.md)
-   [**\_traccia TMSF \_ MCI**](mci-tmsf-track.md)

## <a name="yield-procedures"></a>Procedure yield

-   [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))
-   [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))

## <a name="configuring-a-device"></a>Configurazione di un dispositivo

-   [**interruzione**](break.md)
-   [**configurare**](configure.md)
-   [fuga](escape.md)
-   [**Indice**](./windows-multimedia-start-page.md)
-   [**\_interruzioni MCI**](mci-break.md)
-   [**\_parametri break \_ MCI**](mci-break-parms.md)
-   [**configurazione di MCI \_**](mci-configure.md)
-   [**MCI \_ DGV \_ set \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)
-   [**\_parametri DGV \_ di MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)
-   [**parametri DGV di MCI- \_ \_ video \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)
-   [**\_escape MCI**](mci-escape.md)
-   [**\_Indice MCI**](mci-index.md)
-   [**\_ \_ set \_ parametri di MCI Seq**](mci-seq-set-parms.md)
-   [**SET di MCI \_**](mci-set.md)
-   [**\_set \_ parametri di MCI**](mci-set-parms.md)
-   [**sefonica MCI \_**](mci-setaudio.md)
-   [**\_codice temporale MCI**](mci-settimecode.md)
-   [**\_SEtuner MCI**](mci-settuner.md)
-   [**VIDEO su MCI \_**](mci-setvideo.md)
-   [**\_rotazione MCI**](mci-spin.md)
-   [**\_set VCR di MCI \_ \_ parametri**](mci-vcr-set-parms.md)
-   [**parametri di MCI \_ VCR \_ \_**](mci-vcr-setaudio-parms.md)
-   [**\_parametri MCI VCR \_ \_**](mci-vcr-settuner-parms.md)
-   [**\_ \_ video parametri MCI VCR \_**](mci-vcr-setvideo-parms.md)
-   [**\_parametri di \_ escape MCI VD \_**](mci-vd-escape-parms.md)
-   [**\_set di Wave MCI \_ \_ parametri**](mci-wave-set-parms.md)
-   [**set**](set.md)
-   [**SetAudio**](setaudio.md)
-   [**codice temporale**](settimecode.md)
-   [**setuner**](settuner.md)
-   [**video**](setvideo.md)
-   [**selezione**](spin.md)

## <a name="controlling-playback"></a>Controllo della riproduzione

-   [**congelare**](freeze.md)
-   [**carico**](load.md)
-   [**\_ \_ parametri blocco DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)
-   [**\_parametri DGV \_ Load \_ MCI**](/previous-versions//dd743391(v=vs.85))
-   [**\_DGV di \_ sospensione MCI \_ parametri**](/previous-versions//dd743395(v=vs.85))
-   [**\_parametri DGV \_ Play \_ MCI**](/previous-versions//dd743396(v=vs.85))
-   [**\_parametri DGV per MCI \_ Resume \_**](/previous-versions//dd743403(v=vs.85))
-   [**\_DGV MCI \_ \_ parametri stop**](/previous-versions//dd743411(v=vs.85))
-   [**\_blocco MCI**](mci-freeze.md)
-   [**\_carico MCI**](mci-load.md)
-   [**\_parametri Load \_ MCI**](mci-load-parms.md)
-   [**\_parametri OVLY \_ Load \_ MCI**](mci-ovly-load-parms.md)
-   [**\_pausa MCI**](mci-pause.md)
-   [**\_riproduzione MCI**](mci-play.md)
-   [**parametri di MCI \_ Play \_**](mci-play-parms.md)
-   [**\_ripresa MCI**](mci-resume.md)
-   [**\_arresto MCI**](mci-stop.md)
-   [**\_Sblocca MCI**](mci-unfreeze.md)
-   [**\_parametri VCR \_ Play di MCI \_**](mci-vcr-play-parms.md)
-   [**MCI \_ VD \_ Play \_ parametri**](mci-vd-play-parms.md)
-   [**pause**](pause.md)
-   [**Play**](play.md)
-   [**riprendere**](resume.md)
-   [**arrestare**](stop.md)
-   [**Sblocca**](unfreeze.md)

## <a name="controlling-the-position"></a>Controllo della posizione

-   [**segnale**](cue.md)
-   [**contrassegnare**](mark.md)
-   [**\_cue MCI**](mci-cue.md)
-   [**\_ \_ parametri cue DGV di MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)
-   [**\_ \_ parametri segnale DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)
-   [**\_ \_ parametri passaggio DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms)
-   [**\_contrassegno MCI**](mci-mark.md)
-   [**\_ricerca MCI**](mci-seek.md)
-   [**\_parametri di ricerca MCI \_**](mci-seek-parms.md)
-   [**\_segnale MCI**](mci-signal.md)
-   [**\_passaggio MCI**](mci-step.md)
-   [**\_ \_ parametri cue VCR di MCI \_**](mci-vcr-cue-parms.md)
-   [**parametri di MCI \_ VCR \_ Seek \_**](mci-vcr-seek-parms.md)
-   [**\_ \_ passaggio parametri del VCR MCI \_**](mci-vcr-step-parms.md)
-   [**\_ \_ passaggio parametri MCI \_ VD**](mci-vd-step-parms.md)
-   [**cercare**](seek.md)
-   [**signal**](signal.md)
-   [**passo**](step.md)

## <a name="editing"></a>In fase di modifica

-   [**copy**](copy.md)
-   [**tagliare**](cut.md)
-   [**eliminare**](delete.md)
-   [**\_copia MCI**](mci-copy.md)
-   [**\_taglia MCI**](mci-cut.md)
-   [**eliminazione di MCI \_**](mci-delete.md)
-   [**\_parametri DGV \_ Copia \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)
-   [**\_parametri DGV \_ Cut di MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)
-   [**\_parametri DGV \_ Delete \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)
-   [**\_parametri DGV \_ Incolla \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)
-   [**\_Incolla MCI**](mci-paste.md)
-   [**\_annullamento MCI**](mci-undo.md)
-   [**\_parametri di \_ eliminazione dell'onda MCI \_**](mci-wave-delete-parms.md)
-   [**Incolla**](paste.md)
-   [**annullamento**](undo.md)

## <a name="miscellaneous"></a>Varie

-   [**\_parametri generico \_ MCI**](mci-generic-parms.md)

## <a name="opening-and-closing"></a>Apertura e chiusura

-   [**vicino**](close.md)
-   [**\_chiusura MCI**](mci-close.md)
-   [**MCI \_ DGV \_ Open \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)
-   [**\_aperto MCI**](mci-open.md)
-   [**\_parametri aperto \_ MCI**](mci-open-parms.md)
-   [**MCI \_ OVLY \_ Open \_ parametri**](mci-ovly-open-parms.md)
-   [**\_parametri Wave MCI \_ aperto \_**](mci-wave-open-parms.md)
-   [**aprire**](open.md)

## <a name="realizing-a-palette"></a>Realizzazione di una tavolozza

-   [**realizzazione di MCI \_**](mci-realize.md)
-   [**tenere presente**](realize.md)

## <a name="repainting-a-frame"></a>Ridisegnare un frame

-   [**\_ \_ aggiornamento \_ parametri di MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)
-   [**aggiornamento di MCI \_**](mci-update.md)
-   [**aggiornamento**](update.md)

## <a name="retrieving-information"></a>Recupero di informazioni

-   [**funzionalità**](capability.md)
-   [**informazioni**](info.md)
-   [**list**](list.md)
-   [**\_parametri DGV \_ info \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)
-   [**\_ \_ parametri elenco DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)
-   [**\_ \_ parametri stato DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)
-   [**\_GETDEVCAPS MCI**](mci-getdevcaps.md)
-   [**\_parametri GETDEVCAPS \_ MCI**](mci-getdevcaps-parms.md)
-   [**\_informazioni MCI**](mci-info.md)
-   [**\_parametri info \_ MCI**](mci-info-parms.md)
-   [**\_elenco MCI**](mci-list.md)
-   [**\_stato MCI**](mci-status.md)
-   [**\_parametri stato \_ MCI**](mci-status-parms.md)
-   [**\_sysinfo MCI**](mci-sysinfo.md)
-   [**parametri di MCI \_ sysinfo \_**](mci-sysinfo-parms.md)
-   [**\_ \_ parametri elenco VCR \_ MCI**](mci-vcr-list-parms.md)
-   [**\_ \_ parametri stato VCR \_ MCI**](mci-vcr-status-parms.md)
-   [**stato**](status.md)
-   [sysinfo](sysinfo.md)

## <a name="saving"></a>Saving

-   [**\_ \_ parametri record DGV \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)
-   [**\_parametri DGV per il \_ salvataggio di MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)
-   [**\_parametri OVLY per il \_ salvataggio di MCI \_**](/previous-versions//dd743447(v=vs.85))
-   [**\_record MCI**](mci-record.md)
-   [**\_record MCI \_ parametri**](mci-record-parms.md)
-   [**salvataggio di MCI \_**](mci-save.md)
-   [**\_Salva \_ parametri di MCI**](mci-save-parms.md)
-   [**\_record VCR \_ MCI \_ parametri**](mci-vcr-record-parms.md)
-   [**record**](record.md)
-   [**salvare**](save.md)

## <a name="video-control"></a>Controllo video

-   [**catturare**](capture.md)
-   [**acquisizione di MCI \_**](mci-capture.md)
-   [**\_ \_ parametri monitoraggio MCI \_ DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)
-   [**MCI \_ DGV \_ Quality \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)
-   [**\_ \_ parametri Reserve DGV di MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)
-   [**\_parametri DGV \_ RESTOre MCI \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)
-   [**\_monitoraggio MCI**](mci-monitor.md)
-   [**\_qualità MCI**](mci-quality.md)
-   [**\_riserva MCI**](mci-reserve.md)
-   [**ripristino di MCI \_**](mci-restore.md)
-   [**monitoraggio**](monitor.md)
-   [**qualità**](quality.md)
-   [**riserva**](reserve.md)
-   [**ripristino**](restore.md)

## <a name="window-or-display-rectangles"></a>Rettangoli di finestra o di visualizzazione

-   [**\_parametri DGV \_ put di MCI \_**](/previous-versions//dd743397(v=vs.85))
-   [**MCI \_ DGV \_ Rect \_ parametri**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)
-   [**\_parametri DGV \_ finestra \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)
-   [**MCI \_ OVLY \_ Rect \_ parametri**](mci-ovly-rect-parms.md)
-   [**\_parametri OVLY \_ finestra \_ MCI**](mci-ovly-window-parms.md)
-   [**\_put MCI**](mci-put.md)
-   [**MCI \_ dove**](mci-where.md)
-   [**\_finestra MCI**](mci-window.md)
-   [**mettere**](put.md)
-   [**dove**](where.md)
-   [**finestra**](window.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MCI](mci.md)
</dt> </dl>

 

 