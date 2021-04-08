---
title: Identificatori di callout predefiniti (Fwpmu. h)
description: Gli identificatori per le funzioni di callout compilate in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi identificatori sono definiti nel modo seguente.
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
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964890"
---
# <a name="built-in-callout-identifiers"></a>Identificatori di callout predefiniti

Gli identificatori per le funzioni di callout compilate in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi identificatori sono definiti nel modo seguente.

I suffissi V4 e V6 alla fine degli identificatori di callout indicano se il callout è per lo stack di rete IPv4 o per lo stack di rete IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM callout trasporto in ingresso IPSec di callout \_ \_ \_ \_ \_ V4/FWPM \_ \_ \_ \_ \_** 
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità trasporto arrivi in modo sicuro.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ callout IPSec trasporto in uscita \_ \_ V4/FWPM il trasporto in \_ \_ \_ \_ uscita IPSec in \_ uscita \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto sulle associazioni di sicurezza in modalità trasporto.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM callout tunnel in ingresso IPSec \_ \_ \_ \_ \_ V4/FWPM \_ \_ \_ \_ \_** 
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Tunnel in uscita IPSec FWPM \_ callout \_ \_ \_ \_ V4/FWPM \_ callout IPSec in \_ \_ uscita \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto sulle associazioni di sicurezza in modalità tunnel.

Questo callout è applicabile a livello di trasporto.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ callout \_ IPSec \_ inoltri tunnel in ingresso \_ \_ \_ V4/FWPM \_ callout \_ protocollo IPSec \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.

Questo callout è applicabile a livello di inoltri.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ callout \_ IPSec \_ inoltri in uscita \_ \_ tunnel \_ V4/ \_ FWPM \_ callout \_ in \_ uscita del \_ tunnel \_ V6**
</dt> <dd> <dl> <dt>



Indica a IPsec il traffico in uscita che deve essere protetto tramite un'associazione di sicurezza in modalità tunnel.

Questo callout è applicabile a livello di inoltri.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ callout \_ IPSec in \_ ingresso \_ avvio \_ Secure \_ V4/FWPM \_ callout IPSec in \_ \_ ingresso \_ avviare \_ Secure \_ V6** 
</dt> <dd> <dl> <dt>



Verifica che ogni connessione in ingresso che dovrebbe arrivare sicuro arrivi in modo sicuro.

Questo callout è applicabile al livello di accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ callout \_ IPSec in \_ ingresso \_ tunnel \_ ale \_ Accept \_ V4/FWPM \_ callout \_ in \_ ingresso \_ tunnel \_ ale \_ Accept \_ V6**
</dt> <dd> <dl> <dt>



Consente i pacchetti IP-in modalità tunnel IPsec quando vengono classificati al livello di accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ callout \_ IPSec \_ ale \_ Connect \_ V4/FWPM \_ callout \_ IPSec \_ ale \_ Connect \_ V6**
</dt> <dd> <dl> <dt>



Applica i modificatori di criteri IPsec alle applicazioni client.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ callout \_ IPSec \_ DoSP \_ in poi \_ V4/FWPM \_ callout \_ IPSec \_ DoSP \_ in futuro \_ V6**
</dt> <dd> <dl> <dt>



Segnala alla protezione DoS IPsec che il traffico deve essere verificato per le potenziali DoS e potrebbe essere necessario un limite di frequenza.

> [!Note]  
> Disponibile solo in Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ callout \_ PAM \_ Transport \_ Layer \_ V4 \_ Silent \_ Drop/FWPM \_ callout \_ \_ Transport \_ Layer \_ V6 \_ Silent \_ Drop**
</dt> <dd> <dl> <dt>



Implementa il filtro in modalità Stealth ignorando automaticamente tutti i pacchetti in ingresso per i quali TCP non dispone di un endpoint di ascolto.

Questo callout è applicabile al livello di eliminazione del trasporto in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Abilita o disabilita TCP Chimney Offload per ogni connessione in uscita.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ callout \_ TCP \_ Chimney \_ Accept \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Chimney \_ Accept \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Abilita o disabilita TCP Chimney Offload per ogni connessione in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**Opzioni \_ set di CALLOUT FWPM \_ \_ \_ autenticazione \_ connessione \_ Layer \_ V4/FWPM \_ callout \_ set \_ Opzioni \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Imposta le opzioni di classificazione nei flussi in uscita.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**\_Opzioni set di CALLOUT FWPM \_ \_ \_ auth \_ ricezione \_ Accept \_ Layer \_ V4/FWPM \_ callout \_ set \_ Options \_ auth \_ ricezione \_ Accept \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Imposta le opzioni di classificazione nei flussi in ingresso.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ callout \_ riservato \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ reserved Authentication \_ \_ \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ callout \_ Edge \_ attraversamento \_ ale \_ ascolto \_ V6/FWPM \_ callout \_ TEREDO \_ ale \_ ascolto \_ V6**
</dt> <dd> <dl> <dt>



Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo.

> [!Note]  
> Per Windows 7 e versioni successive, usare **FWPM \_ CALLOUT \_ Edge \_ attraversamento \_ ale \_ ascolto \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**Assegnazione delle risorse ale del callout di FWPM di \_ \_ \_ \_ \_ \_ \_ FWPM V6/ \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo.

> [!Note]  
> Per Windows 7 e versioni successive, usare l' **\_ \_ \_ \_ \_ assegnazione delle risorse \_ \_ di FWPM CALLOUT Edge attraversamento della birra V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_ \_ \_ \_ \_ Assegnazione delle risorse ale del bordo di \_ CALLOUT FWPM \_ V4** 
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per un utilizzo futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ \_ attraversamento bordo CALLOUT- \_ \_ ale \_ ascolto \_ V4**
</dt> <dd> <dl> <dt>



Questo identificatore è riservato per un utilizzo futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ callout \_ i \_ modelli TCP \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Templates \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Applica le impostazioni del modello TCP per la corrispondenza delle connessioni in uscita.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**I \_ modelli TCP di CALLOUT FWPM \_ \_ accettano i \_ \_ modelli TCP di livello \_ V4/FWPM che \_ accettano il \_ \_ \_ \_ livello \_ V6**
</dt> <dd> <dl> <dt>



Applica le impostazioni del modello TCP per la corrispondenza delle connessioni in ingresso.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





