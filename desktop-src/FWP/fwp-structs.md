---
title: Strutture WFP
description: Le Windows dell'API WFP (Filtering Platform) sono le seguenti.
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows Applicazione di filtri ai tipi enumerati dell'API della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b1bd45efbe1a93ddeb0c95161aa52764bf1812ecc5f8e914e01317b657f251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069171"
---
# <a name="wfp-structures"></a>Strutture WFP

Le Windows dell'API WFP (Filtering Platform) sono le seguenti.

Strutture di gestione

-   [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**CALLOUT DI \_ FWPM0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**FWPM \_ CALLOUT \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**FWPM \_ CALLOUT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**FWPM \_ CALLOUT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**OPZIONE DI CLASSIFICAZIONE \_ FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**OPZIONI DI \_ CLASSIFICAZIONE FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ CONNECTION \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**FWPM \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**FWPM \_ FILTER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**FWPM \_ FILTER \_ CONDITION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**FWPM \_ FILTER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**SOTTOSCRIZIONE DEL \_ FILTRO FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**FWPM \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**FWPM \_ LAYER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**STATISTICHE DEL \_ LIVELLO FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   EVENTO NET \_ \_ FWPM:
    -   [**FWPM \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**FUNZIONALITÀ DEGLI EVENTI NET FWPM \_ \_ \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP:
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 e versioni successive)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   INTESTAZIONE DELL'EVENTO \_ NET FWPM: \_ \_
    -   [**FWPM \_ NET \_ EVENT \_ HEADER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   ERRORE EM \_ \_ \_ IKEEXT DELL'EVENTO NET FWPM: \_ \_
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 e versioni successive)
-   FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM FAILURE \_ ::
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 e versioni successive)
-   [**FWPM \_ NET \_ EVENT \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ DOSP \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ KERNEL \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**FWPM \_ NET \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**PROVIDER \_ FWPM0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**FWPM \_ PROVIDER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   CONTESTO \_ DEL PROVIDER FWPM: \_
    -   [**FWPM \_ PROVIDER \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**FWPM \_ PROVIDER \_ CONTEXT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   CONTESTO PROVIDER FWPM2 \_ \_ (Windows 8)
-   [**MODIFICA DEL CONTESTO \_ DEL PROVIDER FWPM0 \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**FWPM \_ PROVIDER \_ CONTEXT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**SOTTOSCRIZIONE DEL CONTESTO \_ DEL PROVIDER FWPM0 \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**FWPM \_ PROVIDER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**SOTTOSCRIZIONE \_ DEL PROVIDER FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**SESSIONE \_ FWPM0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**FWPM \_ SESSION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**STATISTICHE \_ FWPM0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**FWPM \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**FWPM \_ SUBLAYER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**FWPM \_ SUBLAYER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**SOTTOSCRIZIONE DI FWPM \_ \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**PORTE DI \_ SISTEMA FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**PORTE DI SISTEMA FWPM \_ \_ PER \_ \_ TIPO0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Strutture condivise

-   [**MATRICE DI \_ BYTE FWP6 \_**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**MATRICE DI \_ BYTE FWP16 \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**BLOB DI BYTE FWP \_ \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**VALORE CONDIZIONE \_ \_ FWP0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**TIPO DI \_ CORRISPONDENZA \_ FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**FWP \_ V4 \_ ADDR \_ E \_ MASK**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**FWP \_ V6 \_ ADDR \_ E \_ MASK**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**VALORE \_ FWP0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

Strutture IKE/AuthIP

-   METODO DI \_ AUTENTICAZIONE IKEEXT: \_
    -   [**IKEEXT \_ AUTHENTICATION \_ METHOD0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IKEEXT \_ METODO \_ DI AUTENTICAZIONE1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IKEEXT \_ METODO \_ DI AUTENTICAZIONE2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   AUTENTICAZIONE DEL CERTIFICATO \_ IKEEXT: \_
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   CREDENZIALI CERTIFICATO \_ \_ IKEEXT:
    -   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 e versioni successive)
-   [**CRITERI DEL \_ CERTIFICATO IKEEXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**ALGORITMO \_ DI CRITTOGRAFIA IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   STATISTICHE COMUNI \_ \_ IKEEXT:
    -   [**IKEEXT \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 e versioni successive)
-   [**COPPIA DI \_ COOKIE IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   CREDENZIALI \_ IKEEXT:
    -   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 e versioni successive)
-   COPPIA DI \_ CREDENZIALI IKEEXT: \_
    -   [**IKEEXT \_ CREDENTIAL \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 e versioni successive)
-   CREDENZIALI \_ IKEEXT:
    -   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 e versioni successive)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   CRITERI \_ EM IKEEXT: \_
    -   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**ALGORITMO DI \_ INTEGRITÀ IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   STATISTICHE COMUNI \_ SPECIFICHE DELLA VERSIONE IP IKEEXT: \_ \_ \_ \_
    -   [**IKEEXT \_ STATISTICHE \_ COMUNI SPECIFICHE DELLA VERSIONE \_ \_ \_ IP0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICHE \_ COMUNI SPECIFICHE DELLA VERSIONE \_ \_ \_ IP1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 e versioni successive)
-   STATISTICHE \_ KEYMODULE SPECIFICHE DELLA VERSIONE IP IKEEXT: \_ \_ \_ \_
    -   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ VERSIONE \_ IP \_ SPECIFICA \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 e versioni successive)
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   STATISTICHE \_ KEYMODULE \_ IKEEXT:
    -   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista e Windows 7)
    -   [**IKEEXT \_ AUTENTICAZIONE \_ KERBEROS1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   STATISTICHE \_ KEYMODULE \_ IKEEXT:
    -   [**IKEEXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 e versioni successive)
-   [**IKEEXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   CRITERI \_ IKEEXT:
    -   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   AUTENTICAZIONE CON CHIAVE \_ \_ PRECONDIVISA IKEEXT: \_
    -   [**IKEEXT \_ PRESHARED \_ KEY \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IKEEXT \_ PRESHARED \_ KEY \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 e versioni successive)
-   [**PROPOSTA \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**AUTENTICAZIONE RISERVATA \_ \_ IKEEXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   DETTAGLI \_ DELL'SA IKEEXT: \_
    -   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 e versioni successive)
-   [**IKEEXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   STATISTICHE \_ IKEEXT:
    -   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 e versioni successive)
-   [**TRAFFICO \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

Strutture IPsec

-   [**IPSEC \_ ADDRESS \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   STATISTICHE DROP \_ \_ PACKET DI AGGREGAZIONE \_ \_ IPSEC:
    -   [**IPSEC \_ AGGREGARE \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**IPSEC \_ AGGREGATE \_ DROP \_ PACKET \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 e versioni successive)
-   [**STATISTICHE SA \_ \_ AGGREGAZIONE \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ AH \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**IPSEC \_ AUTH \_ AND \_ CIPHER \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**IPSEC \_ CIPHER \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**IPSEC \_ CIPHER \_ TRANSFORM \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**OPZIONI \_ DOSP \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ DOSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**ENUMERAZIONE DI STATO DOSP IPSEC \_ \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ DOSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSEC \_ ESP \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   IPSEC \_ GETSPI:
    -   [**IPSEC \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**IPSEC \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 e versioni successive)
-   [**IPSEC \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**IPSEC \_ KEY \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**CALLBACK \_ DI GESTIONE CHIAVI \_ IPSEC0 \_**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   CRITERI DI \_ KEYING IPSEC: \_
    -   [**IPSEC \_ KEYING \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista e Windows 7)
    -   [**IPSEC \_ KEYING \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**IPSEC \_ KEYMODULE \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**PROPOSTA \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**IPSEC \_ SA0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**INFORMAZIONI DI CRITTOGRAFIA \_ E AUTENTICAZIONE SA \_ \_ \_ \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**INFORMAZIONI \_ SULL'AUTENTICAZIONE SA \_ \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   BUNDLE SA \_ IPSEC: \_
    -   [**IPSEC \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**IPSEC \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 e versioni successive)
-   [**IPSEC \_ SA \_ CIPHER \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   CONTESTO SA \_ \_ IPSEC:
    -   [**IPSEC \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**IPSEC \_ SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 e versioni successive)
-   [**IPSEC \_ SA \_ CONTEXT \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ CONTEXT ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**IPSEC \_ SA \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   DETTAGLI SA \_ \_ IPSEC:
    -   [**IPSEC \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**IPSEC \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 e versioni successive)
-   [**IPSEC \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**IPSEC \_ SA \_ IDLE \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   STATISTICHE \_ IPSEC:
    -   [**IPSEC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**IPSEC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 e versioni successive)
-   [**TOKEN \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   TRAFFICO \_ IPSEC:
    -   [**IPSEC \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 e versioni successive)
-   STATISTICHE SUL \_ TRAFFICO \_ IPSEC:
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 e versioni successive)
-   CRITERI DI TRASPORTO \_ \_ IPSEC:
    -   [**IPSEC \_ TRANSPORT \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**IPSEC \_ TRANSPORT \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**IPSEC \_ TRANSPORT \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**IPSEC \_ TUNNEL \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   ENDPOINT DEL \_ TUNNEL IPSEC: \_
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**IPSEC \_ ENDPOINT \_ TUNNEL1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**IPSEC \_ ENDPOINT \_ TUNNEL2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   CRITERI TUNNEL \_ \_ IPSEC:
    -   [**IPSEC \_ TUNNEL \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**IPSEC \_ TUNNEL \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**IPSEC \_ TUNNEL \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**IPSEC \_ V4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ VIRTUALE IF TUNNEL \_ \_ \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




