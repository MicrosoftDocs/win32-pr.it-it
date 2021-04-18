---
title: Strutture del provider Remote Desktop Protocol
description: L'API del protocollo remoto personalizzato supporta le seguenti strutture.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297631"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Strutture del provider Remote Desktop Protocol

L'API del protocollo remoto personalizzato supporta le seguenti strutture.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**TSMF \_ supporta \_ i dati \_ in**](tsmf-support-data-in.md)
</dt> <dd>

Contiene informazioni sui formati multimediali.

</dd> <dt>

[**TSMF \_ supporta \_ i dati in \_ uscita**](tsmf-support-data-out.md)
</dt> <dd>

Contiene informazioni sui formati multimediali.

</dd> <dt>

[**\_supporto \_ di TSMF NODEDATA \_ in**](tsmf-support-nodedata-in.md)
</dt> <dd>

Usati all'interno del [**TSMF \_ supportano i \_ dati \_ nella**](tsmf-support-data-in.md) struttura per contenere informazioni sui formati multimediali supportati.

</dd> <dt>

[**\_NODEDATA di supporto TSMF \_ \_**](tsmf-support-nodedata-out.md)
</dt> <dd>

Usati all'interno di [**TSMF supportano la struttura \_ \_ dei dati \_**](tsmf-support-data-out.md) per contenere informazioni sui formati multimediali supportati.

</dd> <dt>

[**\_impostazioni di connessione WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contiene informazioni sulle impostazioni di connessione per una sessione remota.

</dd> <dt>

[**\_Impostazioni di connessione WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contiene informazioni sulle impostazioni di connessione per una sessione remota.

</dd> <dt>

[**\_ \_ \_ informazioni sul fuso orario dinamico WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contiene informazioni dinamiche sul fuso orario.

</dd> <dt>

[**\_impostazioni del listener WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contiene informazioni sull'impostazione del listener per una sessione remota.

</dd> <dt>

[**\_Impostazioni listener \_ WRDS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contiene le impostazioni del listener per una sessione remota.

</dd> <dt>

[**\_Impostazioni WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contiene informazioni sulle impostazioni relative ai criteri per una sessione remota.

</dd> <dt>

[**\_Impostazioni WRDS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contiene le impostazioni relative ai criteri per una sessione remota.

</dd> <dt>

[**\_statistiche cache \_ WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contiene le statistiche della cache del protocollo.

</dd> <dt>

[**WTS \_ visualizzare \_ IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contiene informazioni sulla visualizzazione client.

</dd> <dt>

[**\_dati client \_ WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contiene informazioni sulla connessione client.

</dd> <dt>

[**\_funzionalità di licenza WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contiene informazioni sulle funzionalità di gestione licenze del client.

</dd> <dt>

[**\_dati dei criteri di WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contiene le informazioni sui criteri passate dal servizio Servizi Desktop remoto al protocollo.

</dd> <dt>

[**\_valore della proprietà WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contiene informazioni sul valore di una proprietà da recuperare dal protocollo.

</dd> <dt>

[**\_cache del protocollo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contiene il numero di letture della cache e riscontri nella cache.

</dd> <dt>

[**\_contatori del protocollo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contiene contatori delle prestazioni del protocollo.

</dd> <dt>

[**\_stato del protocollo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contiene informazioni sullo stato del protocollo.

</dd> <dt>

[**\_stato del servizio WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contiene informazioni sulle modifiche apportate allo stato del servizio Servizi Desktop remoto.

</dd> <dt>

[**\_ID sessione \_ WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contiene un **GUID** che identifica in modo univoco una sessione.

</dd> <dt>

[**WTS \_ small \_ Rect**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contiene le coordinate della finestra client.

</dd> <dt>

[**\_sockaddr WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contiene un indirizzo socket.

</dd> <dt>

[**WTS \_ SYSTEMTIME**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Specifica le informazioni di data e ora per le transizioni tra l'ora solare e l'ora legale.

</dd> <dt>

[**\_ \_ informazioni sul fuso orario WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contiene informazioni sul fuso orario del client.

</dd> <dt>

[**\_credenziali utente \_ WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contiene informazioni sulle credenziali per un utente.

</dd> <dt>

[**WTS \_ \_ dati utente**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contiene i valori delle proprietà del client SELECT.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al provider Remote Desktop Protocol](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumerazioni del provider Remote Desktop Protocol](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Interfacce del provider Remote Desktop Protocol](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Unioni provider Remote Desktop Protocol](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




