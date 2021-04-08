---
title: Comando MCI_FREEZE (mmsystem. h)
description: Il \_ comando di blocco MCI blocca il movimento sullo schermo. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Comando MCI_FREEZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048058"
---
# <a name="mci_freeze-command"></a>\_Comando blocca MCI

Il \_ comando di blocco MCI blocca il movimento sullo schermo. I dispositivi Digital-video, video-overlay e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti vengono usati dal tipo di dispositivo **digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_blocco DGV \_ MCI \_ in
</dt> <dd>

Il membro **RC** della struttura identificato da *lpFreeze* contiene un rettangolo valido. Il rettangolo specifica un'area all'interno del buffer del frame che avrà il bit della maschera di blocco per ogni pixel attivato. I pixel specificati non verranno aggiornati finché il bit della maschera di blocco non viene disattivato. Se questo flag non è specificato, il rettangolo viene impostato sull'intero buffer del frame. Questo flag è supportato solo se il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) restituisce **true** per il \_ flag MCI DGV \_ GETDEVCAPS \_ can \_ Lock.

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>\_blocco DGV \_ MCI \_ esterno
</dt> <dd>

L'area al di fuori dell'area specificata per il \_ flag di blocco DGV del MCI \_ \_ è bloccata.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpFreeze* punta a una [**struttura \_ DGV \_ Freeze \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .

I flag aggiuntivi seguenti vengono usati dal tipo di dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_ \_ campo blocco videoregistratore \_ MCI
</dt> <dd>

Blocca solo un membro del frame corrente.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_frame di \_ blocco \_ VCR MCI
</dt> <dd>

Blocca entrambi i campi del frame corrente.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_ \_ input blocco VCR \_ MCI
</dt> <dd>

Blocca il frame corrente sullo schermo (usato per la registrazione).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_ \_ output blocco VCR \_ MCI
</dt> <dd>

Blocca il frame corrente dal VCR (usato con l'acquisizione dei frame).

</dd> </dl>

Per i dispositivi VCR, il parametro *lpFreeze* punta a una struttura [**\_ \_ parametri generica MCI**](mci-generic-parms.md) .

Il flag aggiuntivo seguente viene usato dal tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpFreeze* contiene un rettangolo valido. Se questo flag non è specificato, il driver di dispositivo blocca l'intero frame.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpFreeze* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .

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

 

