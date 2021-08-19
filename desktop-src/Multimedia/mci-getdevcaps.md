---
title: MCI_GETDEVCAPS comando (Mmsystem.h)
description: Il comando MCI \_ GETDEVCAPS recupera informazioni statiche su un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7798f72405209f9834c3b67f84e57508c58ffc6153bce860b91f089005648905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803953"
---
# <a name="mci_getdevcaps-command"></a>Comando MCI \_ GETDEVCAPS

Il comando MCI \_ GETDEVCAPS recupera informazioni statiche su un dispositivo. Tutti i dispositivi riconoscono questo comando. I parametri e i flag disponibili per questo comando dipendono dal dispositivo selezionato. Le informazioni vengono restituite **nel membro dwReturn** della struttura identificata da *lpCapsParms*.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT o, per i dispositivi video digitale e \_ VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GETDEVCAPS \_ PARMS.**](mci-getdevcaps-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag standard e specifici dei comandi seguenti si applicano a tutti i dispositivi che supportano MCI \_ GETDEVCAPS:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ GETDEVCAPS \_ COMPOUND \_ DEVICE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo usa l'archiviazione dei dati che deve essere aperta e chiusa in modo esplicito. In caso contrario, è **impostato su FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>TIPO DI \_ DISPOSITIVO MCI GETDEVCAPS \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su uno dei valori elencati in [McI Device Types](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ HA \_ AUDIO
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo ha output audio; In caso contrario, è **impostato su FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ HA UN \_ VIDEO
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo ha output video; In caso contrario, è **impostato su FALSE.** Ad esempio, il membro è impostato su **TRUE per** i dispositivi che supportano il set di comandi videodisc.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ GETDEVCAPS \_ ITEM
</dt> <dd>

Specifica che il **membro dwItem** della struttura [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) contiene una delle costanti seguenti:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ PUÒ ESSERE \_ ESPULSO
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo può estrarre il supporto. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ PUÒ \_ RIPRODURRE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo può riprodurre il contenuto multimediale. in caso contrario, è impostato su **FALSE.** Se un dispositivo specifica **TRUE,** implica che il dispositivo supporta i comandi [MCI \_ PAUSE](mci-pause.md) e [MCI \_ STOP,](mci-stop.md) nonché il [comando MCI \_ PLAY.](mci-play.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ PUÒ \_ REGISTRARE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo supporta la registrazione. in caso contrario, è impostato su **FALSE.** Se un dispositivo specifica **TRUE,** implica che il dispositivo supporta i comandi MCI PAUSE e MCI STOP, nonché il \_ \_ comando [MCI \_ RECORD.](mci-record.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ PUÒ \_ SALVARE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo può salvare un file. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ USA I \_ FILE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo richiede un nome file. In caso contrario, è **impostato su FALSE.** Solo i dispositivi composti usano file.

</dd> </dl>

I flag seguenti possono essere specificati nel **membro dwItem** di [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) per il tipo di **dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ \_ BLOCCARSI
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può bloccare i fotogrammi. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ \_ BLOCCARE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può bloccarsi; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ INVERTIRE \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può essere riprodotto in ordine inverso. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ \_ STR \_ IN
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può estendere l'input; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ ESSERE \_ ESTESA
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può estendere un'immagine; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUÒ \_ TESTARE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può eseguire test. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ HA \_ ANCORA
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può visualizzare immagini fisse; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

Il **membro dwReturn** è impostato sul numero massimo di finestre che il dispositivo può gestire contemporaneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAXIMUM \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione massima per il dispositivo, in fotogrammi al secondo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ MINIMUM \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione minima per il dispositivo, in fotogrammi al secondo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>TAVOLOZZE \_ MCI DGV \_ GETDEVCAPS \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può restituire un handle della tavolozza; in caso contrario, è impostato su **FALSE.**

</dd> </dl>

I flag seguenti possono essere specificati nel **membro dwItem** di [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) per il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ GETDEVCAPS \_ CLOCK \_ INCREMENT \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di incrementi al secondo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ \_ RILEVARE LA \_ LUNGHEZZA
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di rilevare la lunghezza del supporto; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ \_ BLOCCARSI
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo è in grado di bloccare l'immagine di output. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ MONITORARE LE \_ \_ ORIGINI
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di monitorare le origini. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ ESEGUIRE LA \_ PRE-REGISTRAZIONE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di eseguire la preroll; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ VISUALIZZARE IN \_ ANTEPRIMA
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di eseguire anteprime. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ INVERTIRE \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di riprodurre in ordine inverso. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUÒ \_ TESTARE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è in grado di eseguire il test; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>IL VCR MCI \_ \_ GETDEVCAPS \_ HA \_ L'OROLOGIO
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo supporta un orologio esterno. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>IL VCR MCI \_ \_ GETDEVCAPS \_ HA \_ TIMECODE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo ha funzionalità di timecode o se questa funzionalità è sconosciuta. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ GETDEVCAPS \_ NUMBER \_ OF \_ MARKS
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di contrassegni (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ GETDEVCAPS \_ SEEK \_ ACCURACY
</dt> <dd>

Il **membro dwReturn** è impostato sull'accuratezza della ricerca del dispositivo.

</dd> </dl>

I flag seguenti possono essere specificati nel **membro dwItem** di [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) per il tipo **di dispositivo di** sovrimpressione:

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ PUÒ \_ BLOCCARSI
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può bloccare l'immagine. in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ PUÒ \_ ESTENDERSI
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il dispositivo può estendere l'immagine per riempire il frame; in caso contrario, è impostato su **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

Il **membro dwReturn** è impostato sul numero massimo di finestre che il dispositivo può gestire contemporaneamente.

</dd> </dl>

I flag seguenti possono essere specificati nel **membro dwItem** di [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) per il tipo **di dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ PUÒ INVERTIRE \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** il lettore videodisc può essere riprodotto in ordine inverso. in caso contrario, è impostato su **FALSE.** Alcuni lettori possono riprodurre dischi CLV in ordine inverso e dischi CAV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV
</dt> <dd>

In combinazione con altri elementi, specifica che le informazioni restituite si applicano ai videodisc in formato CAV. Questa è l'impostazione predefinita se non viene inserito alcun elemento videodisc.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

In combinazione con altri elementi, specifica che le informazioni restituite si applicano ai videodisc in formato CLV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione veloce standard in fotogrammi al secondo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ NORMAL \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione normale in fotogrammi al secondo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ SLOW \_ RATE
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione lenta standard in fotogrammi al secondo.

</dd> </dl>

I flag seguenti possono essere specificati nel **membro dwItem** di [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) per il **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>INPUT \_ \_ GETDEVCAPS DI MCI WAVE \_
</dt> <dd>

Il **membro dwReturn** è impostato sul numero totale di dispositivi di input waveform (registrazione).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>OUTPUT DI MCI \_ WAVE \_ GETDEVCAPS \_
</dt> <dd>

Il **membro dwReturn** è impostato sul numero totale di dispositivi di output della forma d'onda (riproduzione).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

