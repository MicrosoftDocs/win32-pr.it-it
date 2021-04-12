---
title: Comando MCI_GETDEVCAPS (mmsystem. h)
description: Il \_ comando MCI GETDEVCAPS recupera informazioni statiche su un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Comando MCI_GETDEVCAPS Windows Multimedia
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
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519042"
---
# <a name="mci_getdevcaps-command"></a>\_Comando GETDEVCAPS di MCI

Il \_ comando MCI GETDEVCAPS recupera informazioni statiche su un dispositivo. Tutti i dispositivi riconoscono questo comando. I parametri e i flag disponibili per questo comando dipendono dal dispositivo selezionato. Le informazioni vengono restituite nel membro **dwReturn** della struttura identificata da *lpCapsParms*.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri GETDEVCAPS di MCI**](mci-getdevcaps-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per tutti i dispositivi che supportano MCI GETDEVCAPS sono applicabili i flag aggiuntivi standard e specifici dei comandi seguenti \_ :

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ dispositivo composto GETDEVCAPS \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo utilizza l'archiviazione dei dati che deve essere aperta e chiusa in modo esplicito; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo di \_ dispositivo \_ GETDEVCAPS MCI
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei valori elencati nei [tipi di dispositivo MCI](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>\_GETDEVCAPS MCI \_ con \_ audio
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo ha un output audio. in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>GETDEVCAPS di MCI \_ \_ con \_ video
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se l'output del dispositivo è video; in caso contrario, viene impostato su **false** . Ad esempio, il membro è impostato su **true** per i dispositivi che supportano il set di comandi videodisco.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_elemento GETDEVCAPS di MCI \_
</dt> <dd>

Specifica che il membro **dwItem** della struttura [**\_ GETDEVCAPS \_ parametri di MCI**](mci-getdevcaps-parms.md) contiene una delle costanti seguenti:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>\_GETDEVCAPS MCI \_ possono essere \_ espulsione
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può espellere il supporto. in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>\_GETDEVCAPS MCI \_ può essere \_ riprodotto
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di riprodurre i supporti; in caso contrario, viene impostato su **false**. Se un dispositivo specifica **true**, significa che il dispositivo supporta i comandi [MCI \_ pause](mci-pause.md) e [MCI \_ Stop](mci-stop.md) , oltre al comando [MCI \_ Play](mci-play.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>\_GETDEVCAPS MCI \_ può \_ registrare
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo supporta la registrazione; in caso contrario, viene impostato su **false**. Se un dispositivo specifica **true**, significa che il dispositivo supporta i \_ comandi MCI pause e MCI stop, nonché \_ il comando [MCI \_ record](mci-record.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>\_GETDEVCAPS MCI \_ può \_ salvare
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può salvare un file; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ Usa \_ i file
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo richiede un nome file; in caso contrario, viene impostato su **false** . Solo i dispositivi composti utilizzano i file.

</dd> </dl>

I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Freeze
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di bloccare i frame; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Lock
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può bloccarsi; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ can \_ Reverse
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può essere riprodotto in senso inverso. in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ Str \_ in
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può estendere l'input; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ estendersi
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può allungare un'immagine; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ può \_ testare
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire i test; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>\_GETDEVCAPS DGV di MCI \_ \_ è \_ ancora
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può visualizzare ancora le immagini; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>\_ \_ GETDEVCAPS max DGV \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul numero massimo di finestre che il dispositivo è in grado di gestire simultaneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ frequenza massima GETDEVCAPS DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla velocità di riproduzione massima per il dispositivo, in frame al secondo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_DGV MCI \_ GETDEVCAPS \_ - \_ frequenza minima
</dt> <dd>

Il membro **dwReturn** è impostato sulla velocità di riproduzione minima per il dispositivo, in frame al secondo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ tavolozze GETDEVCAPS DGV MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può restituire un handle della tavolozza; in caso contrario, viene impostato su **false**.

</dd> </dl>

I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **VCR** :

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_frequenza di \_ incremento del clock GETDEVCAPS \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di incrementi al secondo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>\_GETDEVCAPS VCR \_ MCI \_ può \_ rilevare la \_ lunghezza
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di rilevare la lunghezza del supporto; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>il \_ GETDEVCAPS del VCR MCI \_ \_ può \_ bloccarsi
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di bloccare l'immagine di output; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>\_GETDEVCAPS VCR di MCI \_ \_ possono monitorare le \_ \_ origini
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di monitorare le origini; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>\_GETDEVCAPS VCR \_ MCI \_ può essere \_ preroll
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire la preregistrazione; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>GETDEVCAPS VCR di MCI è \_ \_ \_ possibile \_ visualizzare in anteprima
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di visualizzare le anteprime; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>\_GETDEVCAPS VCR \_ MCI \_ possono \_ invertire
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di riprodurre in senso inverso. in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>\_GETDEVCAPS VCR di MCI \_ \_ possono \_ eseguire test
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è in grado di eseguire il test; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>\_GETDEVCAPS VCR \_ MCI \_ con \_ Clock
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo supporta un clock esterno. in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>\_GETDEVCAPS VCR \_ MCI \_ con \_ timecode
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo ha una funzionalità timecode o se questa funzionalità è sconosciuta. in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ \_ numero \_ di \_ CONTRASSEGNi GETDEVCAPS del VCR MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di contrassegni (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_ \_ \_ accuratezza ricerca GETDEVCAPS VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sull'accuratezza della ricerca del dispositivo.

</dd> </dl>

I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ can \_ Freeze
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può bloccare l'immagine; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ può \_ estendersi
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo può allungare l'immagine per riempire il frame; in caso contrario, viene impostato su **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>\_ \_ GETDEVCAPS max OVLY \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul numero massimo di finestre che il dispositivo è in grado di gestire simultaneamente.

</dd> </dl>

I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **videodisco** :

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ può \_ invertire
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il lettore videodisco può riprodurre in ordine inverso. in caso contrario, viene impostato su **false**. Alcuni lettori possono riprodurre dischi CLV in senso inverso, oltre ai dischi CAV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPS \_ CAV
</dt> <dd>

In combinazione con altri elementi, specifica che le informazioni restituite si applicano al formato CAV videodischi. Si tratta dell'impostazione predefinita se non viene inserito alcun videodisco.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

In combinazione con altri elementi, specifica che le informazioni restituite si applicano al formato CLV videodischi.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ frequenza veloce GETDEVCAPS MCI \_ VD
</dt> <dd>

Il membro **dwReturn** è impostato sulla frequenza di riproduzione veloce standard in frame al secondo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ frequenza normale GETDEVCAPS MCI \_ VD
</dt> <dd>

Il membro **dwReturn** è impostato sulla frequenza di riproduzione normale in frame al secondo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ \_ frequenza lenta GETDEVCAPS MCI \_ VD
</dt> <dd>

Il membro **dwReturn** è impostato sulla frequenza di riproduzione lenta standard in frame al secondo.

</dd> </dl>

I flag seguenti possono essere specificati nel membro **dwItem** di [**MCI \_ GETDEVCAPS \_ parametri**](mci-getdevcaps-parms.md) per il tipo di dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ input GETDEVCAPS Wave \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero totale di dispositivi di input della forma d'onda (registrazione).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_ \_ output GETDEVCAPS Wave \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero totale di dispositivi di output della forma d'onda (riproduzione).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

