---
title: MCI_FREEZE comando (Mmsystem.h)
description: Il comando MCI \_ FREEZE blocca il movimento sullo schermo. I dispositivi digital-video, video-overlay e VCR riconoscono questo comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE comando Windows Multimedia
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
ms.openlocfilehash: dc0d57daaa488d70654b946115264fc2177b959f73cbbcee1759bd6823bfaf4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986662"
---
# <a name="mci_freeze-command"></a>Comando MCI \_ FREEZE

Il comando MCI \_ FREEZE blocca il movimento sullo schermo. I dispositivi digital-video, video-overlay e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con parametri aggiuntivi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti vengono usati dal **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>BLOCCO DI MCI \_ DGV \_ \_ IN
</dt> <dd>

Il **membro rc** della struttura identificata da *lpFreeze* contiene un rettangolo valido. Il rettangolo specifica un'area all'interno del buffer dei frame in cui il bit della maschera di blocco per ogni pixel è attivato. I pixel specificati non verranno aggiornati fino a quando il bit della maschera di blocco non viene disattivato. Se questo flag non viene specificato, il rettangolo viene impostato per impostazione predefinita sull'intero buffer dei frame. Questo flag è supportato solo se il [comando MCI \_ GETDEVCAPS](mci-getdevcaps.md) restituisce **TRUE** per il flag MCI \_ DGV \_ GETDEVCAPS \_ CAN \_ LOCK.

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>BLOCCO \_ DGV MCI \_ \_ ALL'ESTERNO
</dt> <dd>

L'area esterna all'area specificata per il flag MCI \_ DGV \_ FREEZE AT è \_ bloccata.

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpFreeze* punta a una [**struttura MCI \_ DGV \_ FREEZE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)

I flag aggiuntivi seguenti vengono usati dal tipo **di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>CAMPO DI BLOCCO \_ DEL VCR \_ \_ MCI
</dt> <dd>

Bloccare un solo membro del frame corrente.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>FRAME DI BLOCCO \_ DEL VCR MCI \_ \_
</dt> <dd>

Bloccare entrambi i campi del frame corrente.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>INPUT DI BLOCCO \_ DEL VCR MCI \_ \_
</dt> <dd>

Bloccare il frame corrente sullo schermo (usato per la registrazione).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>OUTPUT DI BLOCCO \_ DEL VCR MCI \_ \_
</dt> <dd>

Bloccare il frame corrente dal videoregistratore (usato con l'acquisizione di frame).

</dd> </dl>

Per i dispositivi VCR, il *parametro lpFreeze* punta a una [**struttura MCI GENERIC \_ \_ PARMS.**](mci-generic-parms.md)

Il flag aggiuntivo seguente viene usato dal tipo **di dispositivo di** sovrimpressione:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpFreeze* contiene un rettangolo valido. Se questo flag non viene specificato, il driver di dispositivo blocca l'intero frame.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpFreeze* punta a una [**struttura PARMS MCI \_ OVLY \_ RECT. \_**](mci-ovly-rect-parms.md)

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

 

