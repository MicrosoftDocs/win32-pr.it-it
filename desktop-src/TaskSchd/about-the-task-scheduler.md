---
title: Informazioni sul Utilità di pianificazione
description: Il servizio Utilità di pianificazione consente di eseguire attività automatiche in un computer scelto.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Utilità di pianificazione Utilità di pianificazione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298480"
---
# <a name="about-the-task-scheduler"></a>Informazioni sul Utilità di pianificazione

Il servizio Utilità di pianificazione consente di eseguire attività automatiche in un computer scelto. Con questo servizio, è possibile pianificare l'esecuzione di qualsiasi programma in un momento appropriato o quando si verifica un evento specifico. Il Utilità di pianificazione monitora il tempo o i criteri di evento scelti, quindi esegue l'attività quando tali criteri vengono soddisfatti.

## <a name="where-task-scheduler-is-installed"></a>Dove è installato Utilità di pianificazione

Il Utilità di pianificazione viene installato automaticamente con diversi sistemi operativi Microsoft.

Utilità di pianificazione 1,0 viene installato con i sistemi operativi Windows Server 2003, Windows XP e Windows 2000.

Utilità di pianificazione 2,0 viene installato con Windows Vista e Windows Server 2008.

Per lo sviluppo di applicazioni che utilizzano il servizio Utilità di pianificazione in Windows Vista, è necessario utilizzare l'API Utilità di pianificazione 2,0. Per ulteriori informazioni, vedere [utilità di pianificazione Reference](task-scheduler-reference.md).

Utilità di pianificazione viene avviato ogni volta che viene avviato il sistema operativo. Può essere eseguito tramite l'interfaccia utente grafica (GUI) Utilità di pianificazione o tramite l'API Utilità di pianificazione descritta in questo SDK.

## <a name="information-about-tasks"></a>Informazioni sulle attività

Le attività sono il componente principale del Utilità di pianificazione. Per informazioni sulle attività e sui relativi componenti, vedere gli argomenti seguenti:

-   [Attività](tasks.md)
-   [Azioni attività](task-actions.md)
-   [Trigger attività](task-triggers.md)
-   [Informazioni di registrazione delle attività](task-registration-information.md)
-   [Condizioni di inattività](task-idle-conditions.md)
-   [Contesti di sicurezza per le attività](security-contexts-for-running-tasks.md)
-   [Ripetizione di un'attività](repeating-a-task.md)
-   [Manutenzione automatica](task-maintenence.md)

Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 




