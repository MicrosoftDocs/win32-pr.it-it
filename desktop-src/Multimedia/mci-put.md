---
title: Comando MCI_PUT (mmsystem. h)
description: Il \_ comando MCI put imposta i rettangoli di origine, di destinazione e di frame. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Comando MCI_PUT Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121675"
---
# <a name="mci_put-command"></a>\_Comando MCI put

Il \_ comando MCI put imposta i rettangoli di origine, di destinazione e di frame. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_client DGV \_ put \_ MCI
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect si applica alla posizione della finestra client. Il rettangolo specificato è relativo alla finestra padre della finestra di visualizzazione. \_ \_ \_ La finestra put DGV di MCI deve essere impostata simultaneamente con questo flag.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_destinazione DGV MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect specifica un rettangolo di destinazione. Il rettangolo di destinazione specifica la parte della finestra client associata a questa istanza del driver di dispositivo che Visualizza l'immagine o il video.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_ \_ frame put DGV \_ MCI
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato al rettangolo del frame. Il rettangolo del frame specifica la parte del buffer del frame utilizzata come destinazione delle immagini video ottenute dal rettangolo video. Il video deve essere ridimensionato in base al rettangolo del buffer del frame.

Il rettangolo viene specificato nelle coordinate del buffer dei frame. Il rettangolo predefinito è il buffer di frame completo. La specifica di questo rettangolo consente al dispositivo di ridimensionare l'immagine mentre digitalizza i dati. I dispositivi che non possono ridimensionare l'immagine rifiutano questo comando con MCIERR \_ funzione non supportata \_ . È possibile usare il \_ flag MCI GETDEVCAPS \_ can \_ stretch con il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) per determinare se un dispositivo ridimensiona l'immagine. Un dispositivo restituisce **false** se non è possibile ridimensionare l'immagine.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_origine DGV MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect specifica un rettangolo di origine. Il rettangolo di origine specifica quale parte del buffer del frame deve essere ridimensionata per adattarsi al rettangolo di destinazione.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_video di DGV MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato al rettangolo del video. Il rettangolo video specifica quale parte dell'origine della presentazione corrente è archiviata nel buffer del frame. Il rettangolo viene specificato utilizzando le coordinate naturali dell'origine della presentazione. Consente di specificare il ritaglio che si verifica prima di archiviare immagini e video nel buffer del frame. Il rettangolo predefinito è l'area di analisi attiva completa oppure le immagini e il video decompressi completi.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ \_ finestra put DGV di MCI \_
</dt> <dd>

Il rettangolo definito per MCI \_ DGV \_ Rect viene applicato alla finestra di visualizzazione. Questo rettangolo è relativo alla finestra padre della finestra di visualizzazione, in genere il desktop. Se la finestra non è specificata, il valore predefinito è la dimensione e la posizione iniziali della finestra.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpDest* contiene un rettangolo valido.

</dd> </dl>

Per i dispositivi digitali video, *lpDest* punta a una [**struttura \_ DGV \_ put \_ parametri di MCI**](/previous-versions//dd743397(v=vs.85)) .

Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_destinazione OVLY MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area della finestra client utilizzata per visualizzare un'immagine. Il rettangolo contiene l'offset e l'extent visibile dell'immagine rispetto all'origine della finestra. Se il frame viene allungato, l'origine viene allungata al rettangolo di destinazione.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_ \_ frame put OVLY \_ MCI
</dt> <dd>

Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area del buffer video usato per ricevere l'immagine del video. Il rettangolo contiene l'offset e l'extent dell'area del buffer rispetto all'origine del buffer del video.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_origine OVLY MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area del buffer video utilizzato come origine dell'immagine digitale. Il rettangolo contiene l'offset e l'extent del rettangolo di ridimensionamento per il buffer video relativo all'origine.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_video di OVLY MCI \_ put \_
</dt> <dd>

Il rettangolo definito per MCI \_ OVLY \_ Rect specifica l'area di acquisizione video dell'origine dal buffer video. Il rettangolo contiene l'offset e l'extent del rettangolo di ridimensionamento per l'origine video rispetto all'origine.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpDest* contiene un rettangolo di visualizzazione valido. Se questo flag non è specificato, il rettangolo predefinito corrisponde alle coordinate del buffer video o della finestra da ritagliare.

</dd> </dl>

Per i dispositivi con sovrimpressione video, *lpDest* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .

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

 

