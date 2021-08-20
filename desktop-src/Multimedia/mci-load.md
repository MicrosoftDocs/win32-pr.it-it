---
title: MCI_LOAD comando (Mmsystem.h)
description: Il comando MCI \_ LOAD carica un file. I dispositivi digital-video e video-overlay riconoscono questo comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD comando Windows Multimedia
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
ms.openlocfilehash: e318e79bf24e51fec69f97a0dcb56395cb1a8917a31105deae062a865169b778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138539"
---
# <a name="mci_load-command"></a>Comando MCI \_ LOAD

Il comando MCI \_ LOAD carica un file. I dispositivi digital-video e video-overlay riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi video digitali, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Puntatore a [**una struttura MCI \_ LOAD \_ PARMS.**](mci-load-parms.md) I dispositivi con parametri aggiuntivi potrebbero sostituire questa struttura con una struttura specifica del dispositivo. Per i dispositivi video digitali, il **parametro lpLoad** punta a una [**struttura MCI \_ DGV \_ LOAD \_ PARMS.**](/previous-versions//dd743391(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il flag aggiuntivo seguente si applica a tutti i dispositivi che supportano MCI \_ LOAD:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>FILE DI CARICAMENTO MCI \_ \_
</dt> <dd>

Il **membro lpfilename** della struttura identificata da *lpLoad* contiene un indirizzo di un buffer contenente il nome file.

</dd> </dl>

Il flag aggiuntivo seguente viene usato con il **tipo di dispositivo overlay:**

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpLoad* contiene un rettangolo di visualizzazione valido che identifica l'area del buffer video da aggiornare.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il *parametro lpLoad* punta a una [**struttura MCI \_ OVLY \_ LOAD \_ PARMS.**](mci-ovly-load-parms.md)

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

 

