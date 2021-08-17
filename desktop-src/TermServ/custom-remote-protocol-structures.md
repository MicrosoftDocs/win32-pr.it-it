---
title: Remote Desktop Protocol di provider di servizi
description: L'API del protocollo remoto personalizzata supporta le strutture seguenti.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f7d1b7b3ea968925cdcace605ed6c136054b023cc12482475196696bdbcc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856238"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Remote Desktop Protocol di provider di servizi

L'API del protocollo remoto personalizzata supporta le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**DATI DI SUPPORTO TSMF \_ \_ \_ IN**](tsmf-support-data-in.md)
</dt> <dd>

Contiene informazioni sui formati multimediali.

</dd> <dt>

[**DATI DI SUPPORTO TSMF \_ \_ \_ OUT**](tsmf-support-data-out.md)
</dt> <dd>

Contiene informazioni sui formati multimediali.

</dd> <dt>

[**TSMF \_ SUPPORTA \_ NODEDATA \_ IN**](tsmf-support-nodedata-in.md)
</dt> <dd>

Usato all'interno [**della struttura TSMF \_ SUPPORT DATA \_ \_ IN**](tsmf-support-data-in.md) per contenere informazioni sui formati multimediali supportati.

</dd> <dt>

[**SUPPORTO DI TSMF \_ \_ NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> <dd>

Utilizzato all'interno [**della struttura TSMF \_ SUPPORT DATA \_ \_ OUT**](tsmf-support-data-out.md) per contenere informazioni sui formati multimediali supportati.

</dd> <dt>

[**IMPOSTAZIONI DI CONNESSIONE \_ \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contiene informazioni sulle impostazioni di connessione per una sessione remota.

</dd> <dt>

[**IMPOSTAZIONI DI CONNESSIONE WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contiene informazioni sulle impostazioni di connessione per una sessione remota.

</dd> <dt>

[**INFORMAZIONI SUL FUSO \_ \_ ORARIO DINAMICO \_ WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contiene informazioni dinamiche sul fuso orario.

</dd> <dt>

[**IMPOSTAZIONI LISTENER \_ \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contiene informazioni sull'impostazione del listener per una sessione remota.

</dd> <dt>

[**IMPOSTAZIONI LISTENER WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contiene le impostazioni del listener per una sessione remota.

</dd> <dt>

[**IMPOSTAZIONI \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contiene informazioni sulle impostazioni relative ai criteri per una sessione remota.

</dd> <dt>

[**IMPOSTAZIONI WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contiene le impostazioni correlate ai criteri per una sessione remota.

</dd> <dt>

[**\_WTS STATISTICHE \_ DELLA CACHE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contiene le statistiche della cache del protocollo.

</dd> <dt>

[**\_WTS VISUALIZZARE \_ IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contiene informazioni sulla visualizzazione del client.

</dd> <dt>

[**\_WTS DATI \_ CLIENT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contiene informazioni sulla connessione client.

</dd> <dt>

[**\_WTS FUNZIONALITÀ DI \_ LICENZA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contiene informazioni sulle funzionalità di gestione delle licenze del client.

</dd> <dt>

[**\_WTS DATI \_ DEI CRITERI**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contiene le informazioni sui criteri passate dal Servizi Desktop remoto al protocollo.

</dd> <dt>

[**\_WTS VALORE \_ DELLA PROPRIETÀ**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contiene informazioni sul valore di una proprietà da recuperare dal protocollo.

</dd> <dt>

[**\_WTS PROTOCOL \_ CACHE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contiene il numero di riscontri nella cache e di riscontri nella cache.

</dd> <dt>

[**\_WTS CONTATORI \_ DI PROTOCOLLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contiene i contatori delle prestazioni del protocollo.

</dd> <dt>

[**\_WTS STATO \_ DEL PROTOCOLLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contiene informazioni sullo stato del protocollo.

</dd> <dt>

[**\_WTS STATO \_ DEL SERVIZIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contiene informazioni sulle modifiche apportate allo stato del Servizi Desktop remoto servizio.

</dd> <dt>

[**\_WTS \_ID SESSIONE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contiene un **GUID che** identifica in modo univoco una sessione.

</dd> <dt>

[**\_WTS SMALL \_ RECT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contiene le coordinate della finestra client.

</dd> <dt>

[**\_WTS SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contiene un indirizzo socket.

</dd> <dt>

[**\_WTS Systemtime**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Specifica informazioni su data e ora per le transizioni tra l'ora solare e l'ora legale.

</dd> <dt>

[**\_WTS INFORMAZIONI \_ SUL FUSO \_ ORARIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contiene informazioni sul fuso orario del client.

</dd> <dt>

[**\_WTS CREDENZIALI \_ UTENTE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contiene informazioni sulle credenziali per un utente.

</dd> <dt>

[**\_WTS DATI \_ UTENTE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contiene i valori delle proprietà client selezionate.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Remote Desktop Protocol riferimento al provider](custom-remote-protocol-reference.md)
</dt> <dt>

[Remote Desktop Protocol di provider di dati](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Remote Desktop Protocol provider di servizi](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Remote Desktop Protocol unioni provider](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




