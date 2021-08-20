---
title: MCI_SAVE comando (Mmsystem.h)
description: Il comando MCI \_ SAVE salva il file corrente.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd34603e6563e5f76995a8380b88f37424dd9cbd3da024ad491d184dc33aa2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803425"
---
# <a name="mci_save-command"></a>Comando MCI \_ SAVE

Il comando MCI \_ SAVE salva il file corrente. I dispositivi che modificano i file non devono eliminare la copia originale finché non ricevono il messaggio di salvataggio. I dispositivi video-overlay e waveform-audio riconoscono questo comando. Anche se anche i dispositivi video digitali e i sequencer MIDI riconoscono questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Puntatore a [**una struttura MCI \_ SAVE \_ PARMS.**](mci-save-parms.md) I dispositivi con parametri aggiuntivi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando è supportato dai dispositivi che restituiscono **TRUE** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con il flag CAN SAVE DI MCI \_ GETDEVCAPS. \_ \_

Il flag aggiuntivo seguente si applica a tutti i dispositivi che [supportano MCI \_ SAVE:](/windows)

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>FILE DI \_ SALVATAGGIO MCI \_
</dt> <dd>

Il **membro lpfilename** della struttura identificata da *lpSave* contiene un indirizzo di un buffer contenente il nome file di destinazione.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpSave* contiene un rettangolo valido. Il rettangolo specifica un'area del buffer dei frame che verrà salvata nel file specificato. La prima coppia di coordinate specifica l'angolo superiore sinistro del rettangolo. la seconda coppia specifica la larghezza e l'altezza. I dispositivi digital-video devono usare [il comando MCI \_ CAPTURE](mci-capture.md) per acquisire il contenuto del buffer frame. (Anche i dispositivi con sovrapposizione video devono usare MCI \_ CAPTURE. Questo flag è per la compatibilità con il set di comandi di sovrapposizione video MCI esistente.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI \_ DGV \_ SAVE \_ ABORT
</dt> <dd>

Arresta un'operazione di salvataggio in corso. Deve essere l'unico flag presente.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ SAVE \_ KEEPRESERVE
</dt> <dd>

Lo spazio su disco inutilizzato rimanente dal comando [MCI \_ RESERVE](mci-reserve.md) originale non viene deallocato.

</dd> </dl>

Per i dispositivi digital-video, il *parametro lpSave* punta a una [**struttura MCI \_ DGV \_ SAVE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)

Il flag aggiuntivo seguente viene usato con il **tipo di dispositivo overlay:**

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Il **membro rc** della struttura identificata da *lpSave* contiene un rettangolo di visualizzazione valido che indica l'area del buffer video da salvare.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il *parametro lpSave* punta a una [**struttura MCI \_ OVLY \_ SAVE \_ PARMS.**](/previous-versions//dd743447(v=vs.85))

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

 

