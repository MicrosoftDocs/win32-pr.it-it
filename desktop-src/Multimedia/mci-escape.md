---
title: Comando MCI_ESCAPE (mmsystem. h)
description: Il \_ comando di escape MCI invia una stringa direttamente al dispositivo. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Comando MCI_ESCAPE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301758"
---
# <a name="mci_escape-command"></a>\_Comando di escape MCI

Il \_ comando di escape MCI invia una stringa direttamente al dispositivo. I dispositivi videodisco riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
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

<span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri di escape MCI VD**](mci-vd-escape-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I dati inviati con l' \_ escape MCI sono dipendenti dal dispositivo e vengono in genere passati direttamente all'hardware associato al dispositivo.

Il flag aggiuntivo seguente si applica ai dispositivi videodisco:

<dl> <dt>

<span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_stringa di \_ escape MCI VD \_
</dt> <dd>

Una stringa di comando viene specificata nel membro **lpstrCommand** della struttura identificata da *lpEscape*. Questo flag è obbligatorio.

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

 

