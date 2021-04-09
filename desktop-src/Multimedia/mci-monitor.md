---
title: Comando MCI_MONITOR (mmsystem. h)
description: Il \_ comando MCI monitor specifica l'origine della presentazione. I dispositivi digitali video riconoscono questo comando.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Comando MCI_MONITOR Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964528"
---
# <a name="mci_monitor-command"></a>\_Comando di monitoraggio MCI

Il \_ comando MCI monitor specifica l'origine della presentazione. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
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

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri del monitor DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_metodo di \_ monitoraggio MCI DGV \_
</dt> <dd>

Costante che indica che il metodo di monitoraggio è incluso nel membro **dwMethod** della struttura identificata da *lpMonitor*.

Quando il \_ \_ flag di input di DGV del monitor MCI \_ viene usato nel membro **dwSource** , viene selezionato il metodo di monitoraggio. In genere, diversi metodi di monitoraggio hanno implicazioni diverse sulla modalità di utilizzo dell'hardware. Il metodo di monitoraggio predefinito è selezionato dal dispositivo.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_ \_ origine monitoraggio DGV \_ MCI
</dt> <dd>

Costante che indica che l'origine del monitoraggio è inclusa nel membro **dwSource** della struttura identificata da *lpMonitor*.

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

 

