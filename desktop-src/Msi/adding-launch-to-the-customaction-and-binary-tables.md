---
description: Aggiungere un record alla tabella CustomAction per l'azione di avvio personalizzata.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Aggiunta dell'avvio alle tabelle CustomAction e binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131506"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Aggiunta dell'avvio alle tabelle CustomAction e binarie

Aggiungere un record alla [tabella CustomAction](customaction-table.md) per l'azione di avvio personalizzata. Immettere il nome dell'azione personalizzata nella colonna azione della tabella CustomAction. Immettere il tipo numerico totale per Launch, 65, nella colonna Type della tabella delle azioni personalizzate. La colonna di origine della tabella CustomAction specifica una chiave nel record della [tabella binaria](binary-table.md) che contiene i dati binari per la dll. Immettere Tutorial.dll nella colonna origine della tabella CustomAction. Il punto di ingresso specificato nel campo di destinazione della tabella CustomAction deve corrispondere a quello esportato dalla DLL. Immettere LaunchTutorial nella colonna destinazione della tabella CustomAction.

[Tabella CustomAction](customaction-table.md)



| Azione | Tipo | Source (Sorgente)       | Destinazione         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | LaunchTutorial |



 

Aggiungere la Tutorial.dll creata da tutorial. cpp come flusso binario alla tabella binaria.

[Tabella binaria](binary-table.md)



| Nome         | Data                          |
|--------------|-------------------------------|
| Tutorial.dll | {*dati binari aggiunti per la dll*} |



 

Continuare ad [aggiungere un evento di controllo alla fine dell'installazione per eseguire l'avvio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



