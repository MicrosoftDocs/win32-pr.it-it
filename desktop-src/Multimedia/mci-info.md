---
title: Comando MCI_INFO (mmsystem. h)
description: Il \_ comando MCI info recupera le informazioni sulla stringa da un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Comando MCI_INFO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121123"
---
# <a name="mci_info-command"></a>\_Comando informazioni MCI

Il \_ comando MCI info recupera le informazioni sulla stringa da un dispositivo. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro **lpstrReturn** della struttura identificata da *lpinfo*. Il membro **dwRetSize** specifica la lunghezza del buffer per i dati restituiti.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri info di MCI**](mci-info-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per tutti i dispositivi che supportano le informazioni su MCI, viene applicato il flag di comando e lo standard aggiuntivo seguente \_ :

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_prodotto info \_ MCI
</dt> <dd>

Ottiene una descrizione dell'hardware associato a un dispositivo. I dispositivi devono fornire una descrizione che identifichi sia il driver che l'hardware usato.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **CDAudio** :

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_ \_ identità supporto informazioni \_ MCI
</dt> <dd>

Produce un identificatore univoco per il CD audio attualmente caricato nel lettore sottoposto a query. Questo flag restituisce una stringa di 16 cifre esadecimali.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>\_Media informazioni MCI- \_ \_ UPC
</dt> <dd>

Genera il codice di prodotto universale (UPC) codificato in un CD audio. L'UPC è una stringa di cifre. Potrebbe non essere disponibile per tutti i CDs.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_ \_ elemento info DGV \_ MCI
</dt> <dd>

Costante che indica che le informazioni desiderate sono incluse nel membro **dwItem** della struttura identificata da *lpinfo*. Per i dispositivi digitali video sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ info \_ audio \_ ALG
</dt> <dd>

Restituisce il nome dell'algoritmo di compressione audio corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>\_ \_ \_ qualità audio informazioni DGV \_ MCI
</dt> <dd>

Restituisce il nome del descrittore di qualità audio corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>\_informazioni su DGV MCI \_ \_ ancora \_ ALG
</dt> <dd>

Restituisce il nome dell'algoritmo di compressione delle immagini ancora corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>\_informazioni sul DGV MCI \_ \_ ancora \_ qualità
</dt> <dd>

Restituisce il nome del descrittore di qualità dell'immagine ancora corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_utilizzo delle \_ informazioni \_ DGV MCI
</dt> <dd>

Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dei dati visivi o udibili nell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ info \_ video \_ ALG
</dt> <dd>

Restituisce il nome dell'algoritmo di compressione video corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_ \_ \_ qualità video informazioni DGV \_ MCI
</dt> <dd>

Restituisce il nome del descrittore di qualità video corrente.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versione informazioni \_ MCI
</dt> <dd>

Restituisce il livello di rilascio del driver e dell'hardware del dispositivo. Gli sviluppatori di driver di dispositivo devono documentare la sintassi della stringa restituita.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_ \_ testo informazioni DGV \_ MCI
</dt> <dd>

Ottiene la didascalia della finestra.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_
</dt> <dd>

Ottiene il percorso e il nome del file dell'ultimo file specificato con il comando [MCI \_ Open](mci-open.md) o [MCI \_ Load](mci-load.md) . Se non è stato specificato un file, il dispositivo restituisce una stringa con terminazione null. Questo flag è supportato solo dai dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ Usa il \_ flag file del [comando \_ GETDEVCAPS di MCI](mci-getdevcaps.md) .

</dd> </dl>

Per i dispositivi digitali video, *lpinfo* punta a una [**struttura \_ DGV \_ info \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **sequencer** :

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_informazioni \_ sul copyright di MCI
</dt> <dd>

Ottiene le informazioni sul copyright del file MIDI dall'evento meta del copyright.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_
</dt> <dd>

Ottiene il nome del file corrente. Questo flag è supportato solo dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il \_ flag MCI GETDEVCAPS \_ Usa \_ i file.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_nome informazioni \_ MCI
</dt> <dd>

Ottiene il nome della sequenza dall'evento meta del nome di sequenza/track.

</dd> </dl>

Il flag aggiuntivo seguente si applica al tipo di dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_ \_ versione informazioni VCR \_ MCI
</dt> <dd>

Imposta il membro **lpstrReturn** della [**struttura \_ \_ parametri info di MCI**](mci-info-parms.md) in modo che punti al numero di versione. Imposta anche il membro **dwRetSize** uguale alla lunghezza della stringa a cui punta.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_
</dt> <dd>

Ottiene il nome del file corrente. Questo flag è supportato solo dai dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ Usa il \_ flag file del [comando \_ GETDEVCAPS di MCI](mci-getdevcaps.md) .

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_ \_ testo informazioni OVLY \_ MCI
</dt> <dd>

Ottiene la didascalia della finestra associata al dispositivo di sovrimpressione video.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_file di informazioni MCI \_
</dt> <dd>

Ottiene il nome del file corrente. Questo flag è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il \_ flag MCI GETDEVCAPS \_ Usa \_ i file.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI
</dt> <dd>

Ottiene il nome del prodotto dell'input corrente.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI
</dt> <dd>

Ottiene il nome del prodotto dell'output corrente e il relativo valore è specifico del dispositivo.

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

 

