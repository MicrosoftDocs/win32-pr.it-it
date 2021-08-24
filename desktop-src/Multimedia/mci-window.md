---
title: MCI_WINDOW comando (Mmsystem.h)
description: Il comando MCI \_ WINDOW specifica la finestra e le caratteristiche della finestra per i dispositivi grafici. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW comando Windows Multimedia
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
ms.openlocfilehash: 3270dce8b2127cce783c7c3b8bf21102590cd3e82d74a3e990a3117c59772381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783691"
---
# <a name="mci_window-command"></a>Comando MCI \_ WINDOW

Il comando MCI \_ WINDOW specifica la finestra e le caratteristiche della finestra per i dispositivi grafici. I dispositivi di sovrimpressione video e digitale riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi video digitali, MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Puntatore a una [**struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I dispositivi grafici devono creare una finestra predefinita all'apertura di un dispositivo, ma non devono visualizzarla fino a quando non ricevono il [comando MCI \_ PLAY.](mci-play.md) Il comando MCI WINDOW viene usato per fornire una finestra creata dall'applicazione al dispositivo e per modificare le caratteristiche di visualizzazione di una finestra di visualizzazione predefinita o definita \_ dall'applicazione. Se l'applicazione fornisce la finestra di visualizzazione, deve essere preparata ad aggiornare un rettangolo non valido nella finestra.

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>FINESTRA \_ DGV MCI \_ \_ HWND
</dt> <dd>

L'handle della finestra necessaria per l'uso come destinazione è incluso nel membro **hWnd** della struttura identificata da *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>STATO DELLA \_ FINESTRA DGV MCI \_ \_
</dt> <dd>

Il **membro nCmdShow della** struttura identificata da *lpWindow* contiene parametri per l'impostazione dello stato della finestra.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>TESTO DELLA \_ FINESTRA DGV MCI \_ \_
</dt> <dd>

Il **membro lpstrText della** struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia usata nella barra del titolo della finestra.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpWindow* punta a una [**struttura MCI \_ DGV \_ WINDOW \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)

I flag aggiuntivi seguenti vengono usati con il tipo **di dispositivo di** sovrimpressione:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI \_ OVLY \_ WINDOW \_ DISABLE \_ STRETCH
</dt> <dd>

Disabilita l'estensione dell'immagine.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>ABILITARE L'ESTENSIONE DELLA FINESTRA DI MCI \_ OVLY \_ \_ \_
</dt> <dd>

Abilita l'estensione dell'immagine.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>FINESTRA DI MCI \_ OVLY \_ \_ HWND
</dt> <dd>

L'handle della finestra usata per la destinazione è incluso nel membro **hWnd** della struttura identificata da *lpWindow.* Impostare questo flag su MCI \_ OVLY \_ WINDOW DEFAULT per tornare alla finestra \_ predefinita.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>STATO DELLA FINESTRA DI MCI \_ OVLY \_ \_
</dt> <dd>

Il **membro nCmdShow** della struttura *lpWindow* contiene parametri per l'impostazione dello stato della finestra. Questo flag equivale a chiamare [ShowWindow con](/windows/win32/api/winuser/nf-winuser-showwindow) il *parametro state.* Le costanti sono uguali a quelle definite in WINDOWS. H (ad esempio SW \_ HIDE, SW \_ MINIMIZE o SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>TESTO DELLA FINESTRA DI MCI \_ OVLY \_ \_
</dt> <dd>

Il **membro lpstrText** della struttura identificata da *lpWindow* contiene un indirizzo di un buffer contenente la didascalia usata per la finestra.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpWindow* punta a una [**struttura MCI \_ OVLY \_ WINDOW \_ PARMS.**](mci-ovly-window-parms.md)

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

 

