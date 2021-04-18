---
description: A partire da Windows Vista, WMI contiene numerose nuove funzionalità basate su richieste da parte degli utenti WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Novità di Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318841"
---
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="08404-103">Novità di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08404-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="08404-104">A partire da Windows Vista, WMI contiene numerose nuove funzionalità basate su richieste da parte degli utenti WMI.</span><span class="sxs-lookup"><span data-stu-id="08404-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="08404-105">Nuovo strumento per la risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="08404-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="08404-106">Nuove funzionalità di sicurezza in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08404-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="08404-107">Altre nuove funzionalità di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08404-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="08404-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08404-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="08404-109">Nuovo strumento per la risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="08404-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="08404-110">Per il download è disponibile un nuovo strumento per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="08404-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="08404-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilità di diagnosi di WMI</span><span class="sxs-lookup"><span data-stu-id="08404-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="08404-112">Questa utilità esamina lo stato corrente del servizio WMI e i componenti correlati, le impostazioni DCOM e le impostazioni del registro di sistema nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="08404-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="08404-113">L'utilità segnala problemi e offre suggerimenti per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="08404-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="08404-114">Per ulteriori informazioni e per scaricare l'utilità, vedere [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="08404-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="08404-115">Nuove funzionalità di sicurezza in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08404-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="08404-116">Nell'elenco seguente sono elencate le nuove funzionalità di sicurezza WMI disponibili in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08404-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="08404-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Traccia e registrazione degli eventi</span><span class="sxs-lookup"><span data-stu-id="08404-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="08404-118">Il servizio WMI non utilizza più la maggior parte dei [file di log WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="08404-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="08404-119">USA invece [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed eventi sono disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="08404-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="08404-120">Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="08404-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Impostazione della sicurezza dello spazio dei nomi WMI nel file MOF</span><span class="sxs-lookup"><span data-stu-id="08404-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="08404-122">Il qualificatore **NamespaceSecuritySDDL** può essere usato per proteggere qualsiasi spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="08404-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="08404-123">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="08404-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Controllo di sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="08404-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="08404-125">WMI utilizza gli elenchi di controllo di accesso di sistema (SACL) dello spazio dei nomi per controllare l'attività dello spazio dei nomi e segnalare gli eventi al registro eventi di protezione.</span><span class="sxs-lookup"><span data-stu-id="08404-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="08404-126">Per altre informazioni, vedere [accedere agli spazi dei nomi WMI](access-to-wmi-namespaces.md) e [impostare i descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="08404-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Ottenere e impostare i metodi del descrittore di sicurezza per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="08404-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="08404-128">Sono stati aggiunti nuovi metodi di script per ottenere e impostare i descrittori di sicurezza per la [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)e [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="08404-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="08404-129">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="08404-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Modificare i descrittori di sicurezza negli script</span><span class="sxs-lookup"><span data-stu-id="08404-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="08404-131">La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) dispone di metodi che consentono agli script di convertire descrittori di sicurezza binari su oggetti a protezione diretta in oggetti [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o stringhe del [linguaggio di definizione del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="08404-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="08404-132">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="08404-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="08404-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="08404-134">Il controllo dell'account utente influiscono sui dati WMI restituiti, sull'accesso remoto e sul modo in cui è necessario eseguire gli script.</span><span class="sxs-lookup"><span data-stu-id="08404-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="08404-135">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="08404-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="08404-136">Per ulteriori informazioni su UAC, vedere [Introduzione con controllo dell'account utente in Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="08404-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="08404-137">Altre nuove funzionalità di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08404-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="08404-138">Nell'elenco seguente sono elencate le nuove funzionalità WMI disponibili in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08404-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="08404-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nuovi provider di dati del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="08404-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="08404-140">Il processo di individuazione automatica/AutoPurge (ADAP) non trasferisce più gli oggetti contatore delle prestazioni in classi di prestazioni WMI nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="08404-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="08404-141">Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="08404-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="08404-142">Il [provider WMIPerfClass](wmiperfclass-provider.md) crea le classi del contatore delle prestazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="08404-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="08404-143">I dati vengono forniti dinamicamente a queste classi di prestazioni WMI dal [provider WMIPerfInst](wmiperfinst-provider.md).</span><span class="sxs-lookup"><span data-stu-id="08404-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indicizzatore per le raccolte</span><span class="sxs-lookup"><span data-stu-id="08404-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="08404-145">Il metodo [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) restituisce l'oggetto associato a un indice specificato in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="08404-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="08404-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Supporto per IPv6 e IPv4</span><span class="sxs-lookup"><span data-stu-id="08404-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="08404-147">Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="08404-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="08404-148">A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="08404-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="08404-149">Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="08404-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Modifiche alle connessioni remote</span><span class="sxs-lookup"><span data-stu-id="08404-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="08404-151">La connessione a uno spazio dei nomi WMI in un computer remoto che esegue Windows Vista può richiedere modifiche alle impostazioni per [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), il [controllo dell'account utente](/previous-versions/aa905108(v=msdn.10))o DCOM.</span><span class="sxs-lookup"><span data-stu-id="08404-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="08404-152">Per ulteriori informazioni, vedere [connessione a WMI in modalità remota a partire da vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="08404-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Modifiche a [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="08404-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="08404-154">Per i sistemi in esecuzione nel sistema operativo Windows Vista e versioni successive, questa classe restituisce solo gli aggiornamenti forniti da Component Based Servicing (CBS).</span><span class="sxs-lookup"><span data-stu-id="08404-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="08404-155">Questi aggiornamenti non sono elencati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="08404-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="08404-156">Gli aggiornamenti forniti da Windows Installer (MSI) o [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) non vengono restituiti da [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span><span class="sxs-lookup"><span data-stu-id="08404-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="08404-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Abilitazione e disabilitazione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="08404-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="08404-158">[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) dispone di nuovi metodi per abilitare e disabilitare la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="08404-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="08404-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Modifiche del provider di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="08404-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="08404-160">[**Win32 \_ Il prodotto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) presenta nuovi metodi e proprietà per fornire più dati sul prodotto.</span><span class="sxs-lookup"><span data-stu-id="08404-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="08404-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nuove classi di monitoraggio visualizzazione</span><span class="sxs-lookup"><span data-stu-id="08404-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="08404-162">Le [classi di visualizzazione del monitoraggio](/windows/desktop/WmiCoreProv/wmi-core-provider-) contengono i dati forniti dal [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider) che fornisce dati sui monitoraggi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="08404-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="08404-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span><span class="sxs-lookup"><span data-stu-id="08404-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="08404-164">Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI fornisce dati dalle operazioni di Baseboard Management Controller (BMC) al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08404-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="08404-165">Il provider fornisce informazioni alle classi di informazioni di gestione della piattaforma intelligente, che forniscono i dati dei sensori e i dati del messaggio del registro eventi di sistema BMC (SEL).</span><span class="sxs-lookup"><span data-stu-id="08404-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="08404-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Rilevamento di Hyper-Threading e processori multicore</span><span class="sxs-lookup"><span data-stu-id="08404-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="08404-167">[**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) e [**il \_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor) dispongono di nuove proprietà che consentono di scrivere script per determinare se il sistema del computer dispone di processori multicore o Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="08404-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="08404-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Messaggi di evento</span><span class="sxs-lookup"><span data-stu-id="08404-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="08404-169">Windows Vista presenta nuovi messaggi di evento.</span><span class="sxs-lookup"><span data-stu-id="08404-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="08404-170">Per ulteriori informazioni, vedere [eventi WMI](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="08404-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="08404-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Miglioramenti dell'inventario</span><span class="sxs-lookup"><span data-stu-id="08404-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="08404-172">Molte classi hardware hanno apportato modifiche per migliorare l'inventario hardware.</span><span class="sxs-lookup"><span data-stu-id="08404-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="08404-173">Ad esempio, è stata aggiunta una proprietà del numero di serie a [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) e [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span><span class="sxs-lookup"><span data-stu-id="08404-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="08404-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nuovi modelli di hosting del provider</span><span class="sxs-lookup"><span data-stu-id="08404-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="08404-175">Sono stati aggiunti nuovi modelli di hosting dei provider per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08404-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="08404-176">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="08404-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="08404-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08404-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08404-178">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="08404-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
