---
title: Comando MCI_UPDATE (mmsystem. h)
description: Il \_ comando di aggiornamento MCI Aggiorna il rettangolo di visualizzazione. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Comando MCI_UPDATE Windows Multimedia
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
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121258"
---
# <a name="mci_update-command"></a>\_Comando di aggiornamento MCI

Il \_ comando di aggiornamento MCI Aggiorna il rettangolo di visualizzazione. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ NOTIFICA**, **MCI \_ wait** o, per i dispositivi video digitali, **MCI \_ test**. Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>\_ \_ aggiornamento HDC DGV \_ di MCI
</dt> <dd>

Il membro **HDC** della struttura identificato da *lpDest* contiene una finestra valida del controller di dominio da disegnare. Questo flag è obbligatorio.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Il rettangolo specifica il rettangolo di ridimensionamento rispetto al rettangolo client.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_ \_ disegno aggiornamento DGV \_ MCI
</dt> <dd>

Un'applicazione utilizza questo flag quando riceve un messaggio [**di \_ disegno WM**](/windows/desktop/gdi/wm-paint) destinato a un controller di dominio di visualizzazione. Un dispositivo buffer frame in genere disegna il colore della chiave. Se il dispositivo di visualizzazione non dispone di un buffer di frame, potrebbe ignorare il \_ comando di aggiornamento MCI quando viene usato il flag di **\_ \_ \_ disegno dell'aggiornamento DGV di MCI** , perché la visualizzazione verrà ridisegnata durante l'operazione di riproduzione.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpDest* punta a una [**struttura \_ DGV \_ Update \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .

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

 

