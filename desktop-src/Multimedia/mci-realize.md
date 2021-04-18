---
title: Comando MCI_REALIZE (mmsystem. h)
description: Il \_ comando MCI realizz fa in modo che un dispositivo grafico realizzi la propria tavolozza in un contesto di dispositivo (DC). I dispositivi digitali video riconoscono questo comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Comando MCI_REALIZE Windows Multimedia
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
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301465"
---
# <a name="mci_realize-command"></a>\_Comando MCI realizz

Il \_ comando MCI realizz fa in modo che un dispositivo grafico realizzi la propria tavolozza in un contesto di dispositivo (DC). I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ NOTIFICA**, **MCI \_ wait** o, per i dispositivi video digitali, **MCI \_ test**. Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Usare questo comando quando l'applicazione riceve il messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .

Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ realizza \_ bkgd
</dt> <dd>

Realizza la tavolozza come tavolozza di sfondo.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>norma per la realizzazione di MCI \_ DGV \_ \_
</dt> <dd>

Realizza la tavolozza normalmente. Questo è il valore predefinito.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpRealize* punta a una **struttura \_ \_ parametri** per la realizzazione di un MCI. Per ulteriori informazioni, vedere la pagina relativa ai commenti nella struttura [**\_ \_ parametri generica MCI**](mci-generic-parms.md) .

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

 

