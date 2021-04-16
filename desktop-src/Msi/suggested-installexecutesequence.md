---
description: Sequenze di azioni suggerite per una tabella InstallExecuteSequence di base in un database Windows Installer.
ms.assetid: 7f337f37-1528-4b7e-a628-f9d235510a6f
title: InstallExecuteSequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c25f2db56ef3ad7296bddf4088ad32191f57df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530373"
---
# <a name="suggested-installexecutesequence"></a>InstallExecuteSequence suggerito



| Azione                                                          | Condizione                          | Sequenza |
|-----------------------------------------------------------------|------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md)                 |                                    | 100      |
| [AppSearch](appsearch-action.md)                               |                                    | 400      |
| [CCPSearch](ccpsearch-action.md)                               | NON [ **installato**](installed.md) | 500      |
| [RMCCPSearch](rmccpsearch-action.md)                           | NON [ **installato**](installed.md) | 600      |
| [ValidateProductID](validateproductid-action.md)               |                                    | 700      |
| [CostInitialize](costinitialize-action.md)                     |                                    | 800      |
| [Filecost](filecost-action.md)                                 |                                    | 900      |
| [CostFinalize secondo](costfinalize-action.md)                         |                                    | 1000     |
| [SetODBCFolders](setodbcfolders-action.md)                     |                                    | 1100     |
| [InstallValidate](installvalidate-action.md)                   |                                    | 1400     |
| [InstallInitialize](installinitialize-action.md)               |                                    | 1500     |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | NON [ **installato**](installed.md) | 1550     |
| [ProcessComponents](processcomponents-action.md)               |                                    | 1600     |
| [UnpublishComponents](unpublishcomponents-action.md)           |                                    | 1700     |
| [UnpublishFeatures](unpublishfeatures-action.md)               |                                    | 1800     |
| [StopServices](stopservices-action.md)                         | [**VersionNT**](versionnt.md)     | 1900     |
| [DeleteServices](deleteservices-action.md)                     | [**VersionNT**](versionnt.md)     | 2000     |
| [UnregisterComPlus](unregistercomplus-action.md)               |                                    | 2100     |
| [SelfUnregModules](selfunregmodules-action.md)                 |                                    | 2200     |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   |                                    | 2300     |
| [RemoveODBC](removeodbc-action.md)                             |                                    | 2400     |
| [UnregisterFonts](unregisterfonts-action.md)                   |                                    | 2500     |
| [RemoveRegistryValues](removeregistryvalues-action.md)         |                                    | 2600     |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           |                                    | 2700     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   |                                    | 2800     |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         |                                    | 2900     |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             |                                    | 3000     |
| [RemoveIniValues](removeinivalues-action.md)                   |                                    | 3100     |
| [RemoveShortcuts](removeshortcuts-action.md)                   |                                    | 3200     |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) |                                    | 3300     |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         |                                    | 3400     |
| [RemoveFiles](removefiles-action.md)                           |                                    | 3500     |
| [RemoveFolders](removefolders-action.md)                       |                                    | 3600     |
| [CreateFolders](createfolders-action.md)                       |                                    | 3700     |
| [MoveFiles](movefiles-action.md)                               |                                    | 3800     |
| [InstallFiles](installfiles-action.md)                         |                                    | 4000     |
| [PatchFiles](patchfiles-action.md)                             |                                    | 4090     |
| [DuplicateFiles](duplicatefiles-action.md)                     |                                    | 4210     |
| [Azione BindImage sul](bindimage-action.md)                               |                                    | 4300     |
| [CreateShortcuts](createshortcuts-action.md)                   |                                    | 4500     |
| [RegisterClassInfo](registerclassinfo-action.md)               |                                    | 4600     |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       |                                    | 4700     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             |                                    | 4800     |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 |                                    | 4900     |
| [WriteRegistryValori consente](writeregistryvalues-action.md)           |                                    | 5000     |
| [WriteIniValues](writeinivalues-action.md)                     |                                    | 5100     |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   |                                    | 5200     |
| [RegisterFonts](registerfonts-action.md)                       |                                    | 5300     |
| [InstallODBC](installodbc-action.md)                           |                                    | 5400     |
| [RegisterTypeLibraries](registertypelibraries-action.md)       |                                    | 5500     |
| [SelfRegModules](selfregmodules-action.md)                     |                                    | 5600     |
| [RegisterComPlus](registercomplus-action.md)                   |                                    | 5700     |
| [InstallServices](installservices-action.md)                   | [**VersionNT**](versionnt.md)     | 5800     |
| [StartServices](startservices-action.md)                       | [**VersionNT**](versionnt.md)     | 5900     |
| [RegisterUser](registeruser-action.md)                         |                                    | 6000     |
| [RegisterProduct](registerproduct-action.md)                   |                                    | 6100     |
| [PublishComponents](publishcomponents-action.md)               |                                    | 6200     |
| [PublishFeatures](publishfeatures-action.md)                   |                                    | 6300     |
| [PublishProduct](publishproduct-action.md)                     |                                    | 6400     |
| [InstallFinalize](installfinalize-action.md)                   |                                    | 6600     |



 

 

 



