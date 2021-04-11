---
title: Comando MCI_INDEX (mmsystem. h)
description: Il \_ comando MCI index attiva o disattiva la visualizzazione sullo schermo. I dispositivi VCR riconoscono questo comando.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- Comando MCI_INDEX Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121454"
---
# <a name="mci_index-command"></a>\_Comando di indice MCI

Il \_ comando MCI index attiva o disattiva la visualizzazione sullo schermo. I dispositivi VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
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

<span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Le informazioni visualizzate nella schermata sullo schermo sono controllate dal \_ flag MCI VCR \_ set \_ index nel comando [ \_ set di MCI](mci-set.md) .

I seguenti flag aggiuntivi si applicano ai dispositivi VCR:

<dl> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Attiva la visualizzazione sullo schermo.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Attiva la visualizzazione sullo schermo.

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

 

