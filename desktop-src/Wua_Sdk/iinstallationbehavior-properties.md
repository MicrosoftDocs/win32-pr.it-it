---
description: L'interfaccia IInstallationBehavior definisce le proprietà seguenti.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Proprietà di IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a4bcb1f444d628ebff221d19143d0dd5f472149da24f86b46811bb9efc2c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994771"
---
# <a name="iinstallationbehavior-properties"></a>Proprietà di IInstallationBehavior

[**L'interfaccia IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) definisce le proprietà seguenti.



| Proprietà                                                                                 | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Ottiene un valore booleano che indica se l'installazione o la disinstallazione di un aggiornamento può richiedere l'input dell'utente.                                                        |
| [**Impatto**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Ottiene [**un'enumerazione InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) che indica in che modo l'installazione o la disinstallazione dell'aggiornamento influisce sul computer.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Ottiene [**un'enumerazione InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) che specifica il comportamento di riavvio che si verifica quando si installa o si disinstalla l'aggiornamento. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Ottiene un valore booleano che indica se l'installazione o la disinstallazione di un aggiornamento richiede la connettività di rete.                                                     |



 

 

 



