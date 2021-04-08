---
title: Interfacce NDF
description: Le interfacce seguenti possono essere utilizzate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043987"
---
# <a name="ndf-interfaces"></a>Interfacce NDF

Le interfacce seguenti possono essere utilizzate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili. Anche se questa funzionalità non è necessaria per la maggior parte delle applicazioni, può fornire diagnosi e soluzioni più specifiche in alcuni casi.

> [!Note]  
> Queste interfacce e i relativi metodi associati sono destinate agli sviluppatori che implementano le proprie classi helper di terze parti che estendono la funzionalità NDF.

 



| Interface Name (Nome interfaccia)                                                 | Descrizione                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Chiamato da NDF per la maggior parte delle attività che si verificano durante una diagnosi.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Chiamato da NDF per acquisire e fornire informazioni associate a diagnosi e risoluzione dei problemi relativi alla rete. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Chiamato da NDF per verificare che disponga di informazioni obbligatorie                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Riservato per l'utilizzo nel sistema.                                                                                                 |



 

 

 




