---
title: Comando MCI_SYSINFO (mmsystem. h)
description: Il \_ comando MCI sysinfo recupera informazioni sui dispositivi MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Comando MCI_SYSINFO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964329"
---
# <a name="mci_sysinfo-command"></a>\_Comando MCI sysinfo

Il \_ comando MCI sysinfo recupera informazioni sui dispositivi MCI. MCI supporta direttamente questo comando anziché passarlo al dispositivo. Qualsiasi applicazione MCI può utilizzare questo comando. Le informazioni sulla stringa vengono restituite nel buffer fornito dall'applicazione a cui fa riferimento il membro **lpstrReturn** della struttura identificata da *lpSysInfo*. Le informazioni numeriche vengono restituite come valore **DWORD** inserito nel buffer fornito dall'applicazione. Il membro **dwRetSize** specifica la lunghezza del buffer.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
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

Uno o più dei seguenti flag standard e specifici del comando:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>installazione di MCI \_ sysinfo \_
</dt> <dd>

Ottiene il nome (elencato nel registro di sistema o il file di SYSTEM.INI) usato per installare il dispositivo.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nome della sysinfo MCI \_
</dt> <dd>

Ottiene un nome di dispositivo corrispondente al numero di dispositivo specificato nel membro **dwNumber** della struttura identificata da **lpSysInfo**. Se il \_ \_ flag di apertura di MCI sysinfo è impostato, MCI restituisce i nomi dei dispositivi aperti.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>apertura di MCI \_ sysinfo \_
</dt> <dd>

Ottiene la quantità o il nome dei dispositivi aperti.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantità sysinfo \_ MCI
</dt> <dd>

Ottiene il numero di dispositivi del tipo specificato elencati nel registro di sistema o nella \[ \] sezione MCI del file di SYSTEM.INI. Se \_ \_ è impostato il flag di apertura di MCI sysinfo, viene restituito il numero di dispositivi aperti.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri di MCI sysinfo**](mci-sysinfo-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il membro **wDeviceType** della struttura identificata da *lpSysInfo* viene usato per indicare il tipo di dispositivo della query. Se il parametro *wDeviceID* è impostato su MCI \_ All \_ Device \_ ID, viene eseguito l'override del valore di **wDeviceType**. Per un elenco dei tipi di dispositivo, vedere [tipi di dispositivo MCI](mci-device-types.md).

I valori restituiti integer sono valori **DWORD** restituiti nel buffer a cui punta il membro **lpstrReturn** della struttura identificata da *lpSysInfo*.

I valori restituiti dalla stringa sono stringhe con terminazione null restituite nel buffer a cui punta il membro **lpstrReturn** della struttura identificata da *lpSysInfo*.

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

 

