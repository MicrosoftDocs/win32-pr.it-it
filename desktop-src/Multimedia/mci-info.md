---
title: MCI_INFO comando (Mmsystem.h)
description: Il comando MCI \_ INFO recupera informazioni stringa da un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO comando Windows Multimedia
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
ms.openlocfilehash: 18d53acbdfeb0c13b4b9e201d1bea23008dfbaa83221007152181fe685d09957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039200"
---
# <a name="mci_info-command"></a>Comando MCI \_ INFO

Il comando MCI \_ INFO recupera informazioni stringa da un dispositivo. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro **lpstrReturn** della struttura identificata da *lpInfo*. Il **membro dwRetSize** specifica la lunghezza del buffer per i dati restituiti.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Puntatore a [**una struttura MCI \_ INFO \_ PARMS.**](mci-info-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il flag aggiuntivo standard e specifico del comando seguente si applica a tutti i dispositivi che supportano MCI \_ INFO:

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>PRODOTTO MCI \_ INFO \_
</dt> <dd>

Ottiene una descrizione dell'hardware associato a un dispositivo. I dispositivi devono fornire una descrizione che identifica sia il driver che l'hardware usato.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al **tipo di dispositivo cdaudio:**

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI \_ INFO \_ MEDIA \_ IDENTITY
</dt> <dd>

Produce un identificatore univoco per il CD audio attualmente caricato nel lettore su cui viene eseguita la query. Questo flag restituisce una stringa di 16 cifre esadecimali.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ INFO \_ MEDIA \_ UPC
</dt> <dd>

Produce il codice UPC (Universal Product Code) codificato in un CD audio. L'UPC è una stringa di cifre. Potrebbe non essere disponibile per tutti i CD.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>ELEMENTO MCI \_ DGV \_ INFO \_
</dt> <dd>

Una costante che indica le informazioni desiderate è inclusa nel **membro dwItem** della struttura identificata da *lpInfo*. Per i dispositivi video digitali sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ INFO \_ AUDIO \_ ALG
</dt> <dd>

Restituisce il nome dell'algoritmo di compressione audio corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ INFO \_ AUDIO \_ QUALITY
</dt> <dd>

Restituisce il nome del descrittore di qualità audio corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI \_ DGV \_ INFO \_ STILL \_ ALG
</dt> <dd>

Restituisce il nome per l'algoritmo di compressione dell'immagine ancora corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI \_ DGV \_ INFO \_ STILL \_ QUALITY
</dt> <dd>

Restituisce il nome del descrittore di qualità dell'immagine ancora corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>UTILIZZO DELLE INFORMAZIONI \_ MCI \_ \_ DGV
</dt> <dd>

Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dell'oggetto visivo o dei dati udibili nell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ INFO \_ VIDEO \_ ALG
</dt> <dd>

Restituisce il nome dell'algoritmo di compressione video corrente.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>QUALITÀ VIDEO MCI \_ DGV \_ INFO \_ \_
</dt> <dd>

Restituisce il nome del descrittore di qualità video corrente.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>VERSIONE DI MCI \_ INFO \_
</dt> <dd>

Restituisce il livello di rilascio del driver di dispositivo e dell'hardware. Gli sviluppatori di driver di dispositivo devono documentare la sintassi della stringa restituita.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI \_ DGV \_ INFO \_ TEXT
</dt> <dd>

Ottiene la didascalia della finestra.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>FILE DI \_ INFORMAZIONI MCI \_
</dt> <dd>

Ottiene il percorso e il nome file dell'ultimo file specificato con il [comando MCI \_ OPEN](mci-open.md) o [MCI \_ LOAD.](mci-load.md) Se non è stato specificato un file, il dispositivo restituisce una stringa con terminazione Null. Questo flag è supportato solo dai dispositivi che restituiscono **TRUE** al flag MCI \_ GETDEVCAPS \_ USES FILES del comando \_ [MCI \_ GETDEVCAPS.](mci-getdevcaps.md)

</dd> </dl>

Per i dispositivi video digitali, *lpInfo* punta a una [**struttura MCI \_ DGV \_ INFO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)

I flag aggiuntivi seguenti si applicano al **tipo di dispositivo sequencer:**

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>COPYRIGHT DI MCI \_ \_ INFO
</dt> <dd>

Ottiene l'informativa sul copyright del file MIDI dall'evento meta copyright.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>FILE DI \_ INFORMAZIONI MCI \_
</dt> <dd>

Ottiene il nome file del file corrente. Questo flag è supportato solo dai dispositivi che restituiscono **TRUE** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il flag MCI \_ GETDEVCAPS \_ USES \_ FILES.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI \_ INFO \_ NAME
</dt> <dd>

Ottiene il nome della sequenza dall'evento meta sequence/track name.

</dd> </dl>

Il flag aggiuntivo seguente si applica al **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>VERSIONE DI MCI \_ VCR \_ INFO \_
</dt> <dd>

Imposta **il membro lpstrReturn** della [**struttura MCI INFO \_ \_ PARMS**](mci-info-parms.md) in modo che punti al numero di versione. Imposta anche il **membro dwRetSize** uguale alla lunghezza della stringa a cui punta.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al **tipo di dispositivo di** sovrapposizione:

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>FILE DI \_ INFORMAZIONI MCI \_
</dt> <dd>

Ottiene il nome file del file corrente. Questo flag è supportato solo dai dispositivi che restituiscono **TRUE** al flag MCI \_ GETDEVCAPS \_ USES FILES del comando \_ [MCI \_ GETDEVCAPS.](mci-getdevcaps.md)

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI \_ OVLY \_ INFO \_ TEXT
</dt> <dd>

Ottiene la didascalia della finestra associata al dispositivo di sovrapposizione video.

</dd> </dl>

I flag aggiuntivi seguenti si applicano al **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>FILE DI \_ INFORMAZIONI MCI \_
</dt> <dd>

Ottiene il nome file del file corrente. Questo flag è supportato dai dispositivi che restituiscono **TRUE** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il flag MCI \_ GETDEVCAPS \_ USES \_ FILES.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Ottiene il nome del prodotto dell'input corrente.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ OUTPUT
</dt> <dd>

Ottiene il nome del prodotto dell'output corrente e il relativo valore è specifico del dispositivo.

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

 

