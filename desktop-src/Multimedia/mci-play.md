---
title: Comando MCI_PLAY (mmsystem. h)
description: Il \_ comando MCI Play segnala al dispositivo di iniziare a trasmettere i dati di output. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Comando MCI_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874633"
---
# <a name="mci_play-command"></a>\_Comando MCI Play

Il \_ comando MCI Play segnala al dispositivo di iniziare a trasmettere i dati di output. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri di MCI Play**](mci-play-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ Play:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da
</dt> <dd>

Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpPlay*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) . Se MCI \_ from non è specificato, per impostazione predefinita la posizione iniziale viene impostata sulla posizione corrente.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpPlay*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ . Se MCI \_ to non è specificato, il valore predefinito della posizione finale è la fine del supporto.

</dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_ripetizione della \_ riproduzione \_ DGV MCI
</dt> <dd>

La riproduzione deve iniziare di nuovo all'inizio quando viene raggiunta la fine del contenuto.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>\_riesecuzione DGV MCI \_ \_
</dt> <dd>

La riproduzione deve essere eseguita in ordine inverso.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>\_finestra di \_ riproduzione \_ MCIAVI MCI
</dt> <dd>

La riproduzione deve essere eseguita nella finestra associata a un'istanza del dispositivo (impostazione predefinita). Questo flag è specifico di MCIAVI. DRV.)

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>\_MCIAVI MCI \_ Play a \_ schermo intero
</dt> <dd>

La riproduzione deve usare una visualizzazione a schermo intero. Utilizzare questo flag solo per la riproduzione di file compressi o a 8 bit.

</dd> </dl>

Per i dispositivi digitali video, *lpPlay* punta a una [**struttura \_ DGV \_ Play \_ parametri di MCI**](/previous-versions//dd743396(v=vs.85)) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_riproduzione VCR \_ MCI \_
</dt> <dd>

Il membro **dwAt** della struttura identificata da *lpPlay* contiene un'ora di inizio dell'intero comando o se il dispositivo viene riavviato, quando il dispositivo raggiunge la posizione dalla posizione specificata dal comando [MCI \_ cue](mci-cue.md) .

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>\_ \_ riproduzione \_ REverse VCR MCI
</dt> <dd>

La riproduzione deve essere eseguita in ordine inverso.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_ \_ analisi riproduzione VCR \_ MCI
</dt> <dd>

La riproduzione dovrebbe essere il più veloce possibile mantenendo l'output del video.

</dd> </dl>

Per i dispositivi VCR, *lpPlay* punta a una struttura parametri di [**riproduzione del \_ VCR \_ \_ MCI**](mci-vcr-play-parms.md) .

Con il tipo di dispositivo **videodisco** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_ \_ riproduzione \_ rapida di MCI VD
</dt> <dd>

Riproduzione rapida.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>\_Riproduci MCI VD \_ \_ Reverse
</dt> <dd>

Riproduci in ordine inverso.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_ \_ analisi riproduzione MCI \_ VD
</dt> <dd>

Eseguire un'analisi rapida.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>\_ \_ riproduzione \_ lenta di MCI VD
</dt> <dd>

Riproduci lentamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_velocità di \_ riproduzione MCI VD \_
</dt> <dd>

La velocità di riproduzione è inclusa nel membro **dwSpeed** della struttura identificata da *lpPlay*.

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

 

