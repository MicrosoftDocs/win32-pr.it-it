---
title: MCI_UPDATE comando (Mmsystem.h)
description: Il comando MCI \_ UPDATE aggiorna il rettangolo di visualizzazione. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58333b108891a8bcd0e0548d4dcd0db2f2606d1259f0934f19b8f6804afab3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689681"
---
# <a name="mci_update-command"></a>Comando MCI \_ UPDATE

Il comando MCI \_ UPDATE aggiorna il rettangolo di visualizzazione. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

**MCI \_ NOTIFY,** **MCI \_ WAIT** o, per i dispositivi digital-video, **MCI \_ TEST**. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti vengono usati con il tipo di dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ UPDATE \_ HDC
</dt> <dd>

Il **membro hDC** della struttura identificata da *lpDest* contiene una finestra valida del controller di dominio da disegnare. Questo flag è obbligatorio.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Il rettangolo specifica il rettangolo di ritaglio relativo al rettangolo client.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV \_ UPDATE \_ PAINT
</dt> <dd>

Un'applicazione usa questo flag quando riceve un [**messaggio WM \_ PAINT**](/windows/desktop/gdi/wm-paint) destinato a un controller di dominio di visualizzazione. Un dispositivo frame-buffer dipinge in genere il colore della chiave. Se il dispositivo di visualizzazione non dispone di un buffer di frame, potrebbe ignorare il comando MCI UPDATE quando viene usato il \_ flag **MCI \_ DGV \_ UPDATE \_ PAINT** perché la visualizzazione verrà ridisegnata durante l'operazione di riproduzione.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpDest* punta a una [**struttura MCI \_ DGV \_ UPDATE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)

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

 

