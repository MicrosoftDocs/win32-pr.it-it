---
description: Le tabelle seguenti sono obbligatorie in un modulo unione standard.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Unire tabelle di database del modulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201b4af776ae0b68fd4330dca8240390e5731950fdaba5a734f48d887db5be84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580641"
---
# <a name="merge-module-database-tables"></a>Unire tabelle di database del modulo

Le tabelle seguenti sono obbligatorie in un modulo unione standard.



| Nome tabella                                       | Commento                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Componente](component-table.md)                 | (OBBLIGATORIO)                                                                                       |
| [Directory](directory-table.md)                 | (OBBLIGATORIO)                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | (OBBLIGATORIO)                                                                                       |
| [File](file-table.md)                           | (OBBLIGATORIO)                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | (OBBLIGATORIO) Unito nel database del programma di installazione. Elenca le informazioni che identificano un modulo unione. |
| [ModuleComponents](modulecomponents-table.md)   | (OBBLIGATORIO) Unito nel database del programma di installazione. Elenca tutti i componenti del modulo unione.     |



 

Le tabelle seguenti si verificano solo nei moduli unione o in altri database del programma di installazione già combinati con un modulo di merge.



| Nome tabella                                     | Commento                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | Unito nel database del programma di installazione. Elenca gli altri moduli unione richiesti da questo modulo unione.                |
| [ModuleExclusion](moduleexclusion-table.md)   | Unito nel database del programma di installazione. Elenca altri moduli unione incompatibili con questo modulo unione. |



 

Le tabelle ModuleSequence seguenti si verificano solo nei moduli unione.



| Nome tabella                                                             | Commento                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | Unisce le azioni nella [tabella AdminUISequence](adminuisequence-table.md).               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | Unisce le azioni nella [tabella AdminExecuteSequence](adminexecutesequence-table.md).     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | Non usare questa tabella. Per informazioni dettagliate, [vedere Tabella AdvtUISequence.](advtuisequence-table.md) |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | Unisce le azioni nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | Elenca le tabelle del modulo che non vengono unite nel file .msi.                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | Unisce le azioni nella [tabella InstallUISequence](installuisequence-table.md).           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | Unisce le azioni nella [tabella InstallExecuteSequence](installexecutesequence-table.md). |



 

Le tabelle seguenti sono necessarie in ogni modulo unione configurabile. Mergemod.dll 2.0 o versione successiva è necessario per creare un modulo unione configurabile. Per informazioni dettagliate, vedere [Configurable Merge Modules](configurable-merge-modules.md).



| Nome tabella                                                 | Commento                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tabella ModuleSubstitution](modulesubstitution-table.md)   | (OBBLIGATORIO) Questa tabella non viene unita nel database di installazione di destinazione. Specifica i campi configurabili nel database di destinazione e fornisce un modello per la configurazione di ogni campo. |
| [Tabella ModuleConfiguration](moduleconfiguration-table.md) | (OBBLIGATORIO) Questa tabella non viene unita nel database di installazione di destinazione. Identifica gli attributi configurabili del modulo.                                                                 |



 

Le tabelle del programma di installazione seguenti non possono essere presenti in un modulo unione standard.

-   [BBControl](bbcontrol-table.md)
-   [Billboard](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [Error (Errore) (Error (Errore)e)](error-table.md)
-   [Funzionalità](feature-table.md)
-   [Tabella LaunchCondition](launchcondition-table.md)
-   [Supporti](media-table.md)
-   [Patch](patch-table.md)
-   [Aggiornamento](upgrade-table.md)

Le tabelle del programma di installazione seguenti sono facoltative nei moduli unione.

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [Appid](appid-table.md)
-   [Appsearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Classe](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [Controllo](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Finestra di dialogo](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [DuplicateFile](duplicatefile-table.md)
-   [Environment](environment-table.md)
-   [EventMapping](eventmapping-table.md)
-   [Estensione](extension-table.md)
-   [Font](font-table.md)
-   [Icona](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [MIME](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCAttribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [Tabella ProgID](progid-table.md)
-   [Proprietà](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Tabella del Registro di sistema](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [ServiceInstall](serviceinstall-table.md)
-   [Scelte rapide](shortcut-table.md)
-   [Firma](signature-table.md)
-   [TextStyle](textstyle-table.md)
-   [Typelib](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verbo](verb-table.md)

 

 



