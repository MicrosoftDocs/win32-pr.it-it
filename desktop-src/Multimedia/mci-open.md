---
title: MCI_OPEN comando (Mmsystem.h)
description: Il comando MCI \_ OPEN inizializza un dispositivo o un file. Tutti i dispositivi riconoscono questo comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN comando Windows Multimedia
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
ms.openlocfilehash: a84c95df35ecd602c207daa716b62d90f6bdc79b0ede7f937d3a38e6d6a9373b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689981"
---
# <a name="mci_open-command"></a>Comando MCI \_ OPEN

Il comando MCI \_ OPEN inizializza un dispositivo o un file. Tutti i dispositivi riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY o MCI \_ WAIT. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Puntatore a [**una struttura MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il flag MCI OPEN TYPE deve essere usato ogni volta che viene specificato \_ un dispositivo nella funzione \_ [**mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Se si apre un dispositivo specificando una costante di tipo dispositivo, è necessario specificare il flag MCI OPEN TYPE ID oltre a \_ \_ \_ MCI \_ OPEN \_ TYPE. Per un elenco delle costanti di tipo dispositivo, vedere [Tipi di dispositivo MCI](mci-device-types.md).

Se il flag MCI OPEN SHAREABLE non viene specificato quando un dispositivo o un file viene aperto inizialmente, tutti i comandi MCI OPEN successivi per il dispositivo o \_ il file avranno esito \_ \_ negativo. Se il dispositivo o il file è già aperto e questo flag non è specificato, la chiamata avrà esito negativo anche se il primo comando open ha specificato MCI \_ OPEN \_ SHAREABLE. File aperti per MCISEQ. DRV e MCIWAVE. I dispositivi DRV non sono gestibili.

La distinzione tra maiuscole e minuscole viene ignorata nel nome del dispositivo, ma non possono essere presenti spazi vuoti iniziali o finali.

Per usare la selezione automatica dei tipi (tramite le voci nel Registro di sistema), assegnare il nome file e l'estensione di file al membro **lpstrElementName** della struttura identificata da *lpOpen,* impostare il membro **lpstrDeviceType** su **NULL** e impostare il flag MCI \_ OPEN \_ ELEMENT.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ OPEN:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ OPEN \_ ALIAS
</dt> <dd>

Un alias è incluso nel **membro lpstrAlias** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ OPEN \_ CONDIVISIBILE
</dt> <dd>

Il dispositivo o il file deve essere aperto come condivisione.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ OPEN \_ TYPE
</dt> <dd>

Un nome di tipo di dispositivo o una costante è incluso nel **membro lpstrDeviceType** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>ID DEL TIPO \_ MCI \_ \_ OPEN
</dt> <dd>

La parola di ordine basso del membro **lpstrDeviceType** della struttura identificata da *lpOpen* contiene un identificatore di tipo di dispositivo MCI standard e la parola di ordine alto contiene facoltativamente l'indice ordinale per il dispositivo. Usare questo flag con il flag MCI \_ OPEN \_ TYPE.

</dd> </dl>

Ai dispositivi composti si applicano i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>ELEMENTO \_ MCI \_ OPEN
</dt> <dd>

Un nome file è incluso nel **membro lpstrElementName** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>ID ELEMENTO \_ MCI OPEN \_ \_
</dt> <dd>

Il **membro lpstrElementName** della struttura identificata da *lpOpen* viene interpretato come valore **DWORD** e ha un significato interno al dispositivo. Usare questo flag con il flag MCI \_ OPEN \_ ELEMENT.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

Il dispositivo deve ridurre il numero di colori statici (di sistema) nella tavolozza. Ciò aumenta il numero di colori disponibili per il rendering del flusso video. Questo flag si applica solo ai dispositivi che condividono una tavolozza con Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ OPEN \_ PARENT
</dt> <dd>

L'handle della finestra padre viene specificato nel **membro hWndParent** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ OPEN \_ WS
</dt> <dd>

Uno stile di finestra viene specificato nel **membro dwStyle** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT
</dt> <dd>

Indica una preferenza per il supporto dei dispositivi MCI a 16 bit.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ OPEN \_ 32BIT
</dt> <dd>

Indica una preferenza per il supporto dei dispositivi MCI a 32 bit.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpOpen* punta a una [**struttura MCI \_ DGV \_ OPEN \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo overlay:**

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ OPEN \_ PARENT
</dt> <dd>

L'handle della finestra padre viene specificato nel **membro hWndParent** della struttura identificata da *lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ OPEN \_ WS
</dt> <dd>

Uno stile di finestra viene specificato nel **membro dwStyle** della struttura identificata da *lpOpen*. Il **valore dwStyle** specifica lo stile della finestra che verrà creata e visualizzata dal driver se l'applicazione non ne fornisce uno. Il parametro style accetta un numero intero che definisce lo stile della finestra. Queste costanti sono uguali agli stili di finestra standard, ad esempio WS \_ CHILD, WS \_ OVERLAPPEDWINDOW o WS \_ POPUP.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpOpen* punta a una [**struttura PARMS MCI \_ OVLY \_ OPEN. \_**](mci-ovly-open-parms.md)

Il flag aggiuntivo seguente viene usato con il **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI \_ WAVE \_ OPEN \_ BUFFER
</dt> <dd>

La lunghezza del buffer viene specificata nel **membro dwBufferSeconds** della struttura identificata da *lpOpen*.

</dd> </dl>

Per i dispositivi waveform-audio, il *parametro lpOpen* punta a una [**struttura MCI WAVE OPEN \_ \_ \_ PARMS.**](mci-wave-open-parms.md) Il driver MCIWAVE richiede un dispositivo waveform-audio asincrono.

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

 

