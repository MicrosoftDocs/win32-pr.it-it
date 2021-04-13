---
title: Comando MCI_SIGNAL (mmsystem. h)
description: Il \_ comando MCI Signal imposta una posizione specificata nell'area di lavoro. I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Comando MCI_SIGNAL Windows Multimedia
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
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400533"
---
# <a name="mci_signal-command"></a>\_Comando MCI Signal

Il \_ comando MCI Signal imposta una posizione specificata nell'area di lavoro. I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri del segnale DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La finestra il cui handle specificato nel membro **dwCallback** della struttura [**MCI \_ DGV \_ Signal \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) riceve il \_ messaggio MCISIGNAL mm.

I flag seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_segnale DGV \_ MCI \_ a
</dt> <dd>

Una posizione del segnale è inclusa nel membro **dwPosition** della struttura identificata da *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_ \_ annullamento segnale DGV \_ MCI
</dt> <dd>

Rimuove la posizione del segnale specificata dal valore associato al \_ segnale DGV \_ MCI \_ USERVAL.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_segnale DGV \_ MCI \_ ogni
</dt> <dd>

Il valore del periodo del segnale è incluso nel membro **dwPeriod** della struttura identificata da *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_posizione del \_ segnale \_ DGV MCI
</dt> <dd>

Il dispositivo invierà il valore di posizione con il messaggio di Windows invece del valore specificato dall'utente.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_ \_ USERVAL segnale DGV \_ MCI
</dt> <dd>

Un valore di dati è incluso nel membro **dwUserParm** della struttura identificata da *lpSignal*. Il valore di dati associato a questa richiesta viene restituito con il messaggio di Windows.

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

 

