---
description: Novità di Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Novità di Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318843"
---
# <a name="whats-new-in-windows-7"></a>Novità di Windows 7

## <a name="new-security-feature-in-windows-7"></a>Nuova funzionalità di sicurezza di Windows 7

Di seguito sono elencate le nuove funzionalità di sicurezza di Strumentazione gestione Windows (WMI) disponibili in Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Controllo della sicurezza del provider
</dt> <dd>

Modifiche per migliorare la sicurezza del processo host del provider condiviso WMI (wmiprvse.exe). Queste modifiche introducono tre nuovi criteri di gruppo e due modalità di esecuzione per l'host condiviso WMI, chiamati modalità sicure e compatibili. Per ulteriori informazioni, vedere [chiavi del registro di sistema per controllare la sicurezza del provider](registry-keys-for-controlling-provider-security-.md).

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Altre funzionalità nuove o aggiornate in Windows 7

Nell'elenco seguente sono elencate le nuove funzionalità WMI disponibili in Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilità con lo schema CIM
</dt> <dd>

A partire da Windows 7, WMI è compatibile con la versione dello schema Common Information Model (CIM) 2.17.1. Per ulteriori informazioni, vedere [CIM schema Compatibility](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Attraversamento dell'associazione tra spazi dei nomi
</dt> <dd>

In WMI è stato implementato un meccanismo standard per individuare i profili mediante lo schema CIM. Per altre informazioni, vedere attraversamento di [associazioni tra spazi dei nomi](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Provider di associazioni
</dt> <dd>

Informazioni sulla scrittura e la registrazione di un provider di associazioni. I provider di associazioni vengono usati per esporre i profili standard, ad esempio un profilo di alimentazione. Per ulteriori informazioni, vedere [scrittura di un provider di associazioni per l'interoperabilità](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Stato funzionalità facoltativo
</dt> <dd>

WMI ha implementato la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Questa classe esegue una query e restituisce lo stato delle funzionalità facoltative presenti in un computer. Per le query di esempio che usano Windows PowerShell, vedere [esecuzione di query sullo stato delle funzionalità facoltative](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Modifica del comportamento predefinito per la funzionalità del repository autorestore
</dt> <dd>

WMI include una nuova chiave del registro di sistema per abilitare o disabilitare la funzionalità di repository autorestore. Per altre informazioni, vedere [chiave del registro di sistema per la configurazione del repository](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Nuove classi di comando di Windows PowerShell
</dt> <dd>

I cmdlet di Windows PowerShell consentono agli utenti di completare le attività end-to-end necessarie per gestire i computer locali e remoti. Per ulteriori informazioni, vedere [Managed Reference for WMI PowerShell command Classes](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Nuovo meccanismo per la connessione a computer remoti
</dt> <dd>

Windows PowerShell fornisce un meccanismo semplice per connettersi a WMI in un computer remoto. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto tramite PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Modifiche alle classi di gestione licenze software
</dt> <dd>

Le [classi di gestione licenze software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) hanno nuovi metodi e proprietà per fornire più dati sulle licenze software. È stata inoltre aggiunta la classe [**SoftwareLicensingTokenActivationLicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) .

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Nuove classi di misurazione del risparmio di energia e budget
</dt> <dd>

Le [classi di misurazione del risparmio di energia e di budget](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) sono l'interfaccia principale per la query delle informazioni dell'interfaccia del misuratore di energia (PMI) dai contatori di energia sottostante nel sistema.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Nuove classi di criteri di risparmio energia
</dt> <dd>

Le [classi di criteri di risparmio energia](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) consentono la gestione remota di tutte le infrastrutture per i criteri di risparmio energia.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Modifiche alla classe [**Win32 \_ ServerFeature**](win32-serverfeature.md)
</dt> <dd>

La proprietà **ID** di [**Win32 \_ ServerFeature**](win32-serverfeature.md) è stata aggiornata.

</dd> </dl>

Per ulteriori informazioni sulle nuove funzionalità nelle versioni precedenti del sistema operativo, vedere Novità [di Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
