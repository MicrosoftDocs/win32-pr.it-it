---
title: Flag di condizione di filtro (Fwptypes. h)
description: I flag della condizione di filtro della piattaforma filtro Windows (WFP) sono rappresentati da un bit.
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
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743151"
---
# <a name="filtering-condition-flags"></a>Flag di condizione di filtro

I flag della condizione di filtro della piattaforma filtro Windows (WFP) sono rappresentati da un bit.

Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**il \_ flag di condizione FWP \_ \_ è \_ loopback**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è il traffico di loopback.

Filtraggio di livelli:

-   FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}
-   FWPM \_ livello di \_ trasporto in uscita \_ \_ V {4 \| 6}
-   \_Flusso di livello FWPM \_ \_ {V4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   \_ \_ Errore ICMP in ingresso FWPM layer \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   \_ \_ Errore ICMP in uscita livello FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   Flusso di FWPM \_ Layer \_ ale \_ \_ stabilito \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**il \_ flag di condizione FWP \_ \_ è \_ protetto da IPSec \_**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è protetto da IPsec.

Filtraggio di livelli:

-   FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**il \_ flag di condizione FWP \_ \_ è stato \_ riautorizzato**
</dt> <dd> <dl> <dt>



Verifica la modifica di un criterio anziché una nuova connessione.

Filtraggio di livelli:

-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**il \_ flag di condizione FWP \_ \_ è \_ associato a caratteri jolly \_**
</dt> <dd> <dl> <dt>



Verifica se l'applicazione ha specificato un indirizzo jolly durante l'associazione a un indirizzo di rete locale.

Livello filtro:

-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**il \_ flag di condizione FWP \_ è un \_ \_ endpoint non elaborato \_**
</dt> <dd> <dl> <dt>



Verifica se l'endpoint locale che invia e riceve il traffico è un endpoint non elaborato.

Filtraggio di livelli:

-   FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   FWPM \_ livello di \_ trasporto in uscita \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   \_ \_ Dati datagramma FWPM layer \_ \_ {V4 \| 6}
    > [!Note]  
    > Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

     

-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**il \_ flag di condizione FWP \_ è un \_ \_ frammento**
</dt> <dd> <dl> <dt>



Verifica se la \_ struttura dell' \_ elenco di buffer NET passata a un driver di callout è un frammento di pacchetto IP.

Filtraggio di livelli:

-   FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6} \_ Elimina


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**il \_ flag di condizione FWP \_ è un \_ \_ gruppo di frammenti \_**
</dt> <dd> <dl> <dt>



Verifica se la \_ struttura dell' \_ elenco di buffer NET passata a un driver di callout descrive un elenco collegato di frammenti di pacchetti.

Livello filtro:

-   FWPM \_ livello \_ IPFORWARD \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**il \_ flag di condizione FWP \_ \_ è la \_ \_ \_ riclassificazione Natt IPSec**
</dt> <dd> <dl> <dt>



Indica che lo stesso pacchetto viene nuovamente classificato a livello di trasporto, quando lo shim NAT IPsec converte il valore della porta remota.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**il \_ flag di condizione FWP \_ richiede la \_ \_ \_ classificazione ale**
</dt> <dd> <dl> <dt>



Indica che il pacchetto verrà riclassificato al livello di ricezione/accettazione ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**il \_ flag di condizione FWP \_ è un' \_ \_ associazione implicita \_**
</dt> <dd> <dl> <dt>



Verifica se i socket di Windows eseguono un'associazione implicita.

Disponibile solo in Windows Vista e Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**il \_ flag di condizione FWP \_ \_ è stato \_ riassemblato**
</dt> <dd> <dl> <dt>



Verifica se il pacchetto è stato riassemblato.

> [!Note]  
> Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.

 

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**il \_ flag di condizione FWP \_ è l' \_ \_ \_ app nome \_ specificata**
</dt> <dd> <dl> <dt>



Verifica se il nome del computer peer a cui è prevista l'applicazione si connette è stato ricevuto tramite un'API, ad esempio [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) , e non è stato ottenuto tramite l'euristica di Caching.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**il \_ flag di condizione FWP \_ \_ è \_ promiscuo**
</dt> <dd> <dl> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**il \_ flag di condizione FWP \_ \_ è \_ auth \_ FW**
</dt> <dd> <dl> <dt>



Verifica se la connessione è autenticata end-to-end, anche se i singoli pacchetti non sono stati verificati.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**il \_ flag di condizione FWP \_ \_ viene \_ riclassificato**
</dt> <dd> <dl> <dt>



Verifica se il motore di filtro sta riclassificando una richiesta di binding o ascolto precedente.

> [!Note]  
> Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}
-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**il \_ flag di condizione FWP \_ è una \_ \_ \_ connessione proxy**
</dt> <dd> <dl> <dt>



Verifica se la connessione utilizza un proxy.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback appcontainer**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è il traffico di loopback del contenitore di app.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback non appcontainer \_**
</dt> <dd> <dl> <dt>



Verifica se il traffico di rete è il traffico di loopback del contenitore non app.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**il \_ flag di condizione FWP \_ \_ è \_ riservato**
</dt> <dd> <dl> <dt>



Riservato.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**il \_ flag di condizione FWP \_ \_ sta \_ rispettando l' \_ \_ autorizzazione per i criteri**
</dt> <dd> <dl> <dt>



