---
title: Novità di Windows Filtering Platform
description: Windows 8 e Windows Server 2012 nuovi elementi di programmazione Windows Filtering Platform.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e12c1e7add7568b931aabe43f3ab91763df2d5ab12ad448d3683afe13baa3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766661"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Novità di Windows Filtering Platform

Windows 8 e Windows Server 2012 nuovi elementi di programmazione Windows Filtering Platform. Le nuove funzionalità includono quanto segue:

-   *Filtro di livello 2:* fornisce l'accesso al livello L2 (MAC), consentendo di filtrare il traffico a tale livello.
-   *Filtro vSwitch:* consente di controllare e/o modificare i pacchetti che attraversano un vSwitch. I filtri o i callout WFP possono essere usati in ingresso e in uscita di vSwitch.
-   *Gestione dei contenitori di app:* consente l'accesso alle informazioni sui contenitori di app e sui problemi di connettività di isolamento della rete.
-   *Aggiornamenti IPsec:* funzionalità IPsec estesa che include il monitoraggio dello stato della connessione, la selezione dei certificati e la gestione delle chiavi.

Il Windows Driver Kit include anche informazioni sulle modifiche [wfp per Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Windows 8 Aggiornamenti dell'API

Sono state aggiunte molte nuove API per Windows 8 e Windows Server 2012.

## <a name="new-functions"></a>Nuove funzioni

-   [**FWPM \_ NET \_ EVENT \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**CONTROLLO DI DETTATURA CHIAVE DI GESTIONE CHIAVI \_ \_ \_ \_ \_ IPSEC0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**CHIAVE DETTATA DA GESTIONE CHIAVI \_ \_ \_ \_ IPSEC0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**IPSEC \_ KEY \_ MANAGER \_ NOTIFY \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**CALLBACK DEL CONTESTO \_ SA \_ IPSEC0 \_**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**FN DI CALLBACK DI PAC \_ CHANGES \_ \_**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Nuove strutture

-   [**METODO DI \_ AUTENTICAZIONE IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**AUTENTICAZIONE DEL \_ CERTIFICATO IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**CRITERI CERTIFICATO \_ \_ IKEEXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**CRITERI \_ EM IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**AUTENTICAZIONE \_ KERBEROS IKEEXT1 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**CRITERI \_ IKEEXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**GESTIONE CHIAVI \_ \_ IPSEC0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**CALLBACK \_ DI GESTIONE CHIAVI \_ IPSEC0 \_**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**CRITERI DI \_ KEYING IPSEC1 \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**MODIFICA DEL CONTESTO \_ SA \_ IPSEC0 \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**SOTTOSCRIZIONE DEL CONTESTO \_ SA \_ IPSEC0 \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**CRITERI DI TRASPORTO \_ \_ IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**ENDPOINT \_ TUNNEL \_ IPSEC0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**ENDPOINT \_ DEL TUNNEL \_ IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**CRITERI TUNNEL \_ \_ IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ CONNECTION \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FUNZIONALITÀ DEGLI EVENTI NET FWPM \_ \_ \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**CONTESTO DEL \_ PROVIDER FWPM2 \_**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Nuovi tipi enumerati

-   [**TIPO DI \_ RETE VSWITCH \_ \_ FWP**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**TIPO DI FUNZIONALITÀ \_ DI RETE FWPM APPC \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**TIPO DI EVENTO DI CONNESSIONE FWPM \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**TIPO DI EVENTO \_ FWPM VSWITCH \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**TIPO DI NOME DEI CRITERI DEL CERTIFICATO IKEEXT \_ \_ \_ \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**TIPO DI EVENTO \_ CONTESTO SA \_ \_ \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Nuovi identificatori del livello di filtro

[**Filtraggio degli identificatori di livello:**](management-filtering-layer-identifiers-.md)

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FRAME MAC IN INGRESSO DEL LIVELLO FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ ETHERNET
-   FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ ETHERNET
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH TRANSPORT \_ \_ V4/FWPM \_ LAYER \_ INGRESS \_ VSWITCH TRANSPORT \_ \_ V6
-   FWPM \_ LAYER \_ EGRESS \_ VSWITCH TRANSPORT \_ \_ V4/FWPM \_ LAYER \_ EGRESS \_ VSWITCH TRANSPORT \_ \_ V6

## <a name="new-filtering-condition-identifiers"></a>Nuovi identificatori di condizione di filtro

[**Filtraggio degli identificatori di condizione:**](filtering-condition-identifiers-.md)

-   INDIRIZZO \_ MAC DELL'INTERFACCIA DELLA CONDIZIONE \_ FWPM \_ \_
-   CONDIZIONE FWPM \_ \_ INDIRIZZO MAC \_ \_ LOCALE
-   FWPM \_ CONDIZIONE INDIRIZZO REMOTO \_ \_ \_ MAC
-   FWPM \_ CONDITION \_ ETHER \_ TYPE
-   \_ID VLAN della condizione \_ FWPM \_
-   FWPM \_ CONDIZIONE \_ PORTA NDIS \_
-   TIPO DI SUPPORTO \_ FWPM CONDITION \_ NDIS \_ \_
-   FWPM \_ CONDIZIONE \_ NDIS \_ TIPO DI SUPPORTO \_ \_ FISICO
-   FLAG FWPM \_ CONDITION \_ L2 \_
-   FWPM \_ CONDIZIONE MAC TIPO DI INDIRIZZO \_ \_ \_ \_ LOCALE
-   FWPM \_ CONDIZIONE MAC TIPO DI INDIRIZZO \_ \_ \_ \_ REMOTO
-   ID PACCHETTO \_ \_ ALE CONDIZIONE \_ FWPM \_
-   INDIRIZZO DI ORIGINE MAC DELLA CONDIZIONE FWPM \_ \_ \_ \_
-   INDIRIZZO DI DESTINAZIONE MAC DELLA CONDIZIONE FWPM \_ \_ \_ \_
-   FWPM \_ CONDIZIONE TIPO DI INDIRIZZO DI ORIGINE \_ \_ \_ \_ MAC
-   FWPM \_ CONDIZIONE TIPO DI INDIRIZZO DI DESTINAZIONE \_ \_ \_ \_ MAC
-   FWPM \_ CONDIZIONE PORTA DI ORIGINE \_ \_ \_ IP
-   PORTA DI DESTINAZIONE IP DELLA CONDIZIONE FWPM \_ \_ \_ \_
-   \_ID VSWITCH della CONDIZIONE \_ FWPM \_
-   FWPM \_ CONDITION \_ VSWITCH \_ NETWORK \_ TYPE
-   ID INTERFACCIA DI \_ ORIGINE FWPM CONDITION \_ VSWITCH \_ \_ \_
-   ID INTERFACCIA DI \_ DESTINAZIONE FWPM CONDITION \_ VSWITCH \_ \_ \_
-   ID MACCHINA VIRTUALE DI \_ ORIGINE FWPM CONDITION \_ VSWITCH \_ \_ \_
-   ID MACCHINA VIRTUALE DI \_ DESTINAZIONE FWPM CONDITION \_ VSWITCH \_ \_ \_
-   TIPO DI INTERFACCIA \_ DI ORIGINE FWPM CONDITION \_ VSWITCH \_ \_ \_
-   \_FWPM CONDITION \_ VSWITCH TENANT NETWORK ID (ID RETE TENANT FWPM CONDITION \_ \_ \_ VSWITCH)

## <a name="new-filtering-condition-flags"></a>Nuovi flag di condizione di filtro

[**Flag di condizione di filtro:**](filtering-condition-flags-.md)

-   IL \_ FLAG DI CONDIZIONE \_ FWP \_ È LA CONNESSIONE \_ \_ PROXY
-   IL FLAG DELLA CONDIZIONE FWP \_ \_ È \_ \_ LOOPBACK DI APPCONTAINER \_
-   IL FLAG DELLA CONDIZIONE FWP \_ \_ NON È UN \_ \_ \_ \_ LOOPBACK DI APPCONTAINER
-   IL FLAG DELLA CONDIZIONE FWP \_ \_ RISPETTA \_ \_ \_ L'AUTORIZZAZIONE DEI \_ CRITERI
-   LA CONDIZIONE \_ \_ FWP L2 \_ È \_ \_ ETHERNET NATIVA
-   LA CONDIZIONE \_ \_ FWP L2 \_ È \_ WIFI
-   LA CONDIZIONE FWP \_ \_ L2 \_ È MOBILE \_ \_ BROADBAND
-   FWP \_ CONDITION \_ L2 \_ IS \_ WIFI \_ DIRECT \_ DATA
-   LA CONDIZIONE \_ \_ FWP L2 \_ È \_ VM2VM
-   LA CONDIZIONE \_ \_ FWP L2 \_ È UN PACCHETTO IN FORMATO NON \_ \_ VALIDO
-   LA CONDIZIONE FWP \_ \_ L2 \_ È UN GRUPPO \_ DI \_ FRAMMENTI \_ IP
-   CONDIZIONE FWP \_ \_ L2 \_ SE IL \_ CONNETTORE È \_ PRESENTE

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Windows 7 aggiornamenti di Windows Filtering Platform

Il documento Novità di Windows [Filtering Platform]() dettaglia molti degli aggiornamenti apportati per Windows 7. Le informazioni sono disponibili anche in Windows Driver Kit su [WFP Changes per Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 