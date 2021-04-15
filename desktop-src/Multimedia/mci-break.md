---
title: Comando MCI_BREAK (mmsystem. h)
description: Il \_ comando MCI break imposta un tasto di pausa per un dispositivo MCI. MCI supporta direttamente questo comando anziché passarlo al dispositivo. Qualsiasi applicazione MCI può utilizzare questo comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Comando MCI_BREAK Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476240"
---
# <a name="mci_break-command"></a>\_Comando di Interrompi MCI

Il \_ comando MCI break imposta un tasto di pausa per un dispositivo MCI. MCI supporta direttamente questo comando anziché passarlo al dispositivo. Qualsiasi applicazione MCI può utilizzare questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi VCR (Digital-video e videoregistratore), \_ test MCI. Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri break MCI**](mci-break-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Potrebbe essere necessario premere il tasto Break più volte per interrompere un'operazione di attesa. Quando si preme il tasto INTERR dopo che l'attesa di un dispositivo è stata annullata, è possibile inviare l'operazione Se un'applicazione ha un'azione definita per il codice della chiave virtuale, può rispondere inavvertitamente all'interruzioni. Ad esempio, un'applicazione che usa \_ l'annullamento VK per un tasto di scelta rapida può rispondere al tasto Ctrl + Break predefinito se viene premuto dopo l'annullamento di un'attesa.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND Interrompi MCI \_
</dt> <dd>

Il membro **hwndBreak** della struttura identificata da *lpBreak* contiene un handle di finestra che deve essere la finestra corrente per abilitare il rilevamento delle interruzioni per quel dispositivo MCI. Si tratta in genere della finestra principale dell'applicazione. Se omesso, MCI non controlla l'handle della finestra corrente.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_chiave di pausa MCI \_
</dt> <dd>

Il membro **nVirtKey** della struttura identificata da *lpBreak* specifica il codice della chiave virtuale usato per la chiave Break. Per impostazione predefinita, MCI assegna CTRL + INTERr come chiave di break. Questo flag è obbligatorio se MCI \_ break \_ off non è specificato.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interruzione di MCI \_ \_
</dt> <dd>

Disabilita qualsiasi chiave di break esistente per il dispositivo indicato.

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

 

