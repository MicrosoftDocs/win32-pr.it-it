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
# <a name="whats-new-in-windowsvista"></a>Novità di Windows Vista

A partire da Windows Vista, WMI contiene numerose nuove funzionalità basate su richieste da parte degli utenti WMI.

-   [Nuovo strumento per la risoluzione dei problemi](#new-troubleshooting-tool)
-   [Nuove funzionalità di sicurezza in Windows Vista](#new-security-features-in-windows-vista)
-   [Altre nuove funzionalità di Windows Vista](#other-new-features-in-windows-vista)
-   [Argomenti correlati](#related-topics)

## <a name="new-troubleshooting-tool"></a>Nuovo strumento per la risoluzione dei problemi

Per il download è disponibile un nuovo strumento per la risoluzione dei problemi.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilità di diagnosi di WMI
</dt> <dd>

Questa utilità esamina lo stato corrente del servizio WMI e i componenti correlati, le impostazioni DCOM e le impostazioni del registro di sistema nel computer locale. L'utilità segnala problemi e offre suggerimenti per il ripristino. Per ulteriori informazioni e per scaricare l'utilità, vedere [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Nuove funzionalità di sicurezza in Windows Vista

Nell'elenco seguente sono elencate le nuove funzionalità di sicurezza WMI disponibili in Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Traccia e registrazione degli eventi
</dt> <dd>

Il servizio WMI non utilizza più la maggior parte dei [file di log WMI](wmi-log-files.md). USA invece [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed eventi sono disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil. Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Impostazione della sicurezza dello spazio dei nomi WMI nel file MOF
</dt> <dd>

Il qualificatore **NamespaceSecuritySDDL** può essere usato per proteggere qualsiasi spazio dei nomi. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Controllo di sicurezza degli spazi dei nomi WMI
</dt> <dd>

WMI utilizza gli elenchi di controllo di accesso di sistema (SACL) dello spazio dei nomi per controllare l'attività dello spazio dei nomi e segnalare gli eventi al registro eventi di protezione. Per altre informazioni, vedere [accedere agli spazi dei nomi WMI](access-to-wmi-namespaces.md) e [impostare i descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Ottenere e impostare i metodi del descrittore di sicurezza per gli oggetti a protezione diretta
</dt> <dd>

Sono stati aggiunti nuovi metodi di script per ottenere e impostare i descrittori di sicurezza per la [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)e [**\_ \_ SystemSecurity**](--systemsecurity.md). Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Modificare i descrittori di sicurezza negli script
</dt> <dd>

La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) dispone di metodi che consentono agli script di convertire descrittori di sicurezza binari su oggetti a protezione diretta in oggetti [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o stringhe del [linguaggio di definizione del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Controllo dell'account utente
</dt> <dd>

Il controllo dell'account utente influiscono sui dati WMI restituiti, sull'accesso remoto e sul modo in cui è necessario eseguire gli script. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md). Per ulteriori informazioni su UAC, vedere [Introduzione con controllo dell'account utente in Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Altre nuove funzionalità di Windows Vista

Nell'elenco seguente sono elencate le nuove funzionalità WMI disponibili in Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Nuovi provider di dati del contatore delle prestazioni
</dt> <dd>

Il processo di individuazione automatica/AutoPurge (ADAP) non trasferisce più gli oggetti contatore delle prestazioni in classi di prestazioni WMI nel repository WMI. Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md). Il [provider WMIPerfClass](wmiperfclass-provider.md) crea le classi del contatore delle prestazioni WMI. I dati vengono forniti dinamicamente a queste classi di prestazioni WMI dal [provider WMIPerfInst](wmiperfinst-provider.md).

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indicizzatore per le raccolte
</dt> <dd>

Il metodo [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) restituisce l'oggetto associato a un indice specificato in una raccolta.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Supporto per IPv6 e IPv4
</dt> <dd>

Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6. Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Modifiche alle connessioni remote
</dt> <dd>

La connessione a uno spazio dei nomi WMI in un computer remoto che esegue Windows Vista può richiedere modifiche alle impostazioni per [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), il [controllo dell'account utente](/previous-versions/aa905108(v=msdn.10))o DCOM. Per ulteriori informazioni, vedere [connessione a WMI in modalità remota a partire da vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Modifiche a [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Per i sistemi in esecuzione nel sistema operativo Windows Vista e versioni successive, questa classe restituisce solo gli aggiornamenti forniti da Component Based Servicing (CBS). Questi aggiornamenti non sono elencati nel registro di sistema. Gli aggiornamenti forniti da Windows Installer (MSI) o [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) non vengono restituiti da [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Abilitazione e disabilitazione di una scheda di interfaccia di rete
</dt> <dd>

[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) dispone di nuovi metodi per abilitare e disabilitare la scheda di rete.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Modifiche del provider di Windows Installer
</dt> <dd>

[**Win32 \_ Il prodotto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) presenta nuovi metodi e proprietà per fornire più dati sul prodotto.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Nuove classi di monitoraggio visualizzazione
</dt> <dd>

Le [classi di visualizzazione del monitoraggio](/windows/desktop/WmiCoreProv/wmi-core-provider-) contengono i dati forniti dal [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider) che fornisce dati sui monitoraggi di visualizzazione.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider
</dt> <dd>

Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI fornisce dati dalle operazioni di Baseboard Management Controller (BMC) al sistema operativo. Il provider fornisce informazioni alle classi di informazioni di gestione della piattaforma intelligente, che forniscono i dati dei sensori e i dati del messaggio del registro eventi di sistema BMC (SEL).

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Rilevamento di Hyper-Threading e processori multicore
</dt> <dd>

[**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) e [**il \_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor) dispongono di nuove proprietà che consentono di scrivere script per determinare se il sistema del computer dispone di processori multicore o Hyper-Threading.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Messaggi di evento
</dt> <dd>

Windows Vista presenta nuovi messaggi di evento. Per ulteriori informazioni, vedere [eventi WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Miglioramenti dell'inventario
</dt> <dd>

Molte classi hardware hanno apportato modifiche per migliorare l'inventario hardware. Ad esempio, è stata aggiunta una proprietà del numero di serie a [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) e [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Nuovi modelli di hosting del provider
</dt> <dd>

Sono stati aggiunti nuovi modelli di hosting dei provider per Windows Vista. Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
