---
title: Strutture IPsec
description: Strutture IPsec
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd268fda1ee98ec80d20d8c75625d4f68526c741
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "106299481"
---
# <a name="ipsec-structures"></a>Strutture IPsec

## <a name="in-this-section"></a>Contenuto della sezione

-   [**\_Indirizzo IPSec \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [**\_STATISTICS0 di \_ eliminazione \_ pacchetto \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [**\_STATISTICS1 di \_ eliminazione \_ pacchetto \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [**\_STATISTICS0 SA aggregazione IPSec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**\_STATISTICS0 di \_ eliminazione di \_ pacchetti \_ IPSec AH**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_ \_ TRANSFORM0 di autenticazione e \_ crittografia \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**\_TRANSFORM0 di autenticazione IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**\_ID0 di \_ trasformazione \_ autenticazione IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**\_Crittografia IPSec \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**\_ID0 di \_ trasformazione \_ crittografia IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**\_OPTIONS0 DoSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**\_STATE0 DoSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**\_ \_ \_ TEMPLATE0 enum stato DoSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**\_STATISTICS0 DoSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**\_STATISTICS0 di \_ eliminazione \_ pacchetti \_ ESP IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [**\_GETSPI0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [**\_GETSPI1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_Chiave IPsec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_CALLBACKS0 di \_ gestione \_ chiavi IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY0 di chiavi IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [**\_POLICY1 di chiavi IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**STATE0 del modulo di IPSEC \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_ \_ Autenticazione \_ e crittografia SA \_ IPSec \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**\_Autenticazione SA \_ IPSec \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [**\_BUNDLE0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [**\_BUNDLE1 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [**\_INFORMATION0 di \_ crittografia \_ SA IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [**\_CONTEXT0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [**\_CONTEXT1 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [**\_ \_ CHANGE0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_Enumerazione del \_ contesto SA IPSec \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_ \_ SUBSCRIPTION0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_DETAILS0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [**\_Dettagli SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [**\_ \_ TEMPLATE0 enum SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**\_TIMEOUT0 di \_ inattività SA IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**\_LIFETIME0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_STATISTICS0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [**\_STATISTICS1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [**\_TRANSFORM0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [**\_TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [**\_TRAFFIC1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [**\_Traffico IPSec \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [**\_Traffico IPSec \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [**\_POLICY0 trasporto \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [**\_POLICY1 trasporto \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [**\_POLICY2 trasporto \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS0 tunnel \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [**\_ENDPOINTS1 tunnel \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [**\_ENDPOINTS2 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY0 tunnel \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [**\_POLICY1 tunnel \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [**\_POLICY2 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**\_ \_ ENCAPSULATION0 UDP IPSec \_ V4**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**\_Virtuale IPSec \_ se \_ \_ INFO0 tunnel**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




