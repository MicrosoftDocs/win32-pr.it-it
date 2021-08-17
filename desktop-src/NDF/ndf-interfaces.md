---
title: Interfacce NDF
description: Le interfacce seguenti possono essere usate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16ff5dde9246798392903f47370e663e26dd6be7f21252f8791bfee267018b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801951"
---
# <a name="ndf-interfaces"></a>Interfacce NDF

Le interfacce seguenti possono essere usate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili. Anche se questa funzionalità non è necessaria per la maggior parte delle applicazioni, in alcuni casi può fornire diagnosi e risoluzioni più specifiche.

> [!Note]  
> Queste interfacce e i relativi metodi associati sono per gli sviluppatori che implementano le proprie classi helper di terze parti che estendono la funzionalità NDF.

 



| Interface Name (Nome interfaccia)                                                 | Descrizione                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Chiamato dalla funzione definita dall'utente per la maggior parte delle attività che si verificano durante una diagnosi.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Chiamato dalla funzione NDF per acquisire e fornire informazioni associate alle diagnosi e alla risoluzione dei problemi relativi alla rete. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Chiamato dalla funzione NDF per verificare che abbia le informazioni necessarie                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Riservato per l'utilizzo nel sistema.                                                                                                 |



 

 

 




