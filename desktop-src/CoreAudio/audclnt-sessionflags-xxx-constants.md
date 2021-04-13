---
description: Le \_ costanti AUDCLNT SESSIONFLAGS \_ xxx indicano le caratteristiche di una sessione audio associata al flusso.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Costanti AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483924"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>\_Costanti AUDCLNT SESSIONFLAGS \_ xxx

Le \_ costanti AUDCLNT SESSIONFLAGS \_ xxx indicano le caratteristiche di una sessione audio associata al flusso. Un client può specificare queste opzioni durante l'inizializzazione del flusso tramite il parametro *StreamFlags* del metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .



| Costante/valore                                                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | La sessione scade quando non sono presenti flussi associati e oggetti di controllo della sessione proprietari che contengano riferimenti.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ \_Visualizzazione SESSIONFLAGS \_ Hide**</dt> <dt>0x20000000</dt> </dl>                                     | Il controllo volume è nascosto nell'interfaccia utente del mixer del volume quando viene creata la sessione audio. Se la sessione associata al flusso esiste già prima che [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Apra il flusso, il controllo volume viene visualizzato nel mixer del volume.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | Il controllo volume è nascosto nell'interfaccia utente del mixer del volume dopo la scadenza della sessione. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                     |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio Core](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




