---
description: Sequenze di azioni suggerite per una tabella InstalUISequence di base in un database Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence suggerito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313329"
---
# <a name="suggested-installuisequence"></a>InstallUISequence suggerito



| Azione                                          | Condizione                                                                                                  | Sequenza |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| FatalErrorDlg                                   |                                                                                                            | -3       |
| UserExitDlg                                     |                                                                                                            | -2       |
| ExitDlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| PrepareDlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [CCPSearch](ccpsearch-action.md)               | NON [ **installato**](installed.md)                                                                         | 500      |
| [RMCCPSearch](rmccpsearch-action.md)           | NON [ **installato**](installed.md)                                                                         | 600      |
| [CostInitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [Filecost](filecost-action.md)                 |                                                                                                            | 900      |
| [CostFinalize secondo](costfinalize-action.md)         |                                                                                                            | 1000     |
| WelcomeDlg                                      | NON [ **installato**](installed.md)                                                                         | 1230     |
| ResumeDlg                                       | [**Installazione**](installed.md) completata E ( [**ripresa**](resume.md) o [**preselezione**](preselected.md))       | 1240     |
| MaintenanceWelcomeDlg                           | [**Installazione**](installed.md) completata E non [**Riprendi**](resume.md) e non [**preselezionato**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



