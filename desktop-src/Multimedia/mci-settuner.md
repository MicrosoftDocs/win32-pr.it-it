---
title: Comando MCI_SETTUNER (mmsystem. h)
description: Il \_ comando MCI SEtuner imposta il canale corrente sul sintonizzatore. I dispositivi VCR riconoscono questo comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Comando MCI_SETTUNER Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048741"
---
# <a name="mci_settuner-command"></a>\_Comando MCI SEtuner

Il \_ comando MCI SEtuner imposta il canale corrente sul sintonizzatore. I dispositivi VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
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

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri di MCI VCR**](mci-vcr-settuner-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I seguenti flag aggiuntivi si applicano ai dispositivi VCR:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_canale di \_ regolazione del VCR \_ MCI
</dt> <dd>

Il membro **dwChannel** della struttura identificata da *lpSetTuner* contiene il nuovo numero di canale.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_canale di \_ setuner VCR MCI \_ \_ disattivato
</dt> <dd>

Decrementa il canale del sintonizzatore.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_ricerca del \_ \_ canale MCI VCR \_ \_
</dt> <dd>

Cerca un canale valido nella direzione inversa.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ ricerca canale MCI \_ VCR \_
</dt> <dd>

Cerca un canale valido nella direzione in avanti.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_canale di \_ setuner VCR MCI \_ \_ attivo
</dt> <dd>

Incrementa il canale del sintonizzatore.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_numero di \_ setuner \_ VCR MCI
</dt> <dd>

Il membro **dwNumber** della struttura identificata da *lpSetTuner* specifica quale sintonizzatore logico influisce su questo comando.

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

 

