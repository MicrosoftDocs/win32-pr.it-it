---
title: Identificatori di callout predefiniti (Fwpmu.h)
description: Gli identificatori per le funzioni di callout incorporate in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi identificatori sono definiti nel modo seguente.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151427"
---
# <a name="built-in-callout-identifiers"></a>Identificatori di callout predefiniti

Gli identificatori per le funzioni di callout incorporate in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi identificatori sono definiti nel modo seguente.

I suffissi V4 e V6 alla fine degli identificatori di callout indicano se il callout è per lo stack di rete IPv4 o per lo stack di rete IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ IN INGRESSO TRANSPORT \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TRANSPORT \_ V6** 
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare tramite un'associazione di sicurezza in modalità trasporto arrivi in modo sicuro.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V4 /FWPM \_ CALLOUT \_ IPSEC OUTBOUND TRANSPORT \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto tramite associazioni di sicurezza in modalità trasporto.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TUNNEL \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TUNNEL \_ V6** 
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare tramite un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ TUNNEL IN USCITA IPSEC \_ \_ \_ V4/FWPM \_ CALLOUT TUNNEL IN USCITA \_ IPSEC \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto tramite associazioni di sicurezza in modalità tunnel.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD \_ INBOUND TUNNEL \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD \_ \_ \_ INBOUND TUNNEL \_ V6**
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare tramite un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.

Questo callout è applicabile al livello di inoltro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD OUTBOUND \_ \_ TUNNEL \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD OUTBOUND TUNNEL \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto tramite un'associazione di sicurezza in modalità tunnel.

Questo callout è applicabile al livello di inoltro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ IN INGRESSO INITIATE \_ \_ SECURE \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Verifica che ogni connessione in ingresso che dovrebbe arrivare sicura arrivi in modo sicuro.

Questo callout è applicabile al livello di accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TUNNEL \_ ALE \_ ACCEPT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TUNNEL \_ ALE ACCEPT \_ \_ V6**
</dt> <dd> <dl> <dt>



Consente i pacchetti IP-in-IP in modalità tunnel IPsec quando vengono classificati a livello di accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ ALE CONNECT \_ \_ V6**
</dt> <dd> <dl> <dt>



Applica i modificatori di criteri IPsec alle applicazioni client.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ DOSP \_ FORWARD \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ DOSP FORWARD \_ \_ V6**
</dt> <dd> <dl> <dt>



Segnala a Protezione DoS IPsec che il traffico deve essere verificato per potenziali dos e potrebbe essere necessario essere limitato alla frequenza.

> [!Note]  
> Disponibile solo in Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ CALLOUT \_ WFP TRANSPORT \_ LAYER \_ \_ V4 SILENT DROP \_ \_ /FWPM \_ CALLOUT WFP TRANSPORT LAYER \_ \_ \_ \_ V6 SILENT \_ \_ DROP**
</dt> <dd> <dl> <dt>



Implementa il filtro in modalità mascheramenti eliminando automaticamente tutti i pacchetti in ingresso per i quali TCP non dispone di un endpoint di ascolto.

Questo callout è applicabile al livello di eliminazione del trasporto in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ CHIMNEY \_ CONNECT LAYER \_ \_ V4/FWPM \_ CALLOUT TCP \_ \_ CHIMNEY \_ CONNECT LAYER \_ \_ V6**
</dt> <dd> <dl> <dt>



Abilita o disabilita tcp chimney offload per ogni connessione in uscita.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ CHIMNEY \_ ACCEPT LAYER \_ \_ V4/FWPM \_ CALLOUT TCP \_ \_ CHIMNEY \_ ACCEPT LAYER \_ \_ V6**
</dt> <dd> <dl> <dt>



Abilita o disabilita tcp chimney offload per ogni connessione in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**OPZIONI SET DI CALLOUT FWPM \_ \_ \_ \_ AUTH \_ CONNECT LAYER \_ \_ V4/FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Imposta le opzioni di classificazione nei flussi in uscita.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH \_ RECV \_ ACCEPT LAYER \_ \_ V4 /FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH \_ RECV \_ ACCEPT LAYER \_ \_ V6**
</dt> <dd> <dl> <dt>



Imposta le opzioni di classificazione nei flussi in ingresso.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ RESERVED \_ AUTH CONNECT LAYER \_ \_ \_ V4/FWPM \_ CALLOUT RESERVED \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE LISTEN \_ \_ V6 /FWPM \_ CALLOUT \_ TEREDO \_ ALE LISTEN \_ \_ V6**
</dt> <dd> <dl> <dt>



Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo servizio.

> [!Note]  
> Per Windows 7 e versioni successive, usare **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**ASSEGNAZIONE DI RISORSE ALE DI ATTRAVERSAMENTO EDGE DEL CALLOUT FWPM \_ \_ \_ \_ \_ \_ \_ V6/CALLOUT FWPM \_ \_ TEREDO \_ ALE \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo servizio.

> [!Note]  
> Per Windows 7 e versioni successive, usare **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**ASSEGNAZIONE DI RISORSE \_ ALE ATTRAVERSAMENTO EDGE DEL CALLOUT FWPM \_ \_ \_ \_ \_ \_ V4** 
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per un uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V4**
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per un uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP TEMPLATES CONNECT LAYER \_ \_ \_ \_ V4/FWPM \_ CALLOUT TCP TEMPLATES CONNECT \_ LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Applica le impostazioni del modello TCP per le connessioni in uscita corrispondenti.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**I MODELLI TCP DI CALLOUT FWPM ACCETTANO I MODELLI TCP DI \_ \_ LIVELLO \_ \_ \_ \_ V4/FWPM \_ CALLOUT \_ \_ \_ \_ ACCETTANO IL LIVELLO \_ V6**
</dt> <dd> <dl> <dt>



Applica le impostazioni del modello TCP per le connessioni in ingresso corrispondenti.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





