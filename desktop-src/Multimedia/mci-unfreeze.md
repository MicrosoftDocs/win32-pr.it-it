---
title: MCI_UNFREEZE comando (Mmsystem.h)
description: Il comando MCI UNFREEZE ripristina il movimento in un'area del buffer video bloccato \_ con il comando MCI \_ FREEZE. Questo comando viene riconosciuto da dispositivi video digitali, videoregistratori e sovrimpressione video.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE comando Windows Multimedia
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
ms.openlocfilehash: 3011f3d2c05c304b37957c6f4cb78f2ada9389ab727a7af63a358fd4b5afdd3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525571"
---
# <a name="mci_unfreeze-command"></a>Comando MCI \_ UNFREEZE

Il comando MCI UNFREEZE ripristina il movimento in un'area del buffer video bloccato \_ con [il comando MCI \_ FREEZE.](mci-freeze.md) Questo comando viene riconosciuto da dispositivi video digitali, videoregistratori e sovrimpressione video.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Puntatore a [**una struttura MCI \_ GENERIC \_ PARMS.**](mci-generic-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il flag aggiuntivo seguente viene usato con il **tipo di dispositivo digitalvideo:**

MCI \_ DGV \_ RECT

Il **membro rc** della struttura identificata da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Il rettangolo specifica un'area all'interno del buffer dei frame i cui pixel devono avere il bit della maschera di blocco disattivato. Le aree rettangolari vengono specificate come descritto per [il comando MCI \_ PUT.](mci-put.md) Se omesso, il rettangolo viene utilizzato per impostazione predefinita per l'intero buffer dei frame. Usando una sequenza di comandi freeze e unfreeze con rettangoli diversi, è possibile illustrare modelli arbitrari di bit della maschera di blocco.

Per i dispositivi video digitali, il *parametro lpUnfreeze* punta a una **struttura MCI \_ DGV \_ UNFREEZE \_ PARMS.** Per altre informazioni, vedere i commenti per la [**struttura MCI \_ DGV \_ RECT \_ PARMS.**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR \_ UNFREEZE \_ INPUT
</dt> <dd>

Sbloccare l'input.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR \_ UNFREEZE \_ OUTPUT
</dt> <dd>

Sbloccare l'output.

</dd> </dl>

Il flag aggiuntivo seguente viene usato con il **tipo di dispositivo overlay:**

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpUnfreeze* contiene un rettangolo di visualizzazione valido. Parametro obbligatorio.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpUnfreeze* punta a una [**struttura PARMS MCI \_ OVLY \_ RECT. \_**](mci-ovly-rect-parms.md)

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

 

