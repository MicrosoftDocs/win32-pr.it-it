---
title: Comando MCI_OPEN (mmsystem. h)
description: Il \_ comando MCI Open Inizializza un dispositivo o un file. Tutti i dispositivi riconoscono questo comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Comando MCI_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873273"
---
# <a name="mci_open-command"></a>\_Comando di apertura MCI

Il \_ comando MCI Open Inizializza un dispositivo o un file. Tutti i dispositivi riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

\_Attesa notifica MCI o MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri aperta di MCI**](mci-open-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il \_ \_ flag di tipo di apertura MCI deve essere usato ogni volta che un dispositivo viene specificato nella funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se si apre un dispositivo specificando una costante del tipo di dispositivo, è necessario specificare il \_ \_ flag ID tipo aperto MCI \_ oltre al \_ tipo di apertura MCI \_ . Per un elenco di costanti di tipo dispositivo, vedere [tipi di dispositivo MCI](mci-device-types.md).

Se il \_ \_ flag di condivisione Open di MCI non viene specificato quando un dispositivo o un file viene aperto inizialmente, tutti i \_ comandi di apertura di MCI successivi al dispositivo o al file avranno esito negativo. Se il dispositivo o il file è già aperto e questo flag non è specificato, la chiamata avrà esito negativo anche se il primo comando aperto specificato MCI \_ Open \_ Shareable. File aperti per MCISEQ. DRV e MCIWAVE. I dispositivi DRV non sono condivisibili.

Il caso viene ignorato nel nome del dispositivo, ma non possono essere presenti spazi vuoti iniziali o finali.

Per usare la selezione automatica dei tipi (tramite le voci nel registro di sistema), assegnare il nome file e l'estensione del file al membro **lpstrElementName** della struttura identificata da *lpOpen*, impostare il membro **lpstrDeviceType** su **null** e impostare il flag di elemento di \_ apertura MCI \_ .

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ Open:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias di apertura MCI \_
</dt> <dd>

Un alias è incluso nel membro **lpstrAlias** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_ \_ condivisibile aperto MCI
</dt> <dd>

Il dispositivo o il file deve essere aperto come condivisibile.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_tipo di apertura MCI \_
</dt> <dd>

Un nome o una costante del tipo di dispositivo è incluso nel membro **lpstrDeviceType** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ \_ ID tipo aperto \_ MCI
</dt> <dd>

La parola meno significativa del membro **lpstrDeviceType** della struttura identificata da *lpOpen* contiene un identificatore del tipo di dispositivo MCI standard e la parola più significativa, facoltativamente, contiene l'indice ordinale per il dispositivo. Utilizzare questo flag con il \_ flag di \_ tipo aperto MCI.

</dd> </dl>

I flag aggiuntivi seguenti si applicano ai dispositivi composti:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>\_elemento Open di MCI \_
</dt> <dd>

Un nome file è incluso nel membro **lpstrElementName** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ \_ ID elemento aperto \_ MCI
</dt> <dd>

Il membro **lpstrElementName** della struttura identificata da *lpOpen* viene interpretato come valore **DWORD** e ha un significato interno al dispositivo. Utilizzare questo flag con il \_ flag di \_ elemento aperto MCI.

</dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>\_DGV MCI \_ aperto \_ Nostatic
</dt> <dd>

Il dispositivo deve ridurre il numero di colori statici (di sistema) nella tavolozza. Questo aumenta il numero di colori disponibili per il rendering del flusso video. Questo flag si applica solo ai dispositivi che condividono una tavolozza con Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>\_DGV \_ padre aperto \_ MCI
</dt> <dd>

L'handle della finestra padre viene specificato nel membro **hwndParent** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>\_DGV MCI \_ aperto \_ WS
</dt> <dd>

Uno stile della finestra viene specificato nel membro **dwStyle** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>DGV di MCI \_ \_ aperto \_ 16 bit
</dt> <dd>

Indica una preferenza per il supporto dei dispositivi MCI a 16 bit.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>\_DGV MCI \_ aperto a \_ 32 bit
</dt> <dd>

Indica una preferenza per il supporto dei dispositivi MCI a 32 bit.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpOpen* punta a una [**struttura \_ DGV \_ Open \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .

Con il tipo di dispositivo **overlay** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>\_OVLY \_ padre aperto \_ MCI
</dt> <dd>

L'handle della finestra padre viene specificato nel membro **hwndParent** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>\_OVLY MCI \_ aperto \_ WS
</dt> <dd>

Uno stile della finestra viene specificato nel membro **dwStyle** della struttura identificata da *lpOpen*. Il valore **dwStyle** specifica lo stile della finestra che il driver creerà e visualizzerà se l'applicazione non ne fornisce uno. Il parametro style accetta un intero che definisce lo stile della finestra. Queste costanti sono le stesse degli stili della finestra standard (ad esempio WS \_ child, WS \_ OVERLAPPEDWINDOW o WS \_ popup).

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpOpen* punta a una struttura [**\_ OVLY \_ Open \_ parametri di MCI**](mci-ovly-open-parms.md) .

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_buffer di \_ apertura \_ Wave MCI
</dt> <dd>

Viene specificata una lunghezza del buffer nel membro **dwBufferSeconds** della struttura identificata da *lpOpen*.

</dd> </dl>

Per i dispositivi Waveform-Audio, il parametro *lpOpen* punta a una struttura [**\_ \_ \_ parametri Wave Open di MCI**](mci-wave-open-parms.md) . Il driver MCIWAVE richiede un dispositivo audio e una forma d'onda asincrona.

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

 

