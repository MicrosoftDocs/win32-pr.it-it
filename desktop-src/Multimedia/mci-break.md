---
title: MCI_BREAK comando (Mmsystem.h)
description: Il comando MCI \_ BREAK imposta una chiave di interruzione per un dispositivo MCI. MCI supporta questo comando direttamente anziché passarlo al dispositivo. Qualsiasi applicazione MCI può usare questo comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK comando Windows Multimedia
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
ms.openlocfilehash: 07006ddfb38e1a57f6e08cb73d9b33021d139b9542245aec137e0969378140e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803970"
---
# <a name="mci_break-command"></a>Comando MCI \_ BREAK

Il comando MCI \_ BREAK imposta una chiave di interruzione per un dispositivo MCI. MCI supporta questo comando direttamente anziché passarlo al dispositivo. Qualsiasi applicazione MCI può usare questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI NOTIFY, MCI WAIT o, per i dispositivi di registrazione video e \_ \_ videocassetta (VCR), MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Puntatore a [**una struttura MCI \_ BREAK \_ PARMS.**](mci-break-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Potrebbe essere necessario premere il tasto di interruzione più volte per interrompere un'operazione di attesa. Premendo il tasto di interruzione dopo l'annullamento di un'attesa del dispositivo, è possibile inviare l'interruzione a un'applicazione. Se un'applicazione ha un'azione definita per il codice della chiave virtuale, può rispondere inavvertitamente all'interruzione. Ad esempio, un'applicazione che usa VK CANCEL per un tasto di scelta rapida può rispondere al tasto CTRL+BREAK predefinito se viene premuto dopo l'annullamento di \_ un'attesa.

I flag aggiuntivi seguenti si applicano a tutti i dispositivi:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND
</dt> <dd>

Il **membro hwndBreak** della struttura identificata da *lpBreak* contiene un handle di finestra che deve essere la finestra corrente per abilitare il rilevamento delle interruzioni per il dispositivo MCI. Si tratta in genere della finestra principale dell'applicazione. Se omesso, MCI non controlla l'handle di finestra della finestra corrente.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>TASTO DI \_ INTERRUZIONE \_ MCI
</dt> <dd>

Il **membro nVirtKey** della struttura identificata da *lpBreak* specifica il codice della chiave virtuale usato per la chiave di interruzione. Per impostazione predefinita, MCI assegna CTRL+BREAK come tasto di interruzione. Questo flag è obbligatorio se non viene specificato MCI \_ BREAK \_ OFF.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>INTERRUZIONE \_ MCI \_
</dt> <dd>

Disabilita qualsiasi tasto di interruzione esistente per il dispositivo indicato.

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

 

