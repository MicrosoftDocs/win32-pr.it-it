---
title: EM_GETLANGOPTIONS messaggio (Richedit.h)
description: Ottiene le impostazioni delle opzioni di un controllo Rich Edit per Input Method Editor (IME) e il supporto delle lingue asiatiche.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS di controllo Windows messaggio
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
ms.openlocfilehash: a6e3fa3602259ff0b754c79c69d91048c68c60b2703d4cd06a7da4630fcdf646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800201"
---
# <a name="em_getlangoptions-message"></a>Messaggio \_ EM GETLANGOPTIONS

Ottiene le impostazioni delle opzioni di un controllo Rich Edit per Input Method Editor (IME) e il supporto delle lingue asiatiche.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le impostazioni della lingua IME e dell'Asia, che possono essere zero o più dei valori seguenti.



| Codice restituito                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**IMF \_ AUTOFONT**</dt> </dl>                    | Se questo flag è impostato, il controllo modifica automaticamente i tipi di carattere quando l'utente cambia in modo esplicito in un layout di tastiera diverso. È utile disattivare **IMF \_ AUTOFONT** per i tipi di carattere Unicode universali. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**IMF \_ AUTOFONTSIZEADJUST**</dt> </dl>          | Se questo flag è impostato, il controllo ridimensiona le dimensioni del carattere associate al tipo di carattere dalla dimensione del punto di inserimento in base allo script. Ad esempio, i tipi di carattere asiatici sono leggermente più grandi di quelli occidentali. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**IMF \_ AUTOKEYBOARD**</dt> </dl>                | Se questo flag è impostato, il controllo modifica automaticamente il layout della tastiera quando l'utente cambia in modo esplicito in un tipo di carattere diverso o quando l'utente modifica in modo esplicito il punto di inserimento in una nuova posizione nel testo. Verrà attivato automaticamente per i controlli bidirezionali. Per tutti gli altri controlli, è disattivato per impostazione predefinita. Questa opzione è disattivata per impostazione predefinita (0).<br/>                                 |
| <dl> <dt>**IMF \_ DISABLEAUTOBIDIAUTOKEYBOARD**</dt> </dl> | **Windows 8:** se questo flag è impostato, il controllo usa la logica indipendente dalla lingua per il cambio automatico della tastiera. Questa opzione è disattivata per impostazione predefinita (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**IMF \_ DUALFONT**</dt> </dl>                    | Se questo flag è impostato, il controllo usa la modalità a doppio carattere. Usato per il supporto delle lingue asiatiche. Il controllo usa un tipo di carattere inglese per il testo ASCII e un tipo di carattere asiatico per il testo in lingue asiatiche. Questa opzione è attivata per impostazione predefinita (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMF \_ IMEALWAYSSENDNOTIFY**</dt> </dl>         | Questo flag controlla il modo in cui il controllo Rich Edit invia una notifica al client durante la composizione IME: <br/> 0: nessuna [notifica EN \_ CHANGE](en-change.md) o [EN \_ SELCHANGE](en-selchange.md) durante lo stato non determinato. Inviare una notifica quando entra in servizio la stringa finale. Questo è il valore predefinito.<br/> 1: Inviare [eventi EN \_ CHANGE](en-change.md) [ed EN \_ SELCHANGE](en-selchange.md) durante uno stato non determinato.<br/> |
| <dl> <dt>**IMF \_ IMECANCELCOMPLETE**</dt> </dl>           | Questo flag determina in che modo il controllo usa la stringa di composizione di un IME se l'utente lo annulla. Se questo flag è impostato, il controllo elimina la stringa di composizione. Se questo flag non è impostato, il controllo utilizza la stringa di composizione come stringa risultante. Questa opzione è disattivata per impostazione predefinita (0).<br/>                                                                                                              |
| <dl> <dt>**IMF \_ NOIMPLICITLANG**</dt> </dl>              | **Windows 8**: se questo flag è impostato, disabilitare la stampa dell'input della tastiera con la lingua della tastiera e assicurarsi che gli ID lingua non dell'Asia orientale siano compatibili con il carattere . Questa opzione è disattivata per impostazione predefinita (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**IMF \_ NOKBDLIDFIXUP**</dt> </dl>               | **Windows 8:** se questo flag è impostato, il controllo Rich Edit disabilita la lingua della tastiera in un controllo vuoto. Questa opzione è disattivata per impostazione predefinita (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**CONTROLLO \_ ORTOGRAFICO IMF**</dt> </dl>               | **Windows 8:** se questo flag è impostato, il controllo Rich Edit attiva il controllo ortografico. Questa opzione è disattivata per impostazione predefinita (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**IMF \_ TKBAUTOCORRECTION**</dt> </dl>           | **Windows 8:** se questo flag è impostato, abilitare la correzione automatica della tastiera virtuale. Questa opzione è disattivata per impostazione predefinita (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**FMI \_ TKBPREDICTION**</dt> </dl>               | **Windows 10**: ignorato.<br/> **Windows 8:** se questo flag è impostato, il controllo Rich Edit abilita la stima tramite tastiera virtuale. Questa opzione è disattivata per impostazione predefinita (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**IMF \_ UIFONTS**</dt> </dl>                     | Usare i tipi di carattere predefiniti dell'interfaccia utente. Questa opzione è disattivata per impostazione predefinita (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Il flag **\_ AUTOFONT IMF** è impostato per impostazione predefinita. I **flag IMF \_ AUTOKEYBOARD** e **\_ IMECANCELCOMPLETE IMF** sono deselezionati per impostazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





