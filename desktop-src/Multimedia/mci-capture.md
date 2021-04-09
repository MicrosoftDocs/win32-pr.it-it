---
title: Comando MCI_CAPTURE (mmsystem. h)
description: Il \_ comando di acquisizione di MCI acquisisce il contenuto del buffer del frame e lo archivia in un file specificato. I dispositivi digitali video riconoscono questo comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Comando MCI_CAPTURE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964531"
---
# <a name="mci_capture-command"></a>\_Comando di acquisizione MCI

Il \_ comando di acquisizione di MCI acquisisce il contenuto del buffer del frame e lo archivia in un file specificato. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
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

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Puntatore a una [**struttura \_ DGV \_ Capture \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_DGV \_ di acquisizione \_ MCI
</dt> <dd>

Il membro **lpstrFileName** della struttura identificata da *lpCapture* contiene un indirizzo di un buffer che specifica il percorso e il nome del file di destinazione. (Questo flag è obbligatorio).

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_acquisizione DGV \_ MCI \_ in
</dt> <dd>

Il membro **RC** della struttura identificato da *lpCapture* contiene un rettangolo valido. Il rettangolo specifica l'area rettangolare all'interno del buffer del frame che viene ritagliata e salvata su disco. Se omesso, per impostazione predefinita l'area ritagliata viene impostata sul rettangolo specificato o impostato come predefinito in un comando [MCI \_ put](mci-put.md) precedente che specifica l'area di origine per questa istanza del driver di dispositivo.

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

 

