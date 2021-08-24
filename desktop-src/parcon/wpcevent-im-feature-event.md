---
description: Evento per utente generato da un client di Messaggistica immediata quando in Controllo genitori vengono usate funzionalità definite.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: WPCEVENT_IM_FEATURE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046e755540a2282e84ea25c5278cf0c0b113264e78a3db31b6bd8a42de599cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951443"
---
# <a name="wpcevent_im_feature-event"></a>Evento WPCEVENT \_ IM \_ FEATURE

Evento per utente generato da un client di Messaggistica immediata quando in Controllo genitori vengono usate funzionalità definite.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di messaggistica immediata.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Stringa di versione per l'applicazione.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nome dell'account di messaggistica immediata dell'utente.

</dd> <dt>

*ConvID* 
</dt> <dd>

ID per questa conversazione.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ IM \_ FEATURE**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) che indica le informazioni sulle funzionalità a cui si accede durante un'interazione di messaggistica immediata.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero di utenti di messaggistica immediata che ricevono la funzionalità e che dispongono di identità definite nel campo del destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Stringa delimitata che contiene le identità dell'account di messaggistica immediata di tutti gli utenti che ricevono la funzionalità.

</dd> <dt>

*Mittente* 
</dt> <dd>

Nome dell'account di messaggistica immediata per l'utente che sta apprendono la funzionalità.

</dd> <dt>

*SenderIP* 
</dt> <dd>

Indirizzo IP del computer del mittente.

</dd> <dt>

*Dati* 
</dt> <dd>

Descrizione dei dati nella funzionalità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per Controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




