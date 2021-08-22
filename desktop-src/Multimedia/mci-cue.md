---
title: MCI_CUE comando (Mmsystem.h)
description: Il comando MCI CUE indica un dispositivo in modo che la riproduzione \_ o la registrazione inizi con un ritardo minimo. I dispositivi digital-video, VCR e waveform-audio riconoscono questo comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 432c3fcd89a4841840559e44400716834df260b533d2cf40daa9da5e6a8fb6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784601"
---
# <a name="mci_cue-command"></a>Comando MCI \_ CUE

Il comando MCI CUE indica un dispositivo in modo che la riproduzione \_ o la registrazione inizi con un ritardo minimo. I dispositivi digital-video, VCR e waveform-audio riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV \_ CUE \_ INPUT
</dt> <dd>

Un'istanza di video digitale deve prepararsi per la registrazione. Se l'applicazione non ha spazio su disco riservato, il dispositivo riserva lo spazio su disco usando i parametri predefiniti. L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'input esterno. Questo flag non ha alcun effetto sulla selezione dell'origine della presentazione.

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ CUE \_ NOSHOW
</dt> <dd>

Un'istanza di video digitale deve prepararsi per la riproduzione del fotogramma specificato con il comando senza visualizzarlo. Quando si specifica questo flag, la visualizzazione continua a visualizzare l'immagine nel buffer dei frame anche se il frame corrispondente non è la posizione corrente. Ad esempio, se il buffer dei frame contiene l'immagine dal frame 7, il dispositivo continua a visualizzare il frame 7 quando questo flag viene usato per segnalare il dispositivo a qualsiasi altra posizione. Un comando cue successivo senza questo flag e senza il flag MCI \_ TO visualizza il frame corrente.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI \_ DGV \_ CUE \_ OUTPUT
</dt> <dd>

Un'istanza di video digitale deve prepararsi per la riproduzione. Se l'area di lavoro è sospesa, non viene eseguito alcun posizionamento. Se l'area di lavoro viene arrestata, la posizione potrebbe cambiare in un'immagine del fotogramma chiave precedente. L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'area di lavoro.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Una posizione dell'area di lavoro è inclusa nel membro **dwTo** della struttura identificata da *lpCue*. Le unità assegnate ai valori di posizione vengono specificate usando il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Equivale a cercare una posizione, ad eccezione del fatto che il dispositivo viene sospeso dopo il comando.

</dd> </dl>

Per **i dispositivi digitalvideo,** il *parametro lpCue* punta a una [**struttura PARMS MCI \_ DGV \_ CUE. \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Il **membro dwFrom** della struttura a cui punta *lpCue* contiene la posizione iniziale specificata nel formato di ora corrente.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>DA MCI \_ A
</dt> <dd>

Il **membro dwTo** della struttura a cui punta *lpCue* contiene la posizione finale (sospensione) specificata nel formato di ora corrente.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>INPUT \_ CUE DEL \_ VCR MCI \_
</dt> <dd>

Preparare la registrazione.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>OUTPUT \_ CUE DEL \_ VCR MCI \_
</dt> <dd>

Prepararsi per la riproduzione. Se non vengono specificati NÉ \_ MCI VCR CUE INPUT né MCI VCR CUE OUTPUT, viene presupposto \_ \_ \_ \_ \_ MCI \_ VCR \_ CUE \_ OUTPUT.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>PREROLL DI MCI \_ VCR \_ CUE \_
</dt> <dd>

Aggiungere il dispositivo alla posizione corrente o alla posizione **dwFrom** meno la durata del preroll. In questo modo il dispositivo può prepararsi prima di accedere alla modalità di registrazione o riproduzione.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI \_ VCR \_ CUE \_ REVERSE
</dt> <dd>

La direzione del comando di riproduzione o di registrazione successivo è inversa.

</dd> </dl>

Quando si usa il comando MCI CUE con il flag MCI VCR CUE OUTPUT, è possibile annullare MCI CUE emettendo il comando MCI PLAY con \_ \_ \_ \_ \_ MCI FROM, MCI TO o [ \_ ](mci-play.md) \_ \_ MCI \_ \_ VCR PLAY \_ REVERSE.

Quando si usa MCI CUE per la registrazione con il flag MCI VCR CUE INPUT, è possibile annullare MCI CUE emettendo il comando MCI RECORD con \_ \_ \_ \_ \_ MCI FROM, MCI TO o [ \_ ](mci-record.md) \_ \_ MCI \_ VCR \_ RECORD \_ INITIALIZE.

Per **i dispositivi vcr,** il *parametro lpCue* punta a una [**struttura MCI \_ VCR \_ CUE \_ PARMS.**](mci-vcr-cue-parms.md)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Un dispositivo di input waveform-audio deve essere cued.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ OUTPUT
</dt> <dd>

Un dispositivo di output waveform-audio deve essere cued. Si tratta del flag predefinito se non viene specificato un flag.

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

 

