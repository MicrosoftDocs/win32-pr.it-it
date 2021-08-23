---
title: MCI_REALIZE comando (Mmsystem.h)
description: Il comando MCI \_ REALIZE fa sì che un dispositivo grafico si renda conto della tavolozza in un contesto di dispositivo (DC). I dispositivi video digitali riconoscono questo comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81204fe679d543438a0d0dcc7ec333462cb6a3d0c30212706969dc22a143df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689831"
---
# <a name="mci_realize-command"></a>Comando MCI \_ REALIZE

Il comando MCI \_ REALIZE fa sì che un dispositivo grafico si renda conto della tavolozza in un contesto di dispositivo (DC). I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

**MCI \_ NOTIFY,** **MCI \_ WAIT** o, per i dispositivi digital-video, **MCI \_ TEST**. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

È consigliabile usare questo comando quando l'applicazione riceve il [**messaggio WM \_ QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette)

I flag aggiuntivi seguenti vengono usati con il tipo di dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ REALIZE \_ BKGD
</dt> <dd>

La tavolozza viene visualizzata come tavolozza di sfondo.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV \_ REALIZE \_ NORM
</dt> <dd>

Realizza normalmente la tavolozza. Questo è il valore predefinito.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpRealize* punta a una **struttura \_ \_ PARMS MCI REALIZE.** Per altre informazioni, vedere i commenti nella [**struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md)

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

 

