---
title: MCI_SETTUNER comando (Mmsystem.h)
description: Il comando MCI \_ SETTUNER imposta il canale corrente sul sintassi. I dispositivi vcr riconoscono questo comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER comando Windows Multimedia
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
ms.openlocfilehash: dc0e4d812a89c8b7ca5a8e65b322e19dcb4f7d4e7e2ef8c49745ebb16e22af65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138107"
---
# <a name="mci_settuner-command"></a>Comando MCI \_ SETTUNER

Il comando MCI \_ SETTUNER imposta il canale corrente sul sintassi. I dispositivi vcr riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Puntatore a [**una struttura MCI \_ VCR \_ SETTUNER \_ PARMS.**](mci-vcr-settuner-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano ai dispositivi vcr:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>CANALE MCI \_ VCR \_ \_ SETTUNER
</dt> <dd>

Il **membro dwChannel** della struttura identificata da *lpSetTuner* contiene il nuovo numero di canale.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>CANALE DI \_ \_ SETTUNER DEL VIDEOREGISTRATORE MCI \_ IN \_ BASSO
</dt> <dd>

Decrementa il canale del siner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ DOWN
</dt> <dd>

Cerca un canale valido nella direzione inversa.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ UP
</dt> <dd>

Cerca un canale valido nella direzione in avanti.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ UP
</dt> <dd>

Incrementa il canale del siner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>NUMERO \_ DI \_ SETTUNER DEL VIDEOREGISTRATORE MCI \_
</dt> <dd>

Il **membro dwNumber** della struttura identificata da *lpSetTuner* specifica quale sintassi logica influisce su questo comando.

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

 

