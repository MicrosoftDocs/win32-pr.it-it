---
description: L'interfaccia IInstallationBehavior definisce le proprietà seguenti.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Proprietà di IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966737"
---
# <a name="iinstallationbehavior-properties"></a>Proprietà di IInstallationBehavior

L'interfaccia [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) definisce le proprietà seguenti.



| Proprietà                                                                                 | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Ottiene un valore booleano thast indica se l'installazione o la disinstallazione di un aggiornamento può richiedere l'input dell'utente.                                                        |
| [**Impatto**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Ottiene un'enumerazione [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) che indica il modo in cui l'installazione o la disinstallazione dell'aggiornamento influiscono sul computer.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Ottiene un'enumerazione [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) che specifica il comportamento di riavvio che si verifica durante l'installazione o la disinstallazione dell'aggiornamento. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Ottiene un valore booleano che indica se l'installazione o la disinstallazione di un aggiornamento richiede la connettività di rete.                                                     |



 

 

 



