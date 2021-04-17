---
title: Novità della piattaforma filtro Windows
description: Windows 8 e Windows Server 2012 introducono nuovi elementi di programmazione della piattaforma filtro Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339873"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Novità della piattaforma filtro Windows

Windows 8 e Windows Server 2012 introducono nuovi elementi di programmazione della piattaforma filtro Windows. Le nuove funzionalità includono quanto segue:

-   *Filtro di livello 2*: fornisce l'accesso al livello L2 (Mac), consentendo il filtraggio del traffico a tale livello.
-   *filtro vswitch*: consente di controllare e/o modificare i pacchetti che attraversano un vswitch. I filtri o i callout di WFP possono essere usati in ingresso e in uscita vSwitch.
-   *Gestione dei contenitori di app*: consente l'accesso alle informazioni sui contenitori di app e sui problemi di connettività di isolamento rete.
-   *Aggiornamenti IPSec*: funzionalità IPSec estese, tra cui il monitoraggio dello stato della connessione, la selezione del certificato e la gestione delle chiavi.

Il kit driver di Windows include anche informazioni sulle [modifiche del WFP per Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Aggiornamenti dell'API di Windows 8

Sono state aggiunte molte nuove API per Windows 8 e Windows Server 2012.

## <a name="new-functions"></a>Nuove funzioni

-   [**\_Evento FWPM \_ net \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
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
-   [**CHECK0 chiave di \_ Gestione chiavi IPSec \_ \_ \_ \_**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**Il \_ gestore delle chiavi IPSec \_ \_ impone \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_ \_ \_ Notifica Key0 di gestione chiavi IPSec \_**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_ \_ CALLBACK0 contesto SA \_ IPSec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
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
-   [**PAC \_ modifiche \_ richiamate \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Nuove strutture

-   [**\_METHOD2 IKEEXT Authentication \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_Certificato IKEEXT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_Certificato IKEEXT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_Accodare certificato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CRITERIA0 certificato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ em \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_Chiave IPsec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_CALLBACKS0 di \_ gestione \_ chiavi IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY1 di chiavi IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**\_ \_ CHANGE0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_ \_ SUBSCRIPTION0 contesto SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_POLICY2 trasporto \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS2 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY2 tunnel \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**\_CONNECTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_ \_ TEMPLATE0 enum di connessione FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**\_Connessione FWPM \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ net \_ event2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**\_ \_ Funzionalità evento NET \_ FWPM \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**\_ \_ Funzionalità evento NET \_ FWPM \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**\_ \_ Classificazione evento FWPM \_ net \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**\_ \_ Classificazione evento FWPM \_ net \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ net \_ Event \_ Classification \_ Drop \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**\_Evento FWPM \_ net \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**\_Provider FWPM \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ vswitch \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ vswitch \_ evento \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Nuovi tipi enumerati

-   [**\_tipo di \_ rete \_ vswitch FWP**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**\_tipo di \_ funzionalità di rete APPC \_ FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_tipo di \_ evento di connessione FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**\_tipo di \_ evento \_ vswitch di FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**\_tipo di \_ \_ nome criteri CERT IKEEXT \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**\_Evento del \_ contesto SA IPSec \_ \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Nuovi identificatori del livello di filtro

[**Filtraggio degli identificatori di livello:**](management-filtering-layer-identifiers-.md)

-   FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet
-   FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet
-   \_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM
-   \_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo
-   FWPM \_ Layer in \_ ingresso \_ vswitch \_ Ethernet
-   FWPM \_ Layer in \_ uscita \_ vswitch \_ Ethernet
-   FWPM \_ Layer in \_ ingresso \_ vswitch \_ trasporto \_ V4/FWPM \_ livello \_ ingresso \_ vswitch \_ trasporto \_ V6
-   Livello FWPM in \_ \_ uscita vswitch trasporto di \_ \_ \_ livello V4/FWPM in \_ \_ uscita \_ vswitch \_ trasporto \_ V6

## <a name="new-filtering-condition-identifiers"></a>Nuovi identificatori di condizione di filtro

[**Filtraggio degli identificatori di condizione:**](filtering-condition-identifiers-.md)

-   \_ \_ indirizzo MAC dell'interfaccia della condizione FWPM \_ \_
-   \_ \_ \_ indirizzo locale Mac della condizione FWPM \_
-   \_ \_ \_ indirizzo remoto Mac condizione \_ FWPM
-   \_ \_ tipo etere della condizione FWPM \_
-   \_ \_ ID VLAN della condizione FWPM \_
-   \_ \_ porta NDIS (FWPM Condition) \_
-   \_tipo di \_ \_ supporto NDIS Condition FWPM \_
-   \_tipo di \_ \_ supporto fisico \_ NDIS \_ condizione FWPM
-   \_ \_ Flag L2 della condizione FWPM \_
-   \_tipo di \_ \_ indirizzo locale \_ Mac \_ della condizione FWPM
-   \_tipo di \_ \_ indirizzo remoto \_ Mac \_ della condizione FWPM
-   \_ \_ \_ ID pacchetto ale condizione \_ FWPM
-   \_indirizzo di \_ \_ origine Mac della condizione \_ FWPM
-   \_indirizzo di \_ \_ destinazione Mac della condizione \_ FWPM
-   \_tipo di \_ \_ indirizzo di origine Mac della condizione \_ FWPM \_
-   \_tipo di \_ \_ indirizzo di destinazione Mac della condizione \_ FWPM \_
-   \_porta di \_ \_ origine IP della condizione \_ FWPM
-   \_porta di \_ \_ destinazione IP della condizione \_ FWPM
-   \_ \_ ID vswitch condizione \_ FWPM
-   \_tipo di \_ \_ rete vswitch condizione FWPM \_
-   FWPM \_ Condition \_ vswitch \_ \_ ID interfaccia di origine \_
-   FWPM \_ Condition \_ vswitch \_ \_ ID interfaccia di destinazione \_
-   FWPM \_ Condition \_ vswitch \_ \_ ID macchina virtuale di origine \_
-   FWPM \_ Condition \_ vswitch \_ \_ ID macchina virtuale di destinazione \_
-   FWPM \_ Condition \_ vswitch \_ \_ tipo di interfaccia di origine \_
-   FWPM \_ Condition \_ vswitch \_ \_ ID rete \_ tenant

## <a name="new-filtering-condition-flags"></a>Nuovi flag di condizione di filtro

[**Flag di condizione di filtro:**](filtering-condition-flags-.md)

-   il \_ flag di condizione FWP \_ è una \_ \_ \_ connessione proxy
-   il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback appcontainer
-   il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback non appcontainer \_
-   il \_ flag di condizione FWP \_ \_ sta \_ rispettando l' \_ \_ autorizzazione per i criteri
-   \_La condizione \_ FWP \_ L2 \_ è \_ Ethernet nativa
-   \_La condizione FWP \_ L2 \_ è \_ Wi-Fi
-   \_La condizione FWP \_ L2 \_ è \_ mobile \_ Broadband
-   \_La condizione \_ FWP \_ L2 \_ è \_ dati diretti Wi-Fi \_
-   \_La condizione FWP \_ L2 \_ è \_ VM2VM
-   \_La condizione FWP \_ L2 è un \_ \_ pacchetto in formato non valido \_
-   \_La condizione FWP \_ L2 è un gruppo di \_ \_ \_ frammenti IP \_
-   \_Condizione FWP \_ L2 \_ se \_ connettore \_ presente

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Aggiornamenti di Windows 7 alla piattaforma filtro Windows

Il documento [novità di Windows Filtering Platform descrive in]() dettaglio molti degli aggiornamenti effettuati per Windows 7. Le informazioni sono inoltre disponibili nel kit driver Windows sulle [modifiche al WFP per Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 