---
title: Comando MCI_LOAD (mmsystem. h)
description: Il \_ comando MCI Load carica un file. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Comando MCI_LOAD Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963745"
---
# <a name="mci_load-command"></a>\_Comando di caricamento MCI

Il \_ comando MCI Load carica un file. I dispositivi digitali con sovrimpressione video e video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri di caricamento MCI**](mci-load-parms.md) . I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo. Per i dispositivi digitali video, il parametro **lpLoad** punta a una [**struttura \_ DGV \_ Load \_ parametri di MCI**](/previous-versions//dd743391(v=vs.85)) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il flag aggiuntivo seguente si applica a tutti i dispositivi che supportano il \_ carico MCI:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_file di caricamento MCI \_
</dt> <dd>

Il membro **lpFileName** della struttura identificata da *lpLoad* contiene un indirizzo di un buffer contenente il nome del file.

</dd> </dl>

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpLoad* contiene un rettangolo di visualizzazione valido che identifica l'area del buffer video da aggiornare.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpLoad* punta a una struttura [**\_ OVLY \_ Load \_ parametri di MCI**](mci-ovly-load-parms.md) .

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

 

