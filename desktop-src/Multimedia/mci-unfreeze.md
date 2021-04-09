---
title: Comando MCI_UNFREEZE (mmsystem. h)
description: Il \_ comando MCI Unfreeze ripristina il movimento in un'area del buffer video bloccata con il \_ comando di blocco MCI. I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Comando MCI_UNFREEZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121259"
---
# <a name="mci_unfreeze-command"></a>\_Comando di UNFREEZE MCI

Il \_ comando MCI Unfreeze ripristina il movimento in un'area del buffer video bloccata con il comando di [ \_ blocco MCI](mci-freeze.md) . I dispositivi Digital-video, VCR e overlay video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **digitalvideo** :

DGV di MCI \_ \_

Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Il rettangolo specifica un'area all'interno del buffer dei frame i cui pixel dovrebbero avere il bit di maschera di blocco disattivato. Le aree rettangolari vengono specificate come descritto per il comando [MCI \_ put](mci-put.md) . Se omesso, il rettangolo viene impostato sull'intero buffer del frame. Utilizzando una sequenza di comandi Freeze e Unfreeze con rettangoli diversi, è possibile descrivere modelli arbitrari di bit della maschera di blocco.

Per i dispositivi digitali video, il parametro *lpUnfreeze* punta a una **struttura \_ DGV \_ decongelata MCI \_ parametri** . Per ulteriori informazioni, vedere i commenti per la [**struttura \_ DGV \_ Rect \_ parametri di MCI**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_ \_ input sbloccare VCR MCI \_
</dt> <dd>

Sbloccare l'input.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_output di \_ sbloccaggio \_ VCR MCI
</dt> <dd>

Sbloccare l'output.

</dd> </dl>

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Parametro obbligatorio.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpUnfreeze* punta a una struttura [**\_ OVLY \_ Rect \_ parametri di MCI**](mci-ovly-rect-parms.md) .

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

 

