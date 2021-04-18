---
title: Comando MCI_LIST (mmsystem. h)
description: Il \_ comando MCI List ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Comando MCI_LIST Windows Multimedia
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
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519036"
---
# <a name="mci_list-command"></a>\_Comando elenco MCI

Il \_ comando MCI List ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo. I dispositivi Digital-video e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>\_elenco DGV \_ MCI \_
</dt> <dd>

Il membro **lpstrAlgorithm** della struttura identificata da *lpList* contiene un indirizzo di un buffer contenente il nome di un algoritmo. Il nome viene usato per recuperare i tipi di descrittori di qualità associati a un algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_ \_ conteggio elenco DGV \_ MCI
</dt> <dd>

Restituisce il numero di opzioni del tipo specificato.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_ \_ elemento elenco DGV \_ MCI
</dt> <dd>

Costante che indica che il tipo di elenco è incluso nel membro **dwItem** della struttura identificata da *lpList*. Questo flag è obbligatorio. Utilizzare una delle seguenti costanti per indicare il tipo di elenco:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ List \_ audio \_ ALG
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi audio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_ \_ \_ qualità audio elenco DGV \_ MCI
</dt> <dd>

Il comando deve recuperare i livelli di qualità audio. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_ \_ \_ flusso audio elenco DGV \_ MCI
</dt> <dd>

Il comando deve recuperare i nomi dei flussi audio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_elenco DGV \_ MCI \_ ancora \_ al
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi ancora.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>\_elenco DGV di MCI \_ \_ ancora \_ qualità
</dt> <dd>

Il comando deve recuperare i livelli qualitativi. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>VIDEO di MCI \_ DGV \_ List \_ \_ ALG
</dt> <dd>

Il comando deve recuperare i nomi degli algoritmi video.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_ \_ \_ qualità video elenco DGV \_ MCI
</dt> <dd>

Il comando deve recuperare i livelli di qualità del video. I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*. Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_ \_ \_ origine video elenco DGV \_ MCI
</dt> <dd>

Il comando deve restituire informazioni sulle origini video. Quando viene usato con \_ il \_ \_ numero di elenchi DGV di MCI, il comando restituisce il numero di origini video. Se usato con il \_ \_ \_ numero di elenco DGV di MCI, il comando restituisce il tipo di un'origine video. MCI definisce i tipi seguenti:

-   MCI \_ DGV \_ sevideo \_ src \_ Generic
-   MCI \_ DGV \_ video \_ src \_ NTSC
-   DGV di MCI \_ \_ video \_ src \_ PAL
-   MCI \_ DGV \_ video \_ src \_ RGB
-   MCI \_ DGV \_ video \_ src \_ SECAM
-   MCI \_ DGV \_ video \_ src \_ SVIDEO

Potrebbe essere restituita più di un'origine di ogni tipo. Il tipo di origine generico viene usato quando è consentito più di un tipo di segnale per quel connettore.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_ \_ flusso video dell'elenco DGV \_ di \_ MCI
</dt> <dd>

Il comando deve recuperare i nomi dei flussi video.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_numero di \_ elenco \_ DGV MCI
</dt> <dd>

Un indice viene specificato nel membro **dwNumber** della struttura identificata da *lpList*. L'indice deve essere un numero intero compreso tra 1 e il valore restituito per \_ il \_ flag di conteggio DGV elenco MCI \_ .

</dd> </dl>

Per i dispositivi digitali video, *lpList* punta a una [**struttura \_ DGV \_ elenco \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .

I flag aggiuntivi seguenti si applicano al tipo di dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_ \_ \_ origine audio elenco VCR \_ MCI
</dt> <dd>

Elenca gli input o i tipi audio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_ \_ conteggio elenco VCR \_ MCI
</dt> <dd>

Imposta il membro **dwReturn** della struttura identificata da *lpList* sul numero totale di input video o audio.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>\_numero di \_ elenco \_ VCR MCI
</dt> <dd>

Imposta il membro **dwReturn** della struttura identificata da *lpList* sul tipo di input video o audio specificato dal membro **dwNumber** .

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_ \_ \_ origine video elenco VCR \_ MCI
</dt> <dd>

Elenca gli input o i tipi di video.

</dd> </dl>

Per i dispositivi VCR, *lpList* punta a una struttura [**\_ \_ \_ parametri elenco VCR MCI**](mci-vcr-list-parms.md) .

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

 

