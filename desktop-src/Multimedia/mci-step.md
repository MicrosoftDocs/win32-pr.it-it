---
title: Comando MCI_STEP (mmsystem. h)
description: Il \_ comando del passaggio MCI segue il lettore di uno o più frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Comando MCI_STEP Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118951"
---
# <a name="mci_step-command"></a>\_Comando del passaggio MCI

Il \_ comando del passaggio MCI segue il lettore di uno o più frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando supporta i dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ con \_ il flag video del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ frame passaggio DGV \_ MCI
</dt> <dd>

Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da anticipare prima di visualizzare un'altra immagine.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>DGV di MCI- \_ \_ passaggio \_ inverso
</dt> <dd>

Passaggi in ordine inverso.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpStep* punta a una [**struttura \_ DGV \_ Step \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_ \_ frame passaggio VCR \_ MCI
</dt> <dd>

Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da anticipare prima di visualizzare un'altra immagine.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_ \_ passaggio \_ inverso del videoregistratore MCI
</dt> <dd>

Passaggi in ordine inverso.

</dd> </dl>

Per i dispositivi VCR, il parametro *lpStep* punta a una struttura [**\_ \_ \_ parametri del passaggio VCR MCI**](mci-vcr-step-parms.md) .

Con il tipo di dispositivo **videodisco** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>frame di passaggio di MCI \_ VD \_ \_
</dt> <dd>

Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da scorrere.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>il \_ passaggio di MCI VD è \_ \_ inverso
</dt> <dd>

Passaggi in ordine inverso.

</dd> </dl>

Per i dispositivi videodisco, il parametro *lpStep* punta a una struttura [**parametri del passaggio di MCI \_ VD \_ \_**](mci-vd-step-parms.md) .

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

 

