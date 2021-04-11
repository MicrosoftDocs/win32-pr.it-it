---
title: Comando MCI_RESERVE (mmsystem. h)
description: Il \_ comando MCI Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di dispositivo da usare con la registrazione successiva. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Comando MCI_RESERVE Windows Multimedia
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
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964686"
---
# <a name="mci_reserve-command"></a>\_Comando di riserva MCI

Il \_ comando MCI Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del driver di dispositivo da usare con la registrazione successiva. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Test MCI notifica, MCI \_ Wait o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri della riserva DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Se l'area di lavoro contiene dati non salvati, i dati andranno perduti. Se lo spazio su disco non è riservato prima della registrazione, il comando [MCI \_ record](mci-record.md) esegue una riserva implicita con parametri predefiniti specifici del dispositivo. In alcune implementazioni, Reserve non è obbligatorio e potrebbe essere ignorato dal driver di dispositivo. Il mantenimento dello spazio in modo esplicito garantisce un maggiore controllo sul momento in cui si verifica il ritardo nell'allocazione dei dischi, sulla quantità di spazio allocato e sulla posizione di allocazione dello spazio su disco. La quantità e la posizione dello spazio su disco già riservata per questa istanza del dispositivo possono essere modificate rilasciando la riserva di MCI \_ . Qualsiasi spazio su disco allocato e ancora inutilizzato non viene deallocato fino al salvataggio dei dati registrati o fino alla chiusura dell'istanza del driver di dispositivo.

Se il video è disattivato con il \_ flag MCI off del comando [MCI \_ sevideo](mci-setvideo.md) , lo spazio riservato non include alcun video. Se l'audio è disattivato con il \_ flag MCI off del comando [MCI \_ sefonica](mci-setaudio.md) , lo spazio riservato non include alcun audio. Se l'audio e il video sono spenti o se le dimensioni richieste sono pari a zero, nessuno spazio viene riservato e lo spazio riservato esistente viene deallocato.

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_riserva DGV \_ MCI \_ in
</dt> <dd>

Il membro **lpstrPath** della struttura identificata da *lpReserve* contiene un indirizzo di un buffer contenente il percorso di un file temporaneo. Il buffer contiene solo l'unità e il percorso della directory del file utilizzato per contenere i dati registrati. il nome file viene specificato dal driver di dispositivo. Questo file temporaneo viene eliminato quando l'istanza del dispositivo viene chiusa, a meno che non venga salvata in modo esplicito. Se questo flag viene omesso, il driver di dispositivo specifica la posizione in cui è allocato lo spazio su disco.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_ \_ dimensioni riserva DGV \_ MCI
</dt> <dd>

Il membro **dwSize** della struttura identificata da *lpReserve* specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro per la registrazione. Il valore viene specificato nel formato dell'ora corrente. La quantità di spazio su disco è stimata dal tempo richiesto e da quali formati di file e algoritmi video e audio e valori di qualità sono attivi. Se questo flag viene omesso, è possibile che il driver di dispositivo usi un valore predefinito che definisce.

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

 

