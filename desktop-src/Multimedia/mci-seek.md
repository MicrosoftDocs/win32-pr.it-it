---
title: Comando MCI_SEEK (mmsystem. h)
description: Il \_ comando MCI Seek imposta la posizione corrente nel contenuto il più rapidamente possibile.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Comando MCI_SEEK Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048053"
---
# <a name="mci_seek-command"></a>\_Comando di ricerca MCI

Il \_ comando MCI Seek imposta la posizione corrente nel contenuto il più rapidamente possibile. L'output di video e audio è disabilitato durante la ricerca. Al termine della ricerca, il dispositivo viene arrestato. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri Seek di MCI**](mci-seek-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Se la dimensione di un campione di dati per un dispositivo è maggiore di 1 byte, ad esempio con i dati audio stereo della forma d'onda, questo comando si sposta all'inizio dell'esempio più vicino quando una posizione specificata non coincide con l'inizio di un campione.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano la \_ ricerca MCI:

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_ricerca \_ di MCI alla \_ fine
</dt> <dd>

Consente di cercare alla fine del contenuto.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>\_Inizio ricerca \_ MCI \_
</dt> <dd>

Consente di cercare all'inizio del contenuto.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a
</dt> <dd>

Una posizione viene inclusa nel membro **dwTo** della struttura identificata da *lpSeek*. Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) . Non utilizzare questo flag con la ricerca \_ MCI \_ per \_ terminare o MCI \_ Seek \_ per \_ avviare.

</dd> </dl>

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR \_ Seek \_ at
</dt> <dd>

Il membro **dwAt** della struttura identificata da *lpSeek* contiene un'ora di inizio dell'intero comando.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_indicatore di \_ ricerca \_ VCR MCI
</dt> <dd>

Il membro **dwMark** della struttura identificata da *lpSeek* contiene il contrassegno numerato da cercare.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>\_ \_ ricerca \_ INversa VCR MCI
</dt> <dd>

Direzione di ricerca inversa; viene usato solo con il flag del \_ contrassegno di ricerca MCI VCR \_ \_ .

</dd> </dl>

Per i dispositivi VCR, il parametro *lpSeek* punta a una struttura [**\_ \_ \_ parametri di ricerca VCR MCI**](mci-vcr-seek-parms.md) .

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **videodisco** :

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ VD \_ Seek \_ inverso
</dt> <dd>

Direzione di ricerca inversa.

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

 

