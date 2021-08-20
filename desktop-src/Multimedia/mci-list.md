---
title: MCI_LIST comando (Mmsystem.h)
description: Il comando MCI \_ LIST ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo. I dispositivi video digitali e VCR riconoscono questo comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9bd3aa35875791d6fa916d9d6831bdcb83a6db43be6e5859ce582243606f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138637"
---
# <a name="mci_list-command"></a>Comando MCI \_ LIST

Il comando MCI \_ LIST ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo. I dispositivi video digitali e VCR riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
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

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Puntatore a una [**struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano al tipo di **dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ LIST \_ ALG
</dt> <dd>

Il **membro lpstrAlgorithm** della struttura identificata da *lpList* contiene l'indirizzo di un buffer contenente il nome di un algoritmo. Il nome viene usato per recuperare i tipi di descrittori di qualità associati a un algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI \_ DGV \_ LIST \_ COUNT
</dt> <dd>

Restituisce il numero di opzioni del tipo specificato.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI \_ DGV \_ LIST \_ ITEM
</dt> <dd>

Una costante che indica il tipo di elenco è inclusa nel **membro dwItem** della struttura identificata da *lpList*. Questo flag è obbligatorio. Usare una delle costanti seguenti per indicare il tipo di elenco:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ ALG
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi audio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ QUALITY
</dt> <dd>

Il comando deve recuperare i livelli di qualità audio. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato usando la stringa "current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ STREAM
</dt> <dd>

Il comando deve recuperare i nomi dei flussi audio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ LIST \_ STILL \_ AL
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi ancora in esecuzione.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ LIST \_ STILL \_ QUALITY
</dt> <dd>

Il comando deve recuperare i livelli di qualità. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato usando la stringa "current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ ALG
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi video.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI \_ DGV LIST VIDEO QUALITY (QUALITÀ VIDEO ELENCO MCI \_ \_ \_ DGV)
</dt> <dd>

Il comando deve recuperare i livelli di qualità video. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato usando la stringa "current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ SOURCE
</dt> <dd>

Il comando deve restituire informazioni sulle origini video. Se usato con MCI \_ DGV \_ LIST \_ COUNT, il comando restituisce il numero di origini video. Se usato con MCI \_ DGV \_ LIST \_ NUMBER, il comando restituisce il tipo di un'origine video. McI definisce i tipi seguenti:

-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO

Potrebbe essere presente più di un'origine di ogni tipo restituito. Il tipo di origine generico viene usato quando per tale connettore è consentito più di un tipo di segnale.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ STREAM
</dt> <dd>

Il comando deve recuperare i nomi dei flussi video.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI \_ DGV \_ LIST \_ NUMBER
</dt> <dd>

Un indice viene specificato nel **membro dwNumber** della struttura identificata da *lpList*. L'indice deve essere un numero intero compreso tra 1 e il valore restituito per il flag MCI \_ DGV \_ LIST \_ COUNT.

</dd> </dl>

Per i dispositivi video digitali, *lpList* punta a una [**struttura MCI \_ DGV \_ LIST \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)

Al tipo di dispositivo **vcr** si applicano i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>ORIGINE \_ AUDIO ELENCO VCR MCI \_ \_ \_
</dt> <dd>

Elencare gli input o i tipi audio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI \_ VCR \_ LIST \_ COUNT
</dt> <dd>

Imposta il **membro dwReturn** della struttura identificata da *lpList* sul numero totale di input video o audio.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI \_ VCR \_ LIST \_ NUMBER
</dt> <dd>

Imposta il **membro dwReturn** della struttura identificata da *lpList* sul tipo di input video o audio specificato dal **membro dwNumber.**

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>ORIGINE \_ VIDEO ELENCO VCR MCI \_ \_ \_
</dt> <dd>

Elencare gli input o i tipi di video.

</dd> </dl>

Per i dispositivi VCR, *lpList* punta a una [**struttura MCI \_ VCR \_ LIST \_ PARMS.**](mci-vcr-list-parms.md)

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

 

