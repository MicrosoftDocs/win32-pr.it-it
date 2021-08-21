---
title: Flag di condizione di filtro (Fwptypes.h)
description: I flag Windows della condizione di filtro della piattaforma filtro windows (WFP, Windows Filtering Platform) sono rappresentati da un campo di bit.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a43ae080a9ef1c17baa262cc1154f9ae89a837f0ec6f6919d80c22376f3b995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150894"
---
# <a name="filtering-condition-flags"></a>Flag di condizione di filtro

I flag Windows della condizione di filtro della piattaforma filtro windows (WFP, Windows Filtering Platform) sono rappresentati da un campo di bit.

Questi flag e i livelli di filtro in cui possono essere usati sono definiti come segue.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ È \_ LOOPBACK**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è di loopback.

Livelli di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ STREAM \_ {V4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   ERRORE ICMP IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   ERRORE ICMP IN USCITA DEL LIVELLO FWPM \_ \_ \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ È PROTETTO DA \_ \_ IPSEC**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è protetto da IPsec.

Livelli di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**IL \_ FLAG DI CONDIZIONE \_ FWP \_ È \_ REAUTHORIZE**
</dt> <dd> <dl> <dt>



Verifica la modifica di un criterio anziché una nuova connessione.

Livelli di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**IL \_ FLAG DI CONDIZIONE FWP \_ È \_ \_ L'ASSOCIAZIONE CON \_ CARATTERI JOLLY**
</dt> <dd> <dl> <dt>



Verifica se l'applicazione ha specificato un indirizzo con caratteri jolly durante l'associazione a un indirizzo di rete locale.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ È UN ENDPOINT \_ NON \_ ELABORATO**
</dt> <dd> <dl> <dt>



Verifica se l'endpoint locale che invia e riceve traffico è un endpoint non elaborato.

Livelli di filtro:

-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   DATI DEL DATAGRAMMA DEL LIVELLO FWPM \_ \_ \_ \_ {V4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ È \_ FRAGMENT**
</dt> <dd> <dl> <dt>



Verifica se la struttura NET \_ BUFFER \_ LIST passata a un driver callout è un frammento di pacchetto IP.

Livelli di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6} \_ DISCARD


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**IL \_ FLAG DELLA CONDIZIONE FWP \_ È UN GRUPPO DI \_ \_ \_ FRAMMENTI**
</dt> <dd> <dl> <dt>



Verifica se la struttura NET \_ BUFFER \_ LIST passata a un driver callout descrive un elenco collegato di frammenti di pacchetti.

Livello di filtro:

-   FWPM \_ LAYER \_ IPFORWARD \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ È \_ IPSEC \_ NATT \_ RECLASSIFY**
</dt> <dd> <dl> <dt>



Indica che lo stesso pacchetto viene ri-classificato a livello di trasporto, quando lo shim NAT IPsec converte il valore della porta remota.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**IL FLAG DI CONDIZIONE FWP \_ \_ RICHIEDE \_ \_ ALE \_ CLASSIFY**
</dt> <dd> <dl> <dt>



Indica che il pacchetto verrà riclassificato a livello di ricezione/accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**IL \_ FLAG DELLA CONDIZIONE FWP \_ È \_ \_ UN'ASSOCIAZIONE \_ IMPLICITA**
</dt> <dd> <dl> <dt>



Verifica se Windows socket esegue un'associazione implicita.

Disponibile solo in Windows Vista e Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**IL \_ FLAG DELLA \_ CONDIZIONE FWP \_ VIENE \_ RIASSEMBLATO**
</dt> <dd> <dl> <dt>



Verifica se il pacchetto è stato riassemblato.

> [!Note]  
> Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

 

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**IL \_ FLAG DELLA CONDIZIONE FWP \_ È IL NOME SPECIFICATO \_ \_ \_ \_ DALL'APP**
</dt> <dd> <dl> <dt>



Verifica se il nome del computer peer a cui l'applicazione prevede di connettersi è stato ricevuto tramite un'API come [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) e non ottenuto tramite l'euristica di memorizzazione nella cache.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**IL \_ FLAG DI \_ CONDIZIONE FWP \_ È \_ PROMISCUO**
</dt> <dd> <dl> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**IL \_ FLAG DI CONDIZIONE \_ FWP \_ È \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Verifica se la connessione è autenticata end-to-end, anche se i singoli pacchetti non sono stati verificati.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**IL \_ FLAG DELLA CONDIZIONE \_ FWP \_ VIENE \_ RICLASSIFICATO**
</dt> <dd> <dl> <dt>



Verifica se il motore di filtro sta riclassificando una precedente richiesta di associazione o ascolto.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**IL \_ FLAG DI CONDIZIONE \_ FWP \_ È UNA CONNESSIONE \_ \_ PROXY**
</dt> <dd> <dl> <dt>



Verifica se la connessione usa un proxy.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**IL \_ FLAG DELLA CONDIZIONE FWP \_ È \_ \_ LOOPBACK DI APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è traffico di loopback dei contenitori di app.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**IL \_ FLAG DI CONDIZIONE \_ FWP \_ NON È \_ UN \_ LOOPBACK DI \_ APPCONTAINER**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è un traffico di loopback non di contenitori di app.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**IL \_ FLAG DI CONDIZIONE \_ FWP \_ È \_ RISERVATO**
</dt> <dd> <dl> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**IL \_ FLAG DI CONDIZIONE FWP \_ RISPETTA \_ \_ \_ L'AUTORIZZAZIONE DEI \_ CRITERI**
</dt> <dd> <dl> <dt>



Indica che viene eseguita la classificazione corrente per rispettare l'intenzione di un'app Windows Store reindirizzata di connettersi a un host specificato. Tale classificazione conterrà gli stessi valori di campo classificabili come se l'app non fosse mai stata reindirizzata. Il flag indica anche che verrà richiamata una classificazione futura in modo che corrisponda alla destinazione reindirizzata effettiva. Se l'app viene reindirizzata a un servizio proxy per l'ispezione, significa anche che verrà richiamata una classificazione futura nella connessione proxy. I driver di callout devono in genere consentire questa classificazione.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano il motivo della riautorizzazione di una connessione autorizzata in precedenza. Questi flag e i livelli di filtro in cui possono essere usati sono definiti come segue.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**MODIFICA DEI \_ CRITERI MOTIVO PER LA RICHIESTA DI AUTORIZZAZIONE DELLA \_ \_ \_ CONDIZIONE \_ FWP**
</dt> <dd> <dl> <dt>



Indica che la connessione è stata riautorizzata a causa dell'aggiunta o della rimozione di filtri.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**NUOVA AUTORIZZAZIONE DELLA CONDIZIONE FWP \_ PER LA NUOVA INTERFACCIA DI \_ \_ \_ \_ \_ ARRIVO**
</dt> <dd> <dl> <dt>



Indica che il pacchetto è arrivato da un'interfaccia sconosciuta.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**NUOVA AUTORIZZAZIONE DELLA CONDIZIONE FWP \_ PER LA NUOVA INTERFACCIA \_ \_ \_ \_ NEXTHOP \_**
</dt> <dd> <dl> <dt>



Indica che il pacchetto verrà rimosso da un'interfaccia sconosciuta.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**MODIFICA \_ DELL'AUTORIZZAZIONE DEL PROFILO MOTIVO \_ DELLA \_ CONDIZIONE \_ \_ FWP**
</dt> <dd> <dl> <dt>



Indica che il pacchetto è passato attraverso interfacce di più di una categoria di rete.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**RICHIESTA DI AUTORIZZAZIONE DEL MOTIVO PER LA \_ \_ RIAUTENZIONE DELLA CONDIZIONE FWP \_ \_ CLASSIFICA \_ COMPLETAMENTO**
</dt> <dd> <dl> <dt>



Indica che è ora possibile completare una connessione precedentemente mantenuta.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**MODIFICA DELLE \_ PROPRIETÀ \_ IPSEC DELLA CONDIZIONE \_ \_ FWP \_ \_**
</dt> <dd> <dl> <dt>



Indica che le proprietà IPsec sono state modificate o che la connessione è stata modificata da testo non crittografato a connessione protetta.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**MOTIVO DELLA \_ \_ RIAUTORIZZAZIONE DELLA CONDIZIONE FWP DURANTE \_ \_ \_ L'ISPEZIONE DEL FLUSSO \_ INTERMEDIO**
</dt> <dd> <dl> <dt>



Indica che è in corso il controllo di una connessione TCP stabilita in precedenza.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**MODIFICA DELLA \_ PROPRIETÀ \_ DEL \_ \_ SOCKET \_ \_ MOTIVO MODIFICA DELLA CONDIZIONE FWP**
</dt> <dd> <dl> <dt>



Indica che le proprietà del socket sono state impostate dopo che una connessione è stata autorizzata e stabilita.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**NUOVA AUTORIZZAZIONE DELLA CONDIZIONE FWP \_ PER IL NUOVO PACCHETTO \_ \_ \_ \_ \_ BCAST MCAST IN \_ \_ INGRESSO**
</dt> <dd> <dl> <dt>



Indica che i nuovi pacchetti multicast o broadcast in ingresso vengono nuovamente autorizzati nei callout ALE \_ RECV \_ ACCEPT.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano le proprietà del socket correlate al fatto che un'applicazione voglia ricevere il traffico di attraversamento perimetrale. Questi flag e i livelli di filtro in cui possono essere usati sono definiti come segue.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**IL FLAG DELLA PROPRIETÀ SOCKET DELLA CONDIZIONE FWP \_ È RPC DELLA PORTA DI \_ \_ \_ \_ \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>



Indica che l'applicazione sta comunicando con una porta RPC dinamica.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FLAG DI PROPRIETÀ DEL SOCKET DELLA CONDIZIONE FWP \_ CHE CONSENTE IL TRAFFICO \_ \_ \_ \_ \_ \_ PERIMETRALE**
</dt> <dd> <dl> <dt>



Indica che l'applicazione vuole ricevere traffico specifico dell'attraversamento perimetrale.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FLAG DI PROPRIETÀ DEL SOCKET DELLA CONDIZIONE FWP \_ \_ DENY EDGE TRAFFIC \_ \_ \_ \_ (NEGA TRAFFICO \_ PERIMETRALE)**
</dt> <dd> <dl> <dt>



Indica che l'applicazione non vuole ricevere o elaborare il traffico specifico dell'attraversamento perimetrale.

Livello di filtro:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano i dettagli di connessione correlati al filtro L2.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows 8 e Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**LA CONDIZIONE \_ \_ FWP L2 \_ È \_ \_ ETHERNET NATIVA**
</dt> <dd> <dl> <dt>



Indica che la connessione è Ethernet nativa.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN USCITA DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP CONDITION L2 IS WIFI (LA CONDIZIONE \_ \_ FWP L2 \_ \_ È WIFI)**
</dt> <dd> <dl> <dt>



Indica che la connessione è Wi-Fi.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN USCITA DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ MOBILE \_ BROADBAND**
</dt> <dd> <dl> <dt>



Indica che la connessione è Mobile Broadband.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN USCITA DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP \_ CONDITION \_ L2 IS WIFI DIRECT DATA (LA CONDIZIONE FWP L2 \_ È DATI DIRETTI \_ \_ \_ WIFI)**
</dt> <dd> <dl> <dt>



Indica che la connessione è Wi-Fi Direct.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**LA CONDIZIONE \_ \_ FWP L2 \_ È \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica che la connessione è tra macchine virtuali.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**LA CONDIZIONE \_ \_ FWP L2 \_ È UN PACCHETTO IN FORMATO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>



Indica che il formato di un pacchetto non è corretto.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**LA CONDIZIONE FWP \_ \_ L2 \_ È UN GRUPPO \_ DI \_ FRAMMENTI \_ IP**
</dt> <dd> <dl> <dt>



Indica un gruppo di frammenti di pacchetti IP.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**CONDIZIONE FWP \_ \_ L2 \_ SE IL \_ CONNETTORE È \_ PRESENTE**
</dt> <dd> <dl> <dt>



Indica che è presente un connettore.

Livello di filtro:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Fwptypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

