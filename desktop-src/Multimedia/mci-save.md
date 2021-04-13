---
title: Comando MCI_SAVE (mmsystem. h)
description: Il \_ comando MCI Save Salva il file corrente.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Comando MCI_SAVE Windows Multimedia
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
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475694"
---
# <a name="mci_save-command"></a>\_Comando di salvataggio MCI

Il \_ comando MCI Save Salva il file corrente. I dispositivi che modificano i file non devono eliminare definitivamente la copia originale fino a quando non ricevono il messaggio di salvataggio. Video-overlay e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Puntatore a una struttura di [**\_ salvataggio \_ parametri di MCI**](mci-save-parms.md) . I dispositivi con parametri aggiuntivi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con MCI \_ GETDEVCAPS \_ can \_ Save flag.

Il flag aggiuntivo seguente si applica a tutti i dispositivi che supportano [MCI \_ Save](/windows):

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_file di salvataggio MCI \_
</dt> <dd>

Il membro **lpFileName** della struttura identificata da *lpSave* contiene un indirizzo di un buffer contenente il nome file di destinazione.

</dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpSave* contiene un rettangolo valido. Il rettangolo specifica un'area del buffer del frame che verrà salvata nel file specificato. La prima coppia di coordinate specifica l'angolo superiore sinistro del rettangolo. la seconda coppia specifica la larghezza e l'altezza. I dispositivi digitali video devono usare il comando di [ \_ acquisizione MCI](mci-capture.md) per acquisire il contenuto del buffer dei frame. (I dispositivi overlay video devono usare anche MCI \_ ACQUISISCi.) Questo flag è per la compatibilità con il set di comandi video-overlay di MCI esistente.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_interruzione del \_ salvataggio \_ DGV MCI
</dt> <dd>

Arresta un'operazione di salvataggio in corso. Deve essere l'unico flag presente.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>\_KEEPRESERVE DGV per il \_ salvataggio di MCI \_
</dt> <dd>

Lo spazio inutilizzato su disco rimasto dal comando [di \_ riserva MCI](mci-reserve.md) originale non viene deallocato.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpSave* punta a una [**struttura \_ DGV \_ Save \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **overlay** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>OVLY di MCI \_ \_
</dt> <dd>

Il membro **RC** della struttura identificato da *lpSave* contiene un rettangolo di visualizzazione valido che indica l'area del buffer video da salvare.

</dd> </dl>

Per i dispositivi con sovrimpressione video, il parametro *lpSave* punta a una struttura [**\_ OVLY \_ Save \_ parametri di MCI**](/previous-versions//dd743447(v=vs.85)) .

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

 

