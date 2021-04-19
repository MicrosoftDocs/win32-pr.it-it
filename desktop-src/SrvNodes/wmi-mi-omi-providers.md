---
description: Windows Management Infrastructure (WMI), Strumentazione gestione (MI) e Open Management Infrastructure (OMI) utilizzano i file MOF (Management Object Format) per descrivere le informazioni rese disponibili tramite i rispettivi provider.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Provider WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319908"
---
# <a name="wmimiomi-providers"></a><span data-ttu-id="fb4c7-103">Provider WMI/MI/OMI</span><span class="sxs-lookup"><span data-stu-id="fb4c7-103">WMI/MI/OMI Providers</span></span>

<span data-ttu-id="fb4c7-104">Windows Management Infrastructure (WMI), Strumentazione gestione (MI) e Open Management Infrastructure (OMI) utilizzano i file MOF (Management Object Format) per descrivere le informazioni rese disponibili tramite i rispettivi provider.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-104">Windows Management Infrastructure (WMI), Management Instrumentation (MI) and Open Management Infrastructure (OMI) all use Management Object Format (MOF) files to describe the information made available through their respective providers.</span></span>

<dl> <dt>

<span data-ttu-id="fb4c7-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-106">Il provider di Active Directory, noto anche come provider di servizi directory (DS), esegue il mapping Active Directory oggetti a WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-106">The Active Directory provider, also known as the Directory Services (DS) provider, maps Active Directory objects to WMI.</span></span> <span data-ttu-id="fb4c7-107">Accedendo allo spazio dei nomi LDAP (Lightweight Directory Access Protocol) in WMI, è possibile fare riferimento a un oggetto o renderlo un alias nel Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-107">By accessing the Lightweight Directory Access Protocol (LDAP) namespace in WMI, you can reference or make an object an alias in the Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventario delle applicazioni](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Application Inventory](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-109">Le classi WMI per l'inventario delle applicazioni consentono l'individuazione delle applicazioni Win32 installate e delle applicazioni Windows Store in un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-109">The WMI classes for Application Inventory enable discovery of the installed Win32 applications and Windows store applications on a Windows system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Proxy di applicazione](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-111">Il provider WMI del proxy di applicazione consente agli sviluppatori di accedere al servizio proxy applicazione Web in modo che gli amministratori possano pubblicare applicazioni per l'accesso esterno.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-111">Application Proxy WMI Provider enables developers to access the Web Application Proxy service so administrators can publish applications for external access.</span></span> <span data-ttu-id="fb4c7-112">Proxy applicazione Web è un proxy inverso per Active Directory Federation Services (AD FS).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-112">Web Application Proxy is a reverse proxy for Active Directory Federation Services (AD FS).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Crittografia unità BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker Drive Encryption (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-114">Fornisce la configurazione e la gestione di un'area di archiviazione in un'unità disco rigido, rappresentata da un'istanza di [**Win32 \_ EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), che può essere protetta usando la crittografia.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-114">Provides configuration and management for an area of storage on a hard disk drive, represented by an instance of [**Win32\_EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), that can be protected by using encryption.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-115"><span id="BITS"></span><span id="bits"></span>[BIT](/previous-versions/windows/desktop/bitsprov/bits-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-116">La Servizio trasferimento intelligente in background (BITS) Compact Server con gestione remota BITS consente agli amministratori autenticati o alle applicazioni controller di creare, modificare e gestire i processi di trasferimento BITS in modalità remota senza utilizzare il servizio Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-116">The Background Intelligent Transfer Service (BITS) Compact Server with BITS Remote Management allows authenticated administrators or controller applications to create, modify and manage BITS transfer jobs remotely without using the Internet Information Services (IIS) service.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-118">Fornisce accesso agli oggetti di amministrazione BizTalk rappresentati dalle classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-118">Supplies access to the BizTalk administration objects represented by WMI classes.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[dati configurazione di avvio](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Boot Configuration Data](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-120">Il provider di dati configurazione di avvio (BCD) fornisce un archivio utilizzato per descrivere le applicazioni di avvio e le impostazioni dell'applicazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-120">The Boot Configuration Data (BCD) provider provides a store that is used to describe boot applications and boot application settings.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Agente di raccolta eventi di avvio](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Boot Event Collector](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-122">Il provider WMI raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità di raccolta degli eventi di avvio e di installazione in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-122">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, eventi di risparmio energia](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Power Management Events](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-124">I provider CIMWin32 supportano le classi implementate in CimWin32.dll e sono costituite dalle classi CIM principali, dall'implementazione Win32 di tali classi e dagli eventi di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-124">The CIMWin32 providers support the classes implemented in CimWin32.dll, and consist of the core CIM classes, the Win32 implementation of those classes, and power management events.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-126">Il provider CIMWin32a estende le classi disponibili in [cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-126">The CIMWin32a provider extends the classes available in the [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-128">Il provider DcbQosCim supporta classi che descrivono i dati delle impostazioni QOS di rete, i dati delle impostazioni di controllo e i dati di impostazione della classe di traffico.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-128">The DcbQosCim provider supports classes that describe Network QOS setting data, control setting data, and traffic class setting data.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[File system distribuito (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Distributed File System (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-130">Il provider DFS fornisce funzioni DFS tramite script tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-130">The DFS provider supplies scriptable DFS functions through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Replica di file system distribuito (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-132">Consente di creare strumenti per la configurazione e il monitoraggio del servizio [file System distribuito (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-132">Creates tools for configuring and monitoring the [Distributed File System (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) service.</span></span> <span data-ttu-id="fb4c7-133">Per altre informazioni, vedere [classi WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-133">For more information, see [DFSR WMI Classes](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-135">Il provider [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) supporta le classi che implementano l'accesso allo spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-135">The [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) provider supports classes that implement DFS namespace access.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-137">Il provider [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) supporta le classi che interagiscono con un server DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-137">The [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) provider supports classes that interact with a dynamic host configuration protocol (DHCP) server.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Quota disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Disk Quota](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-139">Il provider di quote disco di Windows consente agli amministratori di controllare la quantità di dati archiviata da ogni utente in un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-139">The Windows Disk Quota provider allows administrators to control the amount of data that each user stores on an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-141">Il provider DTC consente la gestione di DTC.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-141">The DTC provider enables management of the DTC.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-143">Consente agli amministratori e ai programmatori di configurare i record di risorse DNS (Domain Name System) e i server DNS con WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-143">Enables administrators and programmers to configure Domain Name System (DNS) resource records (RRs) and DNS Servers using WMI.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Classi provider Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim Provider Classes](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-145">Il provider Dnsclientcim supporta le classi che interagiscono con un client di Domain Name System (DNS).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-145">The Dnsclientcim provider supports classes that interact with a Domain Name System (DNS) client.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-147">Il provider [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) supporta le classi WMI che interagiscono con un client DNS.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-147">The [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) provider supports WMI classes that interact with a DNS client.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-149">Il provider [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) supporta le classi WMI che interagiscono con un server DNS.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-149">The [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) provider supports WMI classes that interact with a DNS server.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-151">Il provider del [registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) fornisce l'accesso ai dati dal servizio Registro eventi e la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-151">The [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supplies access to data from the event log service, and notification of events.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Gestione traccia eventi](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Event Tracing Management](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-153">Il provider di gestione traccia eventi consente l'accesso alle configurazioni di sessione e agli eventi di traccia di Event Tracing for Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-153">The Event Tracing Management provider provides access to Event Tracing for Windows (ETW) autologger session configurations and trace events.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Aggiornamento del Cluster-Aware di failover](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Updating](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-155">Il provider di failover Cluster-Aware Updating (aggiornamento compatibile con cluster) supporta il coordinamento e la gestione di aggiornamento compatibile con cluster.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-155">The Failover Cluster-Aware Updating (CAU) provider supports coordination with and management of CAU.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clustering di failover Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-157">Il provider Hyper-V per il clustering di failover fornisce la gestione e la creazione di report di Hyper-V in un ambiente di clustering.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-157">The Failover Clustering Hyper-V provider provides management and reporting of Hyper-V in a clustering environment.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[QoS di archiviazione di clustering di failover](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-159">Il provider di qualità del servizio (QoS) di archiviazione per il clustering di failover fornisce la gestione e la creazione di report dei criteri QoS di archiviazione di clustering.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-159">The Failover Clustering Storage Quality of Service (QoS) provider provides management and reporting of the clustering storage QoS policies.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Provider del cluster di failover V1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-161">Il provider del cluster di failover V1 fornisce la gestione di un cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-161">The Failover Cluster V1 provider provides management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Estensioni del cluster di failover V1](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failover Cluster V1 Extensions](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-163">Il provider delle estensioni del cluster di failover fornisce una gestione aggiuntiva di un cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-163">The Failover Cluster Extensions provider provides additional management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Monitoraggio dell'integrità del gateway](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-165">Il provider di monitoraggio dell'integrità del gateway gestisce gli eventi e le informazioni di monitoraggio dell'integrità del gateway.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-165">The Gateway Health Monitor provider manages gateway health monitoring events and information.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[API Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Group Policy API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-167">Il provider Criteri di gruppo consente l'amministrazione basata su criteri utilizzando i servizi directory Microsoft Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-167">The Group Policy provider enables policy-based administration using Microsoft Active Directory (AD) directory services.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Servizio sorveglianza host](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host Guardian Service](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-169">Il provider del servizio sorveglianza host fornisce la gestione del servizio sorveglianza host per le macchine virtuali schermate.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-169">The Host Guardian Service provider provides management of the Host Guardian Service for shielded VMs.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-171">Il provider Hyper-V consente di gestire e recuperare le informazioni sulle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-171">The Hyper-V provider allows you to manage and retrieve information about virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-173">Il provider Hyper-V (v2) estende il provider [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-173">The Hyper-V (V2) provider extends the [Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) provider.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="fb4c7-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-175">Espone le interfacce di programmazione che possono essere utilizzate per eseguire query e configurare la metabase IIS.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-175">Exposes programming interfaces that can be used to query and configure the IIS metabase.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Server gestione indirizzi IP](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internet Protocol Address Management (IPAM) Server](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-177">Il provider del server di gestione indirizzi IP consente agli sviluppatori di gestire gestione indirizzi IP tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-177">The IPAM Server Provider enables developers to manage IPAM through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-179">Il provider di route IP preinstallato fornisce informazioni sul routing di rete IPV4, incluse le informazioni disponibili tramite il comando **Route Print** .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-179">The preinstalled IP Route provider supplies IPV4 network routing information, including (but not limited to) the information available through the **route print** command.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Interfaccia di gestione piattaforma intelligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-181">Fornisce dati IPMI dalle operazioni del controller di gestione battiscopa (BMC).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-181">Supplies IPMI data from Baseboard Management Controller (BMC) operations.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI Target Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-183">Il provider del server di destinazione iSCSI supporta un'interfaccia WMI per la gestione del server di destinazione iSCSI Microsoft, ad esempio la creazione di dischi virtuali e la relativa presentazione al client.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-183">The iSCSI Target Server provider supports a WMI interface for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Oggetto processo](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job Object](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-185">Il provider di oggetti processo supporta l'accesso ai dati relativi agli oggetti processo kernel denominati.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-185">The Job Object provider supports access to data about named kernel job objects.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Traccia del kernel](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel Trace](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-187">Il provider di eventi di traccia del kernel preinstallato consente di visualizzare gli eventi di traccia del kernel durante la creazione, la terminazione dei processi, la creazione di thread, la terminazione del thread e il carico del modulo.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-187">The preinstalled Kernel Trace event provider allows you to see kernel trace events on Process creation, Process termination, Thread creation, Thread termination and module load.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span><span class="sxs-lookup"><span data-stu-id="fb4c7-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-189">Fornisce classi per la creazione, la registrazione, la configurazione e la gestione di applicazioni SIP (Session Initiation Protocol) personalizzate con [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-189">Provides classes that create, register, configure, manage custom Session Initiation Protocol (SIP) applications with the [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registro degli strumenti di gestione](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Management Tools Registry](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-191">Il provider del registro di sistema di strumenti di gestione fornisce accesso remoto al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-191">The Management Tools Registry provider provides remote access to the registry.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Gestione attività di strumenti di gestione](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Management Tools Task Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-193">Il provider Gestione attività di strumenti di gestione consente di accedere e gestire i dati di gestione attività.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-193">The Management Tools Task Manager provider provides access and management of the Task Manager data.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Applicazione MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM Application](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-195">Il provider di applicazioni di gestione di dispositivi mobili (MDM) gestisce le applicazioni nei dispositivi che hanno sottoscritto il servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-195">The Mobile Device Management (MDM) application provider manages applications on devices that are subscribed to the MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Bridge MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-197">Il provider del Bridge MDM consente la gestione MDM di un Bridge di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-197">The MDM Bridge provider enables MDM management of a network bridge.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Impostazioni MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM Settings](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-199">Il provider di impostazioni MDM consente la gestione delle impostazioni nei dispositivi registrati con un servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-199">The MDM Settings Provider enables management of settings on devices enrolled with a MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-201">Il provider [MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) espone una classe che definisce una classe di visualizzazione per un sistema di computer fisico.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-201">The [MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) provider exposes a class that defines a view class for a physical computer system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-203">La sezione provider [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) fornisce informazioni di riferimento per le classi del provider MsNetImPlatform implementate in NdisIMPlatCim.dll.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-203">The [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) provider section provides reference information for MsNetImPlatform provider classes implemented in NdisIMPlatCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-205">Il provider [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) supporta le classi che accedono alle schede di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-205">The [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) provider supports classes that access network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-207">In questa sezione vengono fornite informazioni di riferimento per le classi del provider [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-207">This section provides reference information for [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) Provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-209">Fornisce informazioni di riferimento per le classi del provider [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-209">Provides reference information for [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-211">Il provider [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) supporta le classi che interagiscono con l'infrastruttura della cache di Branch.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-211">The [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) provider supports classes that interact with the Branch Cache infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-213">Il provider [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) fornisce dati per i dati di impostazione qualità del servizio (QoS) e QoS di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-213">The [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) provider supplies data for network quality of service (QoS) and QoS setting data.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-215">In questa sezione vengono fornite informazioni di riferimento per le classi del provider NetSwitchTeam dichiarate in NetSwitchTeam. mof e implementate in NetSwitchTeamCim.dll.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-215">This section provides reference information for NetSwitchTeam provider classes declared in NetSwitchTeam.mof and implemented in NetSwitchTeamCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-217">Il provider NetTCPIP supporta le classi che interagiscono con le connessioni TCPIP.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-217">The NetTCPIP provider supports classes that interact with TCPIP connections.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-219">In questa sezione vengono fornite informazioni di riferimento per le classi del provider NetTtCim definite in NetTtCim. mof e implementate in NetTtCim.dll.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-219">This section provides reference information for NetTtCim provider classes defined in NetTtCim.mof and implemented in NetTtCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-221">Il provider NetWNV supporta le classi che interagiscono con le tecnologie di virtualizzazione NET.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-221">The NetWNV provider supports classes that interact with net virtualization technologies.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Protezione accesso alla rete](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Network Access Protection](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-223">Il provider di protezione accesso alla rete espone una piattaforma per l'accesso protetto alle reti private.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-223">The Network Access Protection provider exposes a platform for protected access to private networks.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Bilanciamento carico di rete](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Network Load Balancing](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-225">Il provider di bilanciamento carico di rete (NLB) consente la gestione di un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-225">The Network Load Balancing (NLB) Provider enables management of a NLB cluster.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Server NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-227">Il provider consente la gestione di un server del controller di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-227">The provider enables management of a network controller server.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-229">Il provider per NFS consente di creare strumenti e script per la configurazione e il monitoraggio del file System di rete Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-229">The provider for NFS allows you to create tools and scripts for configuring and monitoring the Windows Network File System.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-231">Il provider ping fornisce accesso alle informazioni sullo stato fornite dal comando ping standard.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-231">The Ping provider supplies access to the status information provided by the standard ping command.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Politica](/previous-versions/windows/desktop/policmanprov/policy-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-233">Fornisce estensioni ai criteri di gruppo e consente il perfezionamento nell'applicazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-233">Provides extensions to group policy, and permits refinements in the application of policy.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Contatore energia elettrica](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Power Meter](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-235">Il provider del Power Meter supporta l'interfaccia di controllo del risparmio di energia (PMB).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-235">The Power Meter provider supports the Power Metering and Budgeting (PMB) interface.</span></span> <span data-ttu-id="fb4c7-236">Queste classi sono l'interfaccia principale per la query delle informazioni sull'interfaccia di Power Meter (PMI) provenienti da contatori di potenza sottostanti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-236">These classes are the primary interface for the query of Power Meter Interface (PMI) information from underlying power meters on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Criteri di risparmio energia](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Power Policy](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-238">Il provider di criteri di risparmio energia fornisce alle classi la possibilità di gestire in remoto tutta l'infrastruttura dei criteri di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-238">The Power Policy provider provides classes the ability to remotely manage all the power policy infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-240">Il provider [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) fornisce le classi per gestire l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-240">The [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) provider provides classes to manage Remote Access.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-242">Il provider [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) fornisce le classi per gestire il server di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-242">The [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) provider provides classes to manage the Remote Access Server.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-244">Il provider [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) espone le metriche di affidabilità del registro eventi di sistema e di Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-244">The [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) provider exposes system and Windows Event Log reliability metrics.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Servizi Desktop remoto](/windows/desktop/TermServ/terminal-services-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remote Desktop Services](/windows/desktop/TermServ/terminal-services-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-246">Consente l'amministrazione coerente del server in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-246">Enables consistent server administration in a Remote Desktop Services environment.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-248">Definisce le classi che consentono di scrivere script e codice per modificare le impostazioni del server di report e del Gestione report.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-248">Defines classes that allow you to write scripts and code to modify the settings of the report server and the Report Manager.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Gruppo di criteri risultante (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultant Set of Policy (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-250">Fornisce metodi per pianificare ed eseguire il debug delle impostazioni dei criteri in una situazione di simulazione.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-250">Supplies methods to plan and debug policy settings in a what-if situation.</span></span> <span data-ttu-id="fb4c7-251">Questi metodi consentono agli amministratori di determinare facilmente la combinazione di impostazioni dei criteri che si applicano o si applicano a un utente o un computer.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-251">These methods allow administrators to determine easily the combination of policy settings that apply to, or will apply to, a user or computer.</span></span> <span data-ttu-id="fb4c7-252">Questa operazione è nota come gruppo di criteri risultante.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-252">This is known as the Resultant Set of Policy (RSoP).</span></span> <span data-ttu-id="fb4c7-253">Per ulteriori informazioni, vedere [informazioni sul provider di metodi WMI RSoP e sulle](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) [classi WMI RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-253">For more information, see [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) and [RSoP WMI Classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Sicurezza](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Security](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-255">Recupera o modifica le impostazioni di sicurezza che controllano la proprietà, il controllo e i diritti di accesso a file, directory e condivisioni.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-255">Retrieves or changes security settings that control ownership, auditing, and access rights to files, directories, and shares.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-257">[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) espone la funzionalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-257">The [ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) exposes deployment functionality.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sessione](/previous-versions/windows/desktop/wmipsess/session-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-259">Gestisce le sessioni e le connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-259">Manages network sessions and connections.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Copia shadow](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Shadow Copy](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-261">Fornisce funzioni di gestione per le copie shadow della funzionalità cartelle condivise.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-261">Supplies management functions for the Shadow Copies of the Shared Folders feature.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Provisioning di macchine virtuali schermate](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Shielded VM Provisioning](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-263">Il provider di provisioning di macchine virtuali schermate consente a un controller di infrastruttura di avviare il provisioning sicuro di una macchina virtuale schermata in un host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-263">The Shielded VM Provisioning provider enables a fabric controller to start the secure provisioning of a shielded VM on a Hyper-V host.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Servizio di provisioning di macchine virtuali schermate](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Shielded VM Provisioning Service](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-265">Il provider Abilita il provisioning di una macchina virtuale schermata.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-265">The provider enables provisioning of a shielded virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB Management](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-267">L'API di gestione SMB fornisce le classi e i metodi per gestire le condivisioni e condividere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-267">The SMB Management API provides classes and methods to manage shares and share access.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-269">Esegue il mapping di oggetti Simple Network Management Protocol (SNMP) definiti negli oggetti dello schema MIB (Management Information Base) alle classi.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-269">Maps Simple Network Management Protocol (SNMP) objects that are defined in Management Information Base (MIB) schema objects to classes.</span></span> <span data-ttu-id="fb4c7-270">Per ulteriori informazioni, vedere [configurazione dell'ambiente WMI SNMP](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-270">For more information, see [Setting up the WMI SNMP Environment](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Software Inventory Logging](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-272">Il provider di registrazione inventario software raccoglie i dati sulle licenze del software installato in un server Windows e fornisce l'accesso remoto ai dati in modo che possano essere aggregati facilmente da un Data Center.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-272">The Software Inventory Logging provider collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licenze software per Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Licensing for Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-274">[Classi di licenze software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) utilizzate per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-274">[Software Licensing Classes](/previous-versions/windows/desktop/sppwmi/software-license-provider-) used for Windows Vista.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licenza software](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software License](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-276">Il provider di licenze software recupera i dati relativi alle licenze software.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-276">The Software Licensing provider retrieves software licensing data.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Volume di archiviazione](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-278">Il provider del volume di archiviazione fornisce funzioni di gestione del volume.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-278">The Storage Volume provider supplies volume management functions.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Replica archiviazione](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-280">Il provider consente la gestione di una replica di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-280">The provider enables management of a storage replica.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-282">Il provider del registro di sistema consente alle applicazioni di gestione di recuperare e modificare i dati nel registro di sistema e di ricevere notifiche quando si verificano modifiche.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-282">The System Registry provider enables management applications to retrieve and modify data in the system registry, and receive notifications when changes occur.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Ripristino configurazione di sistema](/windows/desktop/sr/system-restore-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Restore](/windows/desktop/sr/system-restore-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-284">Fornisce classi che configurano e usano la funzionalità di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-284">Supplies classes that configure and use System Restore functionality.</span></span> <span data-ttu-id="fb4c7-285">Per ulteriori informazioni, vedere [configurazione del ripristino del sistema](/windows/desktop/sr/configuring-system-restore) e delle [classi WMI di ripristino](/windows/desktop/sr/system-restore-wmi-classes)del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-285">For more information, see [Configuring System Restore](/windows/desktop/sr/configuring-system-restore) and the [System Restore WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-287">Consente di accedere ai dati relativi a un dispositivo di sicurezza, rappresentato da un'istanza di [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm), che è la radice di attendibilità di un sistema di computer della piattaforma attendibile Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-287">Provides access to data about a security device, represented by an instance of [**Win32\_TPM**](/windows/desktop/SecProv/win32-tpm), that is the root of trust for a Microsoft Windows trusted platform computer system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-289">Il provider [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) è un provider di istanze che crea classi con informazioni sulle relazioni di trust tra i domini.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-289">The [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) provider is an instance provider that creates classes with information about the trust relationships between domains.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Registrazione accesso utenti](/previous-versions/windows/desktop/ual/user-access-logging)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[User Access Logging](/previous-versions/windows/desktop/ual/user-access-logging)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-291">Registrazione accesso utenti (registrazione accesso utenti) è un Framework comune per i ruoli di Windows Server per segnalare le rispettive metriche di consumo.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-291">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-293">Il provider [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) espone le classi che forniscono informazioni su un profilo utente in un sistema Windows, nonché lo stato di integrità di una cartella utente reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-293">The [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) provider exposes classes that provide information about a user profile on a Windows system, as well as the health status of a redirected user folder.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Gestione stato utente](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[User State Management](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-295">Il provider di gestione dello stato utente espone un'API di gestione e creazione di report per gli scenari aziendali.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-295">The User State Management provider exposes a management and reporting API for enterprise scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[Visualizzare](/windows/desktop/WmiSdk/view-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[View](/windows/desktop/WmiSdk/view-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-297">Crea nuove istanze e metodi in base alle istanze di altre classi.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-297">Creates new instances and methods based on instances of other classes.</span></span> <span data-ttu-id="fb4c7-298">Sulle piattaforme a 64 bit sono disponibili due versioni del provider di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-298">Two versions of the View provider are available on 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-300">Il provider [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) espone una piattaforma per l'automazione della connettività a un client di rete privata virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-300">The [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) provider exposes a platform for automating connectivity to a virtual private network client.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-302">Consente di accedere alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-302">Provides access to the classes, instances, methods, and events of hardware drivers that conform to the Windows Driver Model (WDM).</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-304">Il provider [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) espone le funzionalità di filtro e sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-304">The [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) provider exposes network security and filtering features.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-306">Il provider [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) espone informazioni sulla firma digitale sui driver.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-306">The [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) provider exposes digital signature information about drivers.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-308">Il provider [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) espone i timestamp correnti, locali e UTC in un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-308">The [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) provider exposes the current, local, and UTC-based timestamps on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-310">Fornisce la gestione di WDAC.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-310">Provides management of WDAC.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-312">Il provider di Windows Defender espone le funzionalità di sicurezza di Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-312">The Windows Defender provider exposes Windows Defender security features.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-314">Il provider di Windows Installer, noto anche come provider MSI, consente alle applicazioni di accedere alle informazioni raccolte da Windows Installer le applicazioni conformi.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-314">The Windows Installer provider, also known as the MSI provider allows applications to access information collected from Windows Installer compliant applications.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Attivazione del prodotto Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Product Activation](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-316">Il provider di attivazione del prodotto Windows (WPA) è una tecnologia anti-pirateria mirata a ridurre la copia occasionale del software.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-316">The Windows Product Activation (WPA) provider is an anti-piracy technology aimed at reducing the casual copying of software.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Server Manager di Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-318">Il provider consente l'accesso e la gestione della configurazione controllata dall'applicazione Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-318">The provider enables access to and management of the configuration controlled by the Server Manager application.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Gestione archiviazione Windows Server (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-320">Il provider MsftStrgMan fornisce la gestione dei sistemi di archiviazione nei prodotti Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-320">The MsftStrgMan provider provides management for storage systems on Windows Server products.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Gestione archiviazione Windows (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-322">Il provider StrgMgmt può essere usato per gestire un'ampia gamma di configurazioni di archiviazione, da tablet ad array di archiviazione esterni nei server.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-322">The StrgMgmt provider can be used to manage a wide range of storage configurations, from tablets to external storage arrays on servers.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Strumento valutazione sistema Windows](/windows/desktop/WinSAT/winsat-mof-classes)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-324">Lo strumento di valutazione del sistema Windows (WinSAT) espone alcune classi che valutano le caratteristiche e le funzionalità delle prestazioni di un computer.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-324">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Core WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-326">Il provider di base WMI definisce le classi che costituiscono la funzionalità principale di WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-326">The WMI Core provider defines classes that compose the core functionality of WMI.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[MSFT \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-328">Il provider [MSFT \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) supporta i provider.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-328">The [Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) provider supports providers.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[\_Prestazioni Win32](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32\_Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-330">La classe astratta [**\_ Perf Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) è la classe base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) e [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span><span class="sxs-lookup"><span data-stu-id="fb4c7-330">The [**Win32\_Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) abstract class is the base class for the performance counter classes [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) and [**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span></span> <span data-ttu-id="fb4c7-331">Definisce le proprietà timestamp e Frequency richieste utilizzate negli algoritmi CounterType per le classi del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-331">It defines the required timestamp and frequency properties used in the CounterType algorithms for the performance counter classes.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_PerfFormattedData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-333">Classe di base astratta per le classi di dati calcolate pre-installate.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-333">An abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_PerfRawData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-335">La classe del contatore delle prestazioni [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) è la classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-335">The performance counter class [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) is the abstract base class for all concrete raw performance counter classes.</span></span> <span data-ttu-id="fb4c7-336">Per essere visualizzati in monitoraggio di sistema, le classi del contatore delle prestazioni devono essere aggiunte allo \\ spazio dei nomi "root CIMv2" e derivate da **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-336">To appear in System Monitor, performance counter classes must be added to the "Root\\CIMv2" namespace and derived from **Win32\_PerfRawData**.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-338">Crea le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-338">Creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="fb4c7-339">I dati vengono forniti dinamicamente a queste classi di prestazioni dal provider WMIPerfInst.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-339">Data is dynamically supplied to these performance classes by the WMIPerfInst provider.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-341">Fornisce dati del contatore delle prestazioni non elaborati e formattati dinamicamente dalle definizioni [delle classi dei contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) .</span><span class="sxs-lookup"><span data-stu-id="fb4c7-341">Supplies raw and formatted performance counter data dynamically from [Performance Counter Class](/windows/desktop/CIMWin32Prov/performance-counter-classes) definitions.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c7-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Cartelle di lavoro](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span><span class="sxs-lookup"><span data-stu-id="fb4c7-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Work Folders](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span></span>
</dt> <dd>

<span data-ttu-id="fb4c7-343">Cartelle di lavoro consente di sincronizzare i file con più PC e dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="fb4c7-343">Work Folders is used to synchronize files with multiple PCs and mobile devices.</span></span>

</dd> </dl>

 

 
