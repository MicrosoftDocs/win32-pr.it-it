---
title: Strutture WFP
description: Di seguito sono riportate le strutture API di Windows Filtering Platform (WFP).
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Tipi enumerati dell'API della piattaforma filtro Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10e4d47c307766758cc935787d975ffb636f8f9
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "103724148"
---
# <a name="wfp-structures"></a>Strutture WFP

Di seguito sono riportate le strutture API di Windows Filtering Platform (WFP).

Strutture di gestione

-   [**\_ACTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**\_CALLOUT0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**\_CHANGE0 CALLOUT \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**\_ \_ TEMPLATE0 enum di CALLOUT FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**\_SUBSCRIPTION0 CALLOUT \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**\_Classificazione FWPM \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**\_Classificazione FWPM \_ OPTIONS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**\_CONNECTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_ \_ TEMPLATE0 enum di connessione FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**\_Connessione FWPM \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ Visualizza \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**\_FIELD0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**\_FILTER0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**\_CHANGE0 filtro \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**\_CONDITION0 filtro \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**\_Enumerazione del filtro FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**\_SUBSCRIPTION0 filtro \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**\_LAYER0 "FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**\_Enumerazione livello \_ FWPM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**\_STATISTICS0 livello \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   \_evento FWPM NET \_ :
    -   [**FWPM \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**FWPM \_ NET \_ event1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**FWPM \_ NET \_ event2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**\_ \_ Funzionalità evento NET \_ FWPM \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**\_ \_ Funzionalità evento NET \_ FWPM \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**\_ \_ Classificazione evento FWPM \_ net \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   \_ \_ eliminazione classificazione evento FWPM NET \_ \_ :
    -   [**FWPM \_ \_DROP0 di \_ classificazione \_ evento NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**FWPM \_ NET \_ Event \_ Classification \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 e versioni successive)
    -   [**FWPM \_ \_Classificazione eventi \_ net \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**FWPM \_ net \_ Event \_ Classification \_ Drop \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**\_ \_ \_ Enumerazione \_ TEMPLATE0 evento FWPM NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   FWPM \_ l' \_ intestazione dell'evento NET \_ :
    -   [**FWPM \_ \_ \_ HEADER0 evento NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**FWPM \_ \_ \_ HEADER1 evento NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**FWPM \_ NET \_ Event \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   \_errore FWPM NET \_ Event \_ IKEEXT \_ em \_ :
    -   [**FWPM \_ NET \_ Event \_ IKEEXT \_ em \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ Event \_ IKEEXT \_ em \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 e versioni successive)
-   \_errore FWPM NET \_ Event \_ IKEEXT \_ mm \_ :
    -   [**FWPM \_ NET \_ Event \_ IKEEXT \_ mm \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ Event \_ IKEEXT \_ mm \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 e versioni successive)
-   [**FWPM \_ net \_ Event \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ net \_ Event \_ IPSec \_ DoSP \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**\_ \_ \_ \_ DROP0 kernel IPsec dell'evento FWPM NET \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**\_Evento FWPM \_ net \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**\_PROVIDER0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**\_Provider FWPM \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   \_contesto del provider FWPM \_ :
    -   [**FWPM \_ PROVIDER \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**FWPM \_ PROVIDER \_ CONTEXT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   \_Provider FWPM \_ CONTEXT2 (Windows 8)
-   [**\_ \_ CHANGE0 contesto provider \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**\_Enumerazione del contesto del provider FWPM \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**\_ \_ SUBSCRIPTION0 contesto provider \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**\_ \_ TEMPLATE0 enum provider \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**\_Provider FWPM \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**\_SESSION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**\_ \_ TEMPLATE0 enum della sessione FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**\_STATISTICS0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**\_SUBLAYER0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**\_CHANGE0 SOTTOLIVELLO \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**\_TEMPLATE0 enum SOTTOLIVELLO FWPM \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**\_SUBSCRIPTION0 SOTTOLIVELLO \_ FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**\_PORTS0 di sistema FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**FWPM \_ \_ porte \_ di sistema di \_ TYPE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ vswitch \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ vswitch \_ evento \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Strutture condivise

-   [**\_ARRAY6 FWP byte \_**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**\_ARRAY16 FWP byte \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**\_BLOB di byte FWP \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**\_VALUE0 condizione \_ FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**\_RANGE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**\_tipo di corrispondenza FWP \_**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**FWP \_ V4 \_ addr \_ e \_ mask**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**\_ \_ Indirizzo \_ e maschera FWP \_ V6**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**\_VALUE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

Strutture IKE/AuthIP

-   \_metodo di autenticazione IKEEXT \_ :
    -   [**IKEEXT \_ \_METHOD0 di autenticazione**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IKEEXT \_ \_METHOD1 di autenticazione**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IKEEXT \_ \_METHOD2 di autenticazione**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**\_Certificato IKEEXT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_Certificato IKEEXT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 radice certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   \_autenticazione del certificato IKEEXT \_ :
    -   [**IKEEXT \_ \_AUTHENTICATION0 certificato**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IKEEXT \_ \_AUTHENTICATION1 certificato**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IKEEXT \_ \_Accodare certificato**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   \_credenziale del certificato IKEEXT \_ :
    -   [**IKEEXT \_ \_CREDENTIAL0 certificato**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IKEEXT \_ CERTIFICAte \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 e versioni successive)
-   [**\_CRITERIA0 certificato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 di crittografia IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   \_statistiche comuni di IKEEXT \_ :
    -   [**IKEEXT \_ \_STATISTICS0 comuni**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_STATISTICS1 comuni**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 e versioni successive)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   \_credenziali IKEEXT:
    -   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 e versioni successive)
-   \_coppia di credenziali IKEEXT \_ :
    -   [**IKEEXT \_ \_PAIR0 delle credenziali**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 e versioni successive)
-   \_credenziali IKEEXT:
    -   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 e versioni successive)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   \_criteri IKEEXT em \_ :
    -   [**IKEEXT \_ \_POLICY0 em**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IKEEXT \_ \_POLICY1 em**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IKEEXT \_ \_POLICY2 em**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**\_ALGORITHM0 integrità \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   \_ \_ \_ statistiche comuni specifiche della versione IP di IKEEXT \_ \_ :
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS0 comuni specifici della versione IP**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS1 comuni specifici della versione IP**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 e versioni successive)
-   statistiche specifiche del modulo IKEEXT per la \_ \_ versione IP \_ \_ \_ :
    -   [**IKEEXT \_ \_STATISTICS0 del \_ \_ modulo \_ di versione IP specifico**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_STATISTICS1 del \_ \_ modulo \_ di versione IP specifico**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 e versioni successive)
-   [**\_ \_ AUTHENTICATION0 CGA IKEEXT per IPv6 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   \_statistiche del modulo IKEEXT \_ :
    -   [**IKEEXT \_ \_AUTHENTICATION0 Kerberos**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista e Windows 7)
    -   [**IKEEXT \_ \_AUTHENTICATION1 Kerberos**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   \_statistiche del modulo IKEEXT \_ :
    -   [**IKEEXT \_ \_STATISTICS0 di modulo**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_STATISTICS1 di modulo**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 e versioni successive)
-   [**\_Nome IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ v2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   \_criteri IKEEXT:
    -   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   IKEEXT \_ autenticazione della chiave precondivisa \_ \_ :
    -   [**IKEEXT \_ Chiave precondivisa \_ \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IKEEXT \_ Chiave precondivisa \_ \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 e versioni successive)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 riservato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   \_Dettagli SA IKEEXT \_ :
    -   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IKEEXT \_ SA \_ Dettagli**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 e versioni successive)
-   [**\_ \_ TEMPLATE0 enum IKEEXT \_ sa**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   \_statistiche IKEEXT:
    -   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 e versioni successive)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

Strutture IPsec

-   [**\_Indirizzo IPSec \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   \_statistiche di eliminazione di pacchetti di aggregazione IPSec \_ \_ \_ :
    -   [**IPSec \_ \_ \_ \_ STATISTICS0 di eliminazione pacchetti aggregati**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**IPSec \_ AGGREGAzione \_ Drop \_ Packet \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 e versioni successive)
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
-   \_GETSPI IPSec:
    -   [**IPSec \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**IPSec \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 e versioni successive)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_Chiave IPsec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_CALLBACKS0 di \_ gestione \_ chiavi IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   criteri per le \_ chiavi IPSec \_ :
    -   [**IPSec \_ \_POLICY0 di chiavi**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista e Windows 7)
    -   [**IPSec \_ \_POLICY1 di chiavi**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**STATE0 del modulo di IPSEC \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_ \_ Autenticazione \_ e crittografia SA \_ IPSec \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**\_Autenticazione SA \_ IPSec \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   \_bundle SA IPSec \_ :
    -   [**IPSec \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**IPSec \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 e versioni successive)
-   [**\_INFORMATION0 di \_ crittografia \_ SA IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   \_contesto SA IPSec \_ :
    -   [**IPSec \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**IPSec \_ SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 e versioni successive)
-   [**\_ \_ CHANGE0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_Enumerazione del \_ contesto SA IPSec \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_ \_ SUBSCRIPTION0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   \_Dettagli SA IPSec \_ :
    -   [**IPSec \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**IPSec \_ SA \_ Dettagli**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 e versioni successive)
-   [**\_ \_ TEMPLATE0 enum SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**\_TIMEOUT0 di \_ inattività SA IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**\_LIFETIME0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_TRANSFORM0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   \_statistiche IPSec:
    -   [**IPSec \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**IPSec \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 e versioni successive)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   \_traffico IPSec:
    -   [**IPSec \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**IPSec \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 e versioni successive)
-   \_statistiche sul traffico IPSec \_ :
    -   [**IPSec \_ \_STATISTICS0 del traffico**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**IPSec \_ TRAFFIC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 e versioni successive)
-   \_criteri di trasporto IPSec \_ :
    -   [**IPSec \_ \_POLICY0 di trasporto**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**IPSec \_ \_POLICY1 di trasporto**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**IPSec \_ \_POLICY2 di trasporto**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**\_ENDPOINT0 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   \_Endpoint tunnel IPSec \_ :
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   \_criteri tunnel IPSec \_ :
    -   [**IPSec \_ TUNNEL \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**IPSec \_ TUNNEL \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**IPSec \_ TUNNEL \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**\_ \_ ENCAPSULATION0 UDP IPSec \_ V4**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**\_Virtuale IPSec \_ se \_ \_ INFO0 tunnel**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




