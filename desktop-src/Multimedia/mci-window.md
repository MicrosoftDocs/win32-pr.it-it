---
title: Comando MCI_WINDOW (mmsystem. h)
description: Il \_ comando finestra MCI specifica la finestra e le caratteristiche della finestra per i dispositivi grafici. I dispositivi Digital-video e overlay video riconoscono questo comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Comando MCI_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964366"
---
# <a name="mci_window-command"></a>\_Comando finestra MCI

Il \_ comando finestra MCI specifica la finestra e le caratteristiche della finestra per i dispositivi grafici. I dispositivi Digital-video e overlay video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I dispositivi grafici devono creare una finestra predefinita quando un dispositivo viene aperto, ma non deve visualizzarlo fino a quando non riceve il comando [MCI \_ Play](mci-play.md) . Il \_ comando della finestra MCI viene usato per fornire al dispositivo una finestra creata dall'applicazione e per modificare le caratteristiche di visualizzazione di una finestra di visualizzazione predefinita o definita dall'applicazione. Se l'applicazione fornisce la finestra di visualizzazione, dovrebbe essere preparata ad aggiornare un rettangolo non valido nella finestra.

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ \_ HWND finestra DGV \_ MCI
</dt> <dd>

L'handle della finestra necessaria per l'utilizzo come destinazione è incluso nel membro **HWND** della struttura identificata da *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_stato della \_ finestra \_ DGV MCI
</dt> <dd>

Il membro **nCmdShow** della struttura identificata da *lpWindow* contiene i parametri per l'impostazione dello stato della finestra.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_ \_ testo finestra DGV \_ MCI
</dt> <dd>

Il membro **lpstrText** della struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia usata nella barra del titolo della finestra.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpWindow* punta a una struttura [**DGV della \_ \_ finestra \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .

Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_ \_ \_ disabilitazione dell' \_ estensione OVLY della finestra MCI
</dt> <dd>

Disabilita l'allungamento dell'immagine.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_ \_ \_ Abilita stretch per la finestra OVLY di MCI \_
</dt> <dd>

Abilita l'allungamento dell'immagine.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ \_ HWND finestra OVLY \_ MCI
</dt> <dd>

L'handle della finestra utilizzata per la destinazione è incluso nel membro **HWND** della struttura identificata da *lpWindow*. Impostare questo flag su MCI \_ OVLY \_ Window \_ default per tornare alla finestra predefinita.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_stato della \_ finestra \_ OVLY MCI
</dt> <dd>

Il membro **nCmdShow** della struttura *lpWindow* contiene i parametri per l'impostazione dello stato della finestra. Questo flag equivale a chiamare [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) con il parametro *state* . Le costanti sono le stesse definite in WINDOWS. H (ad esempio \_ , Hide SW, SW \_ Riduci a icona o SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_ \_ testo finestra OVLY \_ MCI
</dt> <dd>

Il membro **lpstrText** della struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia utilizzata per la finestra.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpWindow* punta a una struttura [**OVLY della \_ \_ finestra \_ parametri di MCI**](mci-ovly-window-parms.md) .

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

 

