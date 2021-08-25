---
description: Windows Infrastruttura di gestione (WMI), Strumentazione gestione (MI) e Open Management Infrastructure (OMI) usano tutti file MOF (Management Object Format) per descrivere le informazioni rese disponibili tramite i rispettivi provider.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Provider WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682629f72da94cd2210fb781284a7cb4cf7f85868ff405f22727e619d128ae65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992419"
---
# <a name="wmimiomi-providers"></a>Provider WMI/MI/OMI

Windows Infrastruttura di gestione (WMI), Strumentazione gestione (MI) e Open Management Infrastructure (OMI) usano tutti file MOF (Management Object Format) per descrivere le informazioni rese disponibili tramite i rispettivi provider.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Il provider di Active Directory, noto anche come provider di servizi directory (DS), esegue il mapping degli oggetti di Active Directory a WMI. Accedendo allo spazio dei nomi Lightweight Directory Access Protocol (LDAP) in WMI, è possibile fare riferimento a un oggetto o impostarsi come alias in Active Directory.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventario delle applicazioni](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

Le classi WMI per Application Inventory consentono l'individuazione delle applicazioni Win32 installate e Windows archiviare le applicazioni in un Windows sistema.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Application Proxy provider WMI consente agli sviluppatori di accedere al servizio Web Application Proxy in modo che gli amministratori possano pubblicare applicazioni per l'accesso esterno. Web Application Proxy è un proxy inverso per Active Directory Federation Services (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Crittografia unità BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Fornisce la configurazione e la gestione per un'area di archiviazione in un'unità disco rigido, rappresentata da un'istanza di [**Win32 \_ EncryptableVolume,**](/windows/desktop/SecProv/win32-encryptablevolume)che può essere protetta tramite crittografia.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[Bit](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

Il Servizio trasferimento intelligente in background (BITS) Compact Server con gestione remota BITS consente agli amministratori autenticati o alle applicazioni controller di creare, modificare e gestire processi di trasferimento BITS in modalità remota senza usare il servizio Internet Information Services (IIS).

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Biztalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Fornisce l'accesso agli oggetti di amministrazione BizTalk rappresentati dalle classi WMI.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[dati configurazione di avvio](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

Il provider dati configurazione di avvio (BCD) fornisce un archivio usato per descrivere le applicazioni di avvio e le impostazioni dell'applicazione di avvio.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Agente di raccolta eventi di avvio](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

Il provider WMI dell'agente di raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità Installazione e raccolta eventi di avvio Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Eventi di risparmio energia](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

I provider CIMWin32 supportano le classi implementate in CimWin32.dll e sono costituiti dalle classi CIM di base, dall'implementazione Win32 di tali classi e da eventi di risparmio energia.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Il provider CIMWin32a estende le classi disponibili in [CIMWin32.](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

Il provider DcbQosCim supporta classi che descrivono i dati di impostazione di QOS di rete, i dati delle impostazioni di controllo e i dati di impostazione delle classi di traffico.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[file system distribuito (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

Il provider DFS fornisce funzioni DFS scriptable tramite WMI.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[file system distribuito replica (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Crea strumenti per la configurazione e il monitoraggio [del file system distribuito (DFS).](/previous-versions/windows/desktop/dfs/distributed-file-system) Per altre informazioni, vedere [Classi WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

Il provider [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) supporta le classi che implementano l'accesso allo spazio dei nomi DFS.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

Il provider [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) supporta le classi che interagiscono con un server DHCP (Dynamic Host Configuration Protocol).

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Quota disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

Il provider Windows disk quota consente agli amministratori di controllare la quantità di dati archiviati da ogni utente in un file system NTFS.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

Il provider DTC consente la gestione del DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[Dns](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Consente ad amministratori e programmatori di configurare Domain Name System record di risorse DNS (RR) e server DNS tramite WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Classi del provider Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Il provider Dnsclientcim supporta le classi che interagiscono con un client DOMAIN NAME SYSTEM (DNS).

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

Il provider [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) supporta le classi WMI che interagiscono con un client DNS.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

Il provider [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) supporta le classi WMI che interagiscono con un server DNS.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

Il provider [del registro](/previous-versions/windows/desktop/eventlogprov/event-log-provider) eventi fornisce l'accesso ai dati dal servizio registro eventi e la notifica degli eventi.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Gestione traccia eventi](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

Il provider Di gestione traccia eventi fornisce l'accesso alle configurazioni di sessione e agli eventi di traccia di Traccia eventi per Windows (ETW).

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Aggiornamento Cluster-Aware failover](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

Il provider di aggiornamento Cluster-Aware failover supporta il coordinamento e la gestione di Aggiornamento compatibile con cluster.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

Il provider Hyper-V clustering di failover fornisce la gestione e la creazione di report di Hyper-V in un ambiente di clustering.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Archiviazione QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

Il provider QoS (Quality of Service) Archiviazione Clustering di failover fornisce la gestione e la creazione di report dei criteri QoS di archiviazione cluster.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

Il provider del cluster di failover V1 fornisce la gestione di un cluster di failover.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Estensioni del cluster di failover V1](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

Il provider di estensioni del cluster di failover offre una gestione aggiuntiva di un cluster di failover.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

Il provider Health Monitor gateway gestisce le informazioni e gli eventi di monitoraggio dell'integrità del gateway.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Criteri di gruppo API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

Il provider Criteri di gruppo consente l'amministrazione basata su criteri tramite i servizi directory di Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Servizio Guardiano host](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

Il provider del servizio Guardiano host fornisce la gestione del servizio Guardiano host per le macchine virtuali schermate.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Il provider Hyper-V consente di gestire e recuperare informazioni sulle macchine virtuali.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Il provider Hyper-V (V2) estende il provider [Hyper-V.](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Espone le interfacce di programmazione che possono essere usate per eseguire query e configurare la metabase IIS.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Server di gestione degli indirizzi del protocollo Internet (Gestione indirizzi IP)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

Il provider Gestione indirizzi IP Server consente agli sviluppatori di gestire Gestione indirizzi IP tramite WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

Il provider di route IP preinstallato fornisce informazioni di routing di rete IPV4, incluse (ma non solo) le informazioni disponibili tramite il **comando route print.**

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[IpMI (Intelligent Platform Management Interface)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Fornisce i dati IPMI dalle operazioni di Baseboard Management Controller (BMC).

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

Il provider Server di destinazione iSCSI supporta un'interfaccia WMI per la gestione di Microsoft Server di destinazione iSCSI, ad esempio la creazione di dischi virtuali, e per la presentazione al client.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Oggetto processo](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

Il provider di oggetti processo supporta l'accesso ai dati sugli oggetti processo del kernel denominati.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Traccia kernel](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

Il provider di eventi traccia kernel preinstallato consente di visualizzare gli eventi di traccia del kernel per la creazione del processo, la terminazione del processo, la creazione di thread, la terminazione del thread e il caricamento del modulo.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Fornisce classi che creano, registrano, configurano, gestiscono applicazioni SIP (Session Initiation Protocol) personalizzate con [Live Communications Server 2003.](/previous-versions/office/aa194012(v=office.11))

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registro strumenti di gestione](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

Il provider del Registro di sistema degli strumenti di gestione fornisce l'accesso remoto al Registro di sistema.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Strumenti di gestione Gestione attività](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

Il provider di Gestione attività strumenti di gestione fornisce l'accesso e la gestione dei Gestione attività dati.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Applicazione MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

Il provider di applicazioni Gestione dispositivi mobili (MDM) gestisce le applicazioni nei dispositivi sottoscritti al servizio MDM.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

Il provider di bridge MDM consente la gestione MDM di un bridge di rete.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Gestione Impostazioni MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

Il provider Impostazioni MDM consente la gestione delle impostazioni nei dispositivi registrati con un servizio MDM.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

Il provider [ \_ MSFT PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) espone una classe che definisce una classe di visualizzazione per un computer fisico.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

La [sezione Provider MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) fornisce informazioni di riferimento per le classi del provider MsNetImPlatform implementate in NdisIMPlatCim.dll.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

Il provider [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) supporta le classi che accedono alle schede di rete.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

In questa sezione vengono fornite informazioni di riferimento per le classi del provider [NetDaCim.](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Fornisce informazioni di riferimento per le classi del provider [NetNcCim.](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

Il provider [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) supporta classi che interagiscono con l'infrastruttura di Branch Cache.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

Il provider [NetQosCim fornisce](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) i dati per i dati delle impostazioni QoS (Quality of Service) di rete.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

Questa sezione fornisce informazioni di riferimento per le classi del provider NetSwitchTeam dichiarate in NetSwitchTeam.mof e implementate in NetSwitchTeamCim.dll.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

Il provider NetTCPIP supporta classi che interagiscono con le connessioni TCPIP.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

Questa sezione fornisce informazioni di riferimento per le classi del provider NetTtCim definite in NetTtCim.mof e implementate in NetTtCim.dll.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

Il provider NetWNV supporta classi che interagiscono con le tecnologie di virtualizzazione di rete.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protezione accesso alla rete](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

Il provider di Protezione accesso alla rete espone una piattaforma per l'accesso protetto alle reti private.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Bilanciamento carico di rete](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

Il provider di Bilanciamento carico di rete consente la gestione di un cluster di Bilanciamento carico di rete.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

Il provider consente la gestione di un server controller di rete.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[Nfs](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

Il provider per NFS consente di creare strumenti e script per la configurazione e il monitoraggio Windows file system di rete.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Il provider Ping fornisce l'accesso alle informazioni sullo stato fornite dal comando ping standard.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Politica](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Fornisce estensioni ai criteri di gruppo e consente miglioramenti nell'applicazione dei criteri.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Contatore alimentazione](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

Il provider power meter supporta l'interfaccia di misurazione e budget alimentazione (PMB). Queste classi sono l'interfaccia principale per la query delle informazioni dell'interfaccia del contatore di alimentazione (POWER Meter Interface) dai contatori di alimentazione sottostanti nel sistema.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Criteri di risparmio energia](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

Il provider di Criteri di risparmio energia offre alle classi la possibilità di gestire in remoto tutta l'infrastruttura dei criteri di risparmio energia.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

Il provider [RAMgmtPSProvider fornisce](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) classi per gestire Accesso remoto.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

Il provider [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) fornisce le classi per gestire il server di accesso remoto.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

Il provider [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) espone le metriche di affidabilità del Windows e del registro eventi.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Servizi Desktop remoto](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Consente l'amministrazione coerente del server in Servizi Desktop remoto ambiente.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Definisce le classi che consentono di scrivere script e codice per modificare le impostazioni del server di report e del Gestione report.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Gruppo di criteri risultante (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Fornisce metodi per pianificare ed eseguire il debug delle impostazioni dei criteri in una situazione di what-if. Questi metodi consentono agli amministratori di determinare facilmente la combinazione di impostazioni dei criteri che si applicano a un utente o a un computer. Questo è noto come gruppo di criteri risultante (RSoP). Per altre informazioni, vedere [Informazioni sul provider di metodi WMI RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) e Classi WMI [RSoP.](/previous-versions/windows/desktop/Policy/rsop-wmi-classes)

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Sicurezza](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Recupera o modifica le impostazioni di sicurezza che controllano la proprietà, il controllo e i diritti di accesso a file, directory e condivisioni.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager.DeploymentProvider espone](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) la funzionalità di distribuzione.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sessione](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Gestisce le sessioni e le connessioni di rete.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Copia shadow](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Fornisce funzioni di gestione per le copie shadow della funzionalità Cartelle condivise.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Provisioning di macchine virtuali schermate](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

Il provider di provisioning di macchine virtuali schermate consente a un controller di infrastruttura di avviare il provisioning sicuro di una macchina virtuale schermata in un host Hyper-V.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Servizio di provisioning di macchine virtuali schermate](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

Il provider consente il provisioning di una macchina virtuale schermata.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

La libreria SMB API Gestione classi e metodi per gestire le condivisioni e condividere l'accesso.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[Snmp](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Mappe Simple Network Management Protocol (SNMP) definiti negli oggetti dello schema MIB (Management Information Base) alle classi. Per altre informazioni, vedere [Configurazione dell'ambiente SNMP WMI.](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment)

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

Il provider di Registrazione inventario software raccoglie i dati sulle licenze relative al software installato in un server Windows e fornisce l'accesso remoto ai dati in modo che possano essere aggregati facilmente da un data center.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licenze software per Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Classi di licenze](/previous-versions/windows/desktop/sppwmi/software-license-provider-) software usate per Windows Vista.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licenza software](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

Il provider di licenze software recupera i dati sulle licenze software.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Archiviazione Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

Il provider Archiviazione volume fornisce funzioni di gestione dei volumi.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Archiviazione Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

Il provider consente la gestione di una replica di archiviazione.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

Il provider del Registro di sistema consente alle applicazioni di gestione di recuperare e modificare i dati nel Registro di sistema e di ricevere notifiche quando si verificano modifiche.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Ripristino configurazione di sistema](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Fornisce classi che configurano e usano Ripristino configurazione di sistema funzionalità. Per altre informazioni, vedere [Configuring Ripristino configurazione di sistema](/windows/desktop/sr/configuring-system-restore) and the Ripristino configurazione di sistema [WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Fornisce l'accesso ai dati relativi a un dispositivo di sicurezza, rappresentato da un'istanza di [**\_ TPM Win32,**](/windows/desktop/SecProv/win32-tpm)che rappresenta la radice di attendibilità per un sistema di computer microsoft Windows piattaforma attendibile.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

Il provider [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) è un provider di istanze che crea classi con informazioni sulle relazioni di trust tra domini.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Registrazione dell'accesso utente](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

Registrazione accesso utenti è un framework comune che consente ai ruoli Windows Server di segnalare le rispettive metriche di utilizzo.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

Il provider [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) espone le classi che forniscono informazioni su un profilo utente in un sistema Windows, nonché lo stato di integrità di una cartella utente reindirizzata.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Gestione dello stato utente](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

Il provider User State Management espone un'API di gestione e creazione di report per scenari aziendali.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Mostra](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Crea nuove istanze e metodi basati su istanze di altre classi. Nelle piattaforme a 64 bit sono disponibili due versioni del provider View.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[Provider VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

Il provider [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) espone una piattaforma per l'automazione della connettività a un client di rete privata virtuale.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[Wdm](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Fornisce l'accesso a classi, istanze, metodi ed eventi dei driver hardware conformi al modello Windows Driver Model (WDM).

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

Il provider [WFasCim espone](/previous-versions/windows/desktop/wfascimprov/network-security-classes) le funzionalità di filtro e sicurezza di rete.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

Il provider [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) espone informazioni sulla firma digitale sui driver.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

Il provider [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) espone i timestamp correnti, locali e basati su UTC in un computer.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Componenti di accesso ai dati (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Fornisce la gestione di WDAC.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

Il provider Windows Defender espone le Windows Defender di sicurezza.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

Il provider Windows Installer, noto anche come provider MSI, consente alle applicazioni di accedere alle informazioni raccolte Windows applicazioni conformi al programma di installazione.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Attivazione del prodotto](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

Il provider Windows product activation (WPA) è una tecnologia anti-piracy finalizzata a ridurre la copia casuale del software.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

Il provider consente l'accesso e la gestione della configurazione controllata dall'Server Manager applicazione.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Gestione Archiviazione server (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

Il provider MsftStrgMan fornisce la gestione per i sistemi di archiviazione Windows Server.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[gestione Windows Archiviazione (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

Il provider StrgMgmt può essere usato per gestire un'ampia gamma di configurazioni di archiviazione, dai tablet agli array di archiviazione esterni nei server.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

Lo Windows System Assessment Tool (WinSAT) espone diverse classi che valutano le caratteristiche e le funzionalità delle prestazioni di un computer.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

Il provider WMI Core definisce le classi che costituiscono le funzionalità di base di WMI.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

Il provider [Msft \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) supporta i provider.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32 \_ Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

La [**classe astratta \_ Win32 Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) è la classe di base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) e [**Win32 \_ PerfFormattedData.**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov) Definisce le proprietà timestamp e frequency necessarie usate negli algoritmi CounterType per le classi dei contatori delle prestazioni.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Classe di base astratta per le classi di dati calcolate preinstallato.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

La classe del contatore delle [**prestazioni Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) è la classe di base astratta per tutte le classi di contatori delle prestazioni non elaborati concrete. Per essere visualizzate in Monitoraggio di sistema, le classi dei contatori delle prestazioni devono essere aggiunte allo spazio dei nomi "Root CIMv2" e derivate \\ da **Win32 \_ PerfRawData.**

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Crea le classi del [contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI . I dati vengono forniti dinamicamente a queste classi di prestazioni dal provider WMIPerfInst.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Fornisce dati non elaborati e formattati dei contatori delle prestazioni in modo dinamico dalle [definizioni della classe del contatore delle](/windows/desktop/CIMWin32Prov/performance-counter-classes) prestazioni.

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Cartelle di lavoro](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Cartelle di lavoro viene usato per sincronizzare i file con più PC e dispositivi mobili.

</dd> </dl>

 

 