Indica che è in corso l'esecuzione della classificazione corrente per rispettare l'intenzione di un'app di Windows Store reindirizzata di connettersi a un host specificato. Tale classificazione conterrà gli stessi valori di campo classificabili come se l'app non venisse mai reindirizzata. Il flag indica inoltre che verrà richiamata una futura classificazione in modo che corrisponda alla destinazione reindirizzata effettiva. Se l'app viene reindirizzata a un servizio proxy per l'ispezione, significa anche che verrà richiamata una futura classificazione sulla connessione proxy. In genere, i driver di callout devono consentire questa classificazione.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano il motivo per la riautorizzazione di una connessione precedentemente autorizzata. Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**\_modifica dei \_ \_ criteri per il motivo della Riautorizzazione della \_ condizione \_ FWP**
</dt> <dd> <dl> <dt>



Indica che la connessione è stata riautorizzata a causa dell'aggiunta o della rimozione dei filtri.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**\_condizione FWP \_ nuova autorizzazione \_ motivo \_ nuova \_ interfaccia di arrivo \_**
</dt> <dd> <dl> <dt>



Indica che il pacchetto è arrivato da un'interfaccia sconosciuta.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**condizione di FWP \_ \_ \_ nuova autorizzazione \_ motivo \_ nuova \_ interfaccia NEXTHOP**
</dt> <dd> <dl> <dt>



Indica che il pacchetto verrà ripartito da un'interfaccia sconosciuta.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP \_ condizione di \_ riautorizzazione del \_ profilo motivo- \_ \_ incrocio**
</dt> <dd> <dl> <dt>



Indica che il pacchetto ha attraversato interfacce di più di una categoria di rete.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ condizione di \_ Riautorizzazione \_ per la classificazione del \_ \_ completamento**
</dt> <dd> <dl> <dt>



Indica che è ora possibile completare una connessione precedentemente mantenuta.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ condizione di \_ riautorizzazione del \_ motivo \_ \_ Proprietà IPSec \_ modificate**
</dt> <dd> <dl> <dt>



Indica che le proprietà IPsec sono state modificate o che la connessione è cambiata da testo non crittografato a una connessione protetta.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ condizione di \_ riautorizzazione del \_ motivo \_ Mid- \_ ispezione del flusso \_**
</dt> <dd> <dl> <dt>



Indica che è in corso l'ispezione di una connessione TCP stabilita in precedenza.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_proprietà del \_ socket del motivo di Riautorizzazione della condizione FWP \_ \_ \_ \_ modificata**
</dt> <dd> <dl> <dt>



Indica che le proprietà del socket sono state impostate dopo che è stata autorizzata e stabilita una connessione.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_condizione FWP \_ riautorizzare il \_ \_ nuovo \_ \_ pacchetto mcast in ingresso \_ gettati \_**
</dt> <dd> <dl> <dt>



Indica che i nuovi pacchetti broadcast o multicast in ingresso vengono riautorizzati in ALE \_ ricezione \_ accettano i callout.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano le proprietà del socket correlate a se un'applicazione vuole ricevere traffico di attraversamento perimetrale. Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**il \_ flag della proprietà Socket della condizione FWP \_ \_ \_ \_ è RPC per la \_ porta di sistema \_ \_**
</dt> <dd> <dl> <dt>



Indica che l'applicazione sta comunicando con una porta RPC dinamica.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}
-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_flag della proprietà Socket della condizione FWP che consente il \_ \_ \_ \_ \_ traffico perimetrale \_**
</dt> <dd> <dl> <dt>



Indica che l'applicazione vuole ricevere traffico specifico di attraversamento del perimetro.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}
-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_flag della proprietà Socket della condizione FWP che nega il \_ \_ \_ \_ \_ traffico perimetrale \_**
</dt> <dd> <dl> <dt>



Indica che l'applicazione non vuole ricevere o elaborare traffico specifico di attraversamento del perimetro.

Livello filtro:

-   FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}
-   \_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

I flag seguenti specificano i dettagli della connessione correlati al filtro L2.

> [!Note]  
> Queste condizioni di filtro sono disponibili solo in Windows 8 e Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**\_La condizione \_ FWP \_ L2 \_ è \_ Ethernet nativa**
</dt> <dd> <dl> <dt>



Indica che la connessione è Ethernet nativa.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**\_La condizione FWP \_ L2 \_ è \_ Wi-Fi**
</dt> <dd> <dl> <dt>



Indica che la connessione è Wi-Fi.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**\_La condizione FWP \_ L2 \_ è \_ mobile \_ Broadband**
</dt> <dd> <dl> <dt>



Indica che la connessione è Mobile Broadband.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_La condizione \_ FWP \_ L2 \_ è \_ dati diretti Wi-Fi \_**
</dt> <dd> <dl> <dt>



Indica che la connessione è Wi-Fi diretta.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_La condizione FWP \_ L2 \_ è \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica che la connessione è tra macchine virtuali.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**\_La condizione FWP \_ L2 è un \_ \_ pacchetto in formato non valido \_**
</dt> <dd> <dl> <dt>



Indica che un pacchetto sembra non essere corretto.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_La condizione FWP \_ L2 è un gruppo di \_ \_ \_ frammenti IP \_**
</dt> <dd> <dl> <dt>



Indica un gruppo di frammenti di pacchetti IP.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Condizione FWP \_ L2 \_ se \_ connettore \_ presente**
</dt> <dd> <dl> <dt>



Indica che è presente un connettore.

Livello filtro:

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Fwptypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

