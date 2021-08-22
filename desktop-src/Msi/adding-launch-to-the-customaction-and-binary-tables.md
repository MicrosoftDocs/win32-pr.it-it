---
description: Aggiungere un record alla tabella CustomAction per l'azione personalizzata Avvia.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Aggiunta di Launch alle tabelle CustomAction e Binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145964"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Aggiunta di Launch alle tabelle CustomAction e Binary

Aggiungere un record alla tabella [CustomAction per](customaction-table.md) l'azione personalizzata Avvia. Immettere il nome dell'azione personalizzata nella colonna Azione della tabella CustomAction. Immettere il tipo numerico totale per Launch, 65, nella colonna Type (Tipo) della tabella Custom action (Azione personalizzata). La colonna Source della tabella CustomAction specifica una chiave nel record della [tabella binaria](binary-table.md) che contiene i dati binari per la DLL. Immettere Tutorial.dll nella colonna Origine della tabella CustomAction. Il punto di ingresso specificato nel campo Target della tabella CustomAction deve corrispondere a quello esportato dalla DLL. Immettere LaunchTutorial nella colonna Target della tabella CustomAction.

[Tabella CustomAction](customaction-table.md)



| Azione | Tipo | Source (Sorgente)       | Destinazione         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | LaunchTutorial |



 

Aggiungere il Tutorial.dll creato da Tutorial.cpp come flusso binario alla tabella Binary.

[Tabella binaria](binary-table.md)



| Nome         | Dati                          |
|--------------|-------------------------------|
| Tutorial.dll | {*Dati binari aggiunti per la DLL*} |



 

Continuare ad [aggiungere un evento di controllo al termine dell'installazione per eseguire Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



