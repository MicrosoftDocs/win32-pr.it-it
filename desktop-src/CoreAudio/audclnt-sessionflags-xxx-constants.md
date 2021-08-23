---
description: Le costanti AUDCLNT SESSIONFLAGS XXX indicano le \_ caratteristiche di una sessione audio \_ associata al flusso.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX costanti (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15423d24d48a98b69c4ab1651941fba639885c03e27cf9df8b1834aab830bb6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018499"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>Costanti AUDCLNT \_ SESSIONFLAGS \_ XXX

Le costanti AUDCLNT SESSIONFLAGS XXX indicano le \_ caratteristiche di una sessione audio \_ associata al flusso. Un client può specificare queste opzioni durante l'inizializzazione del flusso tramite il *parametro StreamFlags* del [**metodo IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)



| Costante/valore                                                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | La sessione scade quando non sono presenti flussi associati e oggetti di controllo della sessione proprietari che conteneno riferimenti.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDE**</dt> <dt>0x20000000</dt> </dl>                                     | Il controllo del volume viene nascosto nell'interfaccia utente del mixer di volumi quando viene creata la sessione audio. Se la sessione associata al flusso esiste già prima che [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) apra il flusso, il controllo del volume viene visualizzato nel mixer di volumi.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ VISUALIZZA \_ HIDEWHENEXPIRED**</dt> <dt>0X40000000</dt> </dl> | Il controllo del volume viene nascosto nell'interfaccia utente del mixer di volumi dopo la scadenza della sessione. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio di base](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




