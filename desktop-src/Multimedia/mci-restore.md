---
title: Comando MCI_RESTORE (mmsystem. h)
description: Il \_ comando di ripristino MCI copia una bitmap da un file nel buffer dei frame. I dispositivi digitali video riconoscono questo comando. Questo comando esegue l'azione opposta del \_ comando di acquisizione MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Comando MCI_RESTORE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742810"
---
# <a name="mci_restore-command"></a>\_Comando di ripristino MCI

Il \_ comando di ripristino MCI copia una bitmap da un file nel buffer dei frame. I dispositivi digitali video riconoscono questo comando. Questo comando esegue l'azione opposta del comando di [ \_ acquisizione MCI](mci-capture.md) .

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

Puntatore a una [**struttura \_ \_ \_ parametri DGV Restore MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

L'implementazione di è in grado di riconoscere diversi formati di immagine, ma viene sempre accettata una bitmap indipendente dal dispositivo (DIB) Windows.

I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ ripristino di MCI DGV \_ da
</dt> <dd>

Il membro **lpstrFileName** della struttura identificata da *lpRestore* contiene un indirizzo di un buffer contenente il nome del file di origine. Il nome file è obbligatorio.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ripristino DGV \_ MCI \_ in
</dt> <dd>

Il membro **RC** della struttura identificato da *lpRestore* contiene un rettangolo valido. Il rettangolo specifica un'area del buffer del frame rispetto all'origine. La prima coppia di coordinate specifica l'angolo superiore sinistro del rettangolo. la seconda coppia specifica la larghezza e l'altezza. Se questo flag non è specificato, l'immagine viene copiata nell'angolo superiore sinistro del buffer del frame.

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

 

