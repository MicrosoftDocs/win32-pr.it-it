---
description: Novità di Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Novità di Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000a3460366855df65096333a8b847a6d2c0c0a48a89c91f6791db3286d634fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502861"
---
# <a name="whats-new-in-windows-7"></a>Novità di Windows 7

## <a name="new-security-feature-in-windows-7"></a>Nuova funzionalità di sicurezza in Windows 7

Di seguito è riportata la nuova Windows di sicurezza di Strumentazione gestione Windows (WMI) disponibile in Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Controllo della sicurezza del provider
</dt> <dd>

Modifiche per migliorare la sicurezza del processo host del provider condiviso WMI (wmiprvse.exe). Queste modifiche introducono tre nuovi criteri di gruppo e due modalità di esecuzione per l'host condiviso WMI, denominate modalità protette e compatibili. Per altre informazioni, vedere Chiavi del [Registro di sistema per il controllo della sicurezza del provider.](registry-keys-for-controlling-provider-security-.md)

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Altre funzionalità nuove o aggiornate in Windows 7

Nell'elenco seguente sono elencate le nuove funzionalità WMI disponibili in Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilità dello schema CIM
</dt> <dd>

A partire Windows 7, WMI è compatibile con lo schema Common Information Model (CIM) versione 2.17.1. Per altre informazioni, vedere [Compatibilità dello schema CIM.](cim-schema-compatibility.md)

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Attraversamento dell'associazione tra spazi dei nomi
</dt> <dd>

WMI ha implementato un meccanismo standard per l'individuazione dei profili tramite lo schema CIM. Per altre informazioni, vedere [Cross Namespace Association Traversal](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Provider di associazioni
</dt> <dd>

Informazioni sulla scrittura e la registrazione di un provider di associazioni. I provider di associazioni vengono usati per esporre profili standard, ad esempio un profilo di risparmio energia. Per altre informazioni, vedere [Scrittura di un provider di associazioni per l'interoperabilità.](writing-an-association-provider-for-interop.md)

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Stato delle funzionalità facoltativo
</dt> <dd>

WMI ha implementato [**la classe \_ OptionalFeature Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Questa classe esegue una query e restituisce lo stato delle funzionalità facoltative presenti in un computer. Per query di esempio che usano Windows PowerShell, vedere [Esecuzione di query sullo stato delle funzionalità facoltative.](querying-the-status-of-optional-features.md)

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Modifica del comportamento predefinito per la funzionalità del repository AutoRestore
</dt> <dd>

WMI include una nuova chiave del Registro di sistema per abilitare o disabilitare la funzionalità del repository AutoRestore. Per altre informazioni, vedere [Chiave del Registro di sistema per la configurazione del repository.](registry-key-for-repository-configuration.md)

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Nuove Windows PowerShell di comando
</dt> <dd>

Windows PowerShell cmdlet consentono agli utenti di completare le attività end-to-end necessarie per gestire computer locali e remoti. Per altre informazioni, vedere [Managed Reference for WMI PowerShell Command Classes](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Nuovo meccanismo per la connessione ai computer remoti
</dt> <dd>

Windows PowerShell fornisce un meccanismo semplice per connettersi a WMI in un computer remoto. Per altre informazioni, vedere [Connessione a WMI in un computer remoto tramite PowerShell.](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Modifiche alle classi di licenze software
</dt> <dd>

Le [classi di licenze software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) hanno nuovi metodi e proprietà per fornire più dati sulle licenze software. È stata aggiunta anche la classe [**SoftwareLicensingTokenActivationLicense.**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense)

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Nuove classi di misurazione dell'alimentazione e budget
</dt> <dd>

[Le classi di misurazione dell'alimentazione](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) e di budget sono l'interfaccia principale per la query delle informazioni DELL'interfaccia del contatore di alimentazione dai contatori di alimentazione sottostanti nel sistema.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Nuove classi di criteri di risparmio energia
</dt> <dd>

[Le classi di criteri di](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) risparmio energia consentono la gestione remota di tutte le infrastrutture di criteri di risparmio energia.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Modifiche alla [**classe \_ ServerFeature Win32**](win32-serverfeature.md)
</dt> <dd>

La **proprietà ID** di [**Win32 \_ ServerFeature è**](win32-serverfeature.md) stata aggiornata.

</dd> </dl>

Per altre informazioni sulle nuove funzionalità delle versioni precedenti del sistema operativo, vedere Novità [di Windows Vista.](what-s-new-in-windows-vista.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
