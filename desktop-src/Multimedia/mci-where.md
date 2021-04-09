---
title: Comando MCI_WHERE (mmsystem. h)
description: Il \_ comando MCI where ottiene il rettangolo di ridimensionamento per il dispositivo video.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Comando MCI_WHERE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964278"
---
# <a name="mci_where-command"></a>\_Comando MCI where

Il \_ comando MCI where ottiene il rettangolo di ridimensionamento per il dispositivo video. I dispositivi Digital-video e overlay video riconoscono questo comando. I membri **superiore** e **sinistro** dell'oggetto [Rect](/previous-versions//ms536136(v=vs.85)) restituito contengono l'origine del rettangolo di ritaglio e i membri **destro** e **inferiore** contengono la larghezza e l'altezza del rettangolo di ridimensionamento. (Non si tratta dell'utilizzo standard dei membri **destro** e **inferiore** ).

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>DGV MCI in \_ \_ cui \_ destinazione
</dt> <dd>

Ottiene una descrizione dell'area rettangolare utilizzata per visualizzare video e immagini nell'area client della finestra corrente.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>DGV MCI in \_ \_ cui \_ frame
</dt> <dd>

Ottiene una descrizione dell'area rettangolare del buffer del frame in cui vengono ridimensionate le immagini del rettangolo video. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>DGV MCI in \_ \_ cui \_ Max
</dt> <dd>

Se usato con MCI \_ DGV \_ dove \_ Destination o \_ MCI DGV \_ dove \_ source, il rettangolo restituito indica la larghezza e l'altezza massime dell'area specificata. Se usato con la \_ \_ finestra DGV \_ di MCI, il rettangolo restituito indica le dimensioni dell'intero schermo.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ Where \_ source
</dt> <dd>

Ottiene una descrizione dell'area rettangolare (ritagliata dal buffer del frame) allungata per adattarsi al rettangolo di destinazione sullo schermo.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>DGV MCI in \_ \_ cui \_ video
</dt> <dd>

Ottiene una descrizione dell'area rettangolare ritagliata dall'origine della presentazione per riempire il rettangolo del frame nel buffer del frame. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>DGV MCI in \_ \_ cui \_ finestra
</dt> <dd>

Ottiene una descrizione della cornice della finestra di visualizzazione.

</dd> <dt>


</dt> <dd></dd> </dl>

Per i dispositivi digitali video, il parametro *lpQuery* punta a un **DGV MCI in cui è presente la struttura \_ \_ \_ parametri** . **DGV MCI in cui la struttura \_ \_ \_ parametri** è identica alla [**struttura \_ DGV \_ Rect \_ parametri di MCI**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>OVLY MCI in \_ \_ cui \_ destinazione
</dt> <dd>

Ottiene il rettangolo di visualizzazione della destinazione. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>OVLY MCI in \_ \_ cui \_ frame
</dt> <dd>

Ottiene il rettangolo del frame di sovrapposizione. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ source
</dt> <dd>

Ottiene il rettangolo di origine. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>OVLY MCI in \_ \_ cui \_ video
</dt> <dd>

Ottiene il rettangolo del video. Le coordinate del rettangolo vengono inserite nel membro **RC** della struttura identificata da *lpQuery*.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpQuery* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .

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

 

