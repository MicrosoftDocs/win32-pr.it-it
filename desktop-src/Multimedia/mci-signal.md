---
title: MCI_SIGNAL comando (Mmsystem.h)
description: Il comando MCI \_ SIGNAL imposta una posizione specificata nell'area di lavoro. I dispositivi video digitali riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda7585ad63415f888f5971397df2b27c23710864ea21a8ed5e6ebce1a7c66f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689841"
---
# <a name="mci_signal-command"></a>Comando MCI \_ SIGNAL

Il comando MCI \_ SIGNAL imposta una posizione specificata nell'area di lavoro. I dispositivi video digitali riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Puntatore a [**una struttura MCI \_ DGV \_ SIGNAL \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La finestra il cui handle specificato nel **membro dwCallback** della struttura [**MCI \_ DGV \_ SIGNAL \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) riceve il messaggio MM \_ MCISIGNAL.

I flag seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV \_ SIGNAL \_ AT
</dt> <dd>

Una posizione del segnale è inclusa nel **membro dwPosition** della struttura identificata da *lpSignal.*

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI \_ DGV \_ SIGNAL \_ CANCEL
</dt> <dd>

Rimuove la posizione del segnale specificata dal valore associato a MCI \_ DGV \_ SIGNAL \_ USERVAL.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI \_ DGV \_ SIGNAL \_ EVERY
</dt> <dd>

Un valore del periodo di segnale è incluso nel **membro dwPeriod** della struttura identificata da *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>POSIZIONE DEL \_ SEGNALE MCI DGV \_ \_
</dt> <dd>

Il dispositivo invierà il valore della posizione con Windows al posto del valore specificato dall'utente.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ SIGNAL \_ USERVAL
</dt> <dd>

Un valore di dati è incluso **nel membro dwUserParm** della struttura identificata da *lpSignal*. Il valore dei dati associato a questa richiesta viene restituito con il Windows messaggio.

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

 

