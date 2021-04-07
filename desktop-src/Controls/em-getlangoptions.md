---
title: Messaggio di EM_GETLANGOPTIONS (RichEdit. h)
description: Ottiene le impostazioni delle opzioni di un controllo Rich Edit per l'IME (Input Method Editor) e il supporto per la lingua asiatica.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- Controlli di Windows Message EM_GETLANGOPTIONS
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27254ccb10093059eb9161410f4e25efdc59306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873393"
---
# <a name="em_getlangoptions-message"></a>\_Messaggio GETLANGOPTIONS em

Ottiene le impostazioni delle opzioni di un controllo Rich Edit per l'IME (Input Method Editor) e il supporto per la lingua asiatica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le impostazioni della lingua asiatica e IME, che possono essere pari a zero o più dei valori seguenti.



| Codice restituito                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**tipo di carattere autoil FMI \_**</dt> </dl>                    | Se questo flag è impostato, il controllo modifica automaticamente i tipi di carattere quando l'utente cambia in modo esplicito in un layout di tastiera diverso. È utile disattivare il tipo di **carattere del FMI \_ AutoFont** per i tipi di carattere Unicode universali. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**\_AUTOFONTSIZEADJUST FMI**</dt> </dl>          | Se questo flag è impostato, il controllo Ridimensiona le dimensioni del tipo di carattere associato al carattere dalle dimensioni del punto di inserimento in base allo script. Ad esempio, i tipi di carattere asiatici sono leggermente più grandi di quelli occidentali. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**\_tastiera autotastiera FMI**</dt> </dl>                | Se questo flag è impostato, il controllo modifica automaticamente il layout di tastiera quando l'utente cambia in modo esplicito in un tipo di carattere diverso o quando l'utente modifica in modo esplicito il punto di inserimento in una nuova posizione nel testo. Verrà attivato automaticamente per i controlli bidirezionali. Per tutti gli altri controlli, è disattivato per impostazione predefinita. Per impostazione predefinita, questa opzione è disattivata (0).<br/>                                 |
| <dl> <dt>**\_DISABLEAUTOBIDIAUTOKEYBOARD FMI**</dt> </dl> | **Windows 8**: se questo flag è impostato, il controllo Usa la logica indipendente dalla lingua per il cambio automatico della tastiera. Per impostazione predefinita, questa opzione è disattivata (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_DUALFONT FMI**</dt> </dl>                    | Se questo flag è impostato, il controllo Usa la modalità Dual font. Usato per il supporto della lingua asiatica. Il controllo Usa un tipo di carattere inglese per il testo ASCII e un carattere asiatico per il testo asiatico. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**\_IMEALWAYSSENDNOTIFY FMI**</dt> </dl>         | Questo flag controlla il modo in cui il controllo Rich Edit invia una notifica al client durante la composizione IME: <br/> 0: nessuna [notifica \_ en](en-change.md) o [ \_ selChange](en-selchange.md) durante lo stato non determinato. Invia una notifica quando viene ricevuta la stringa finale. Questo è il valore predefinito.<br/> 1: invia gli eventi [en \_ Change](en-change.md) e [en \_ selChange](en-selchange.md) durante lo stato non determinato.<br/> |
| <dl> <dt>**\_IMECANCELCOMPLETE FMI**</dt> </dl>           | Questo flag determina il modo in cui il controllo utilizza la stringa di composizione di un IME se viene annullata dall'utente. Se questo flag è impostato, il controllo elimina la stringa di composizione. Se questo flag non è impostato, il controllo utilizza la stringa di composizione come stringa risultante. Per impostazione predefinita, questa opzione è disattivata (0).<br/>                                                                                                              |
| <dl> <dt>**\_NOIMPLICITLANG FMI**</dt> </dl>              | **Windows 8**: se questo flag è impostato, disabilitare il timbro dell'input della tastiera con la lingua della tastiera e verificare che le IDSS della lingua asiatica non orientale siano compatibili con il repertorio di caratteri. Per impostazione predefinita, questa opzione è disattivata (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**\_NOKBDLIDFIXUP FMI**</dt> </dl>               | **Windows 8**: se questo flag è impostato, il controllo Rich Edit Disabilita la lingua della tastiera di stampa su un controllo vuoto. Per impostazione predefinita, questa opzione è disattivata (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_controllo ortografico FMI**</dt> </dl>               | **Windows 8**: se questo flag è impostato, il controllo Rich Edit attiva il controllo ortografico. Per impostazione predefinita, questa opzione è disattivata (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_TKBAUTOCORRECTION FMI**</dt> </dl>           | **Windows 8**: se questo flag è impostato, abilitare la correzione automatica della tastiera tocco. Per impostazione predefinita, questa opzione è disattivata (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**\_TKBPREDICTION FMI**</dt> </dl>               | **Windows 10**: ignorato.<br/> **Windows 8**: se questo flag è impostato, il controllo Rich Edit Abilita la stima della tastiera touch. Per impostazione predefinita, questa opzione è disattivata (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**\_UIFONTS FMI**</dt> </dl>                     | Usare i tipi di carattere predefiniti dell'interfaccia utente. Per impostazione predefinita, questa opzione è disattivata (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, viene impostato il flag del **\_ tipo di carattere** autoil FMI. Per impostazione predefinita, i flag **FMI \_ autokeyboard** e **FMI \_ IMECANCELCOMPLETE** sono cancellati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETLANGOPTIONS em**](em-setlangoptions.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





