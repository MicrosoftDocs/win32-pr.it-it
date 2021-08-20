---
title: MCI_RESERVE comando (Mmsystem.h)
description: Il comando MCI RESERVE alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di \_ dispositivo per l'uso con la registrazione successiva. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f21570d37fba9bc0c9595715715a9291aedd30650081edfa5d50f7264cf16c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803462"
---
# <a name="mci_reserve-command"></a>Comando MCI \_ RESERVE

Il comando MCI RESERVE alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di \_ dispositivo per l'uso con la registrazione successiva. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
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

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Puntatore a [**una struttura MCI \_ DGV \_ RESERVE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se l'area di lavoro contiene dati non salvati, questi dati vengono persi. Se lo spazio su disco non è riservato prima della registrazione, il [comando MCI \_ RECORD](mci-record.md) esegue una riserva implicita con parametri predefiniti specifici del dispositivo. In alcune implementazioni, reserve non è obbligatorio e potrebbe essere ignorato dal driver di dispositivo. Riservando esplicitamente spazio è possibile controllare meglio quando si verifica il ritardo per l'allocazione del disco, la quantità di spazio allocata e la posizione in cui viene allocato lo spazio su disco. La quantità e la posizione dello spazio su disco già riservato per questa istanza del dispositivo possono essere modificate emettendo nuovamente MCI \_ RESERVE. Lo spazio su disco allocato e ancora inutilizzato non viene deallocato fino a quando non vengono salvati i dati registrati o fino alla chiusura dell'istanza del driver di dispositivo.

Se il video è disattivato con il flag MCI OFF del comando \_ [MCI \_ SETVIDEO,](mci-setvideo.md) lo spazio riservato non include alcun video. Se l'audio è disattivato con il flag MCI OFF del comando \_ [MCI \_ SETAUDIO,](mci-setaudio.md) lo spazio riservato non include audio. Se sia l'audio che il video sono disattivati o se le dimensioni richieste sono pari a zero, non viene riservato spazio e viene deallocato qualsiasi spazio riservato esistente.

I flag aggiuntivi seguenti si applicano ai dispositivi video digitali:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI \_ DGV \_ RESERVE \_ IN
</dt> <dd>

Il **membro lpstrPath** della struttura identificata da *lpReserve* contiene un indirizzo di un buffer contenente la posizione di un file temporaneo. Il buffer contiene solo l'unità e il percorso di directory del file usato per contenere i dati registrati. il nome file viene specificato dal driver di dispositivo. Questo file temporaneo viene eliminato alla chiusura dell'istanza del dispositivo, a meno che non venga salvato in modo esplicito. Se questo flag viene omesso, il driver di dispositivo specifica dove viene allocato lo spazio su disco.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI \_ DGV \_ RESERVE \_ SIZE
</dt> <dd>

Il **membro dwSize** della struttura identificata da *lpReserve* specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro per la registrazione. Il valore è specificato nel formato di ora corrente. La quantità di spazio su disco viene stimata a partire dal tempo richiesto e da quale formato di file, algoritmo video e audio e valori di qualità sono effettivi. Se questo flag viene omesso, il driver di dispositivo potrebbe usare un valore predefinito definito.

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

 

