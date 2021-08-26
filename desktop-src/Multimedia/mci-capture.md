---
title: MCI_CAPTURE comando (Mmsystem.h)
description: Il comando MCI \_ CAPTURE acquisisce il contenuto del buffer dei frame e lo archivia in un file specificato. I dispositivi video digitali riconoscono questo comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE comando Windows Multimedia
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
ms.openlocfilehash: 7cc6bc6e31fd66153a8ea867f56a4e2638ad1f3392a284a61818e521327e52d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039451"
---
# <a name="mci_capture-command"></a>Comando MCI \_ CAPTURE

Il comando MCI \_ CAPTURE acquisisce il contenuto del buffer dei frame e lo archivia in un file specificato. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Puntatore a [**una struttura MCI \_ DGV \_ CAPTURE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Ai dispositivi con video digitali si applicano i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ CAPTURE \_ AS
</dt> <dd>

Il **membro lpstrFileName** della struttura identificata da *lpCapture* contiene un indirizzo di un buffer che specifica il percorso e il nome file di destinazione. Questo flag è obbligatorio.

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV \_ CAPTURE \_ AT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpCapture* contiene un rettangolo valido. Il rettangolo specifica l'area rettangolare all'interno del buffer frame ritagliato e salvato su disco. Se omesso, l'area ritagliata viene impostata per impostazione predefinita sul rettangolo specificato o predefinito in un comando [MCI \_ PUT](mci-put.md) precedente che specifica l'area di origine per questa istanza del driver di dispositivo.

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

 

