---
description: Un smart card interface è costituito da un set predefinito di servizi disponibili all'interno di un smart card, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfacce smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db3fb5369f36f76e8bf5909afad94959ff70541d9026762234d65ae181b0172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917770"
---
# <a name="smart-card-interfaces"></a>Interfacce smart card

[*Un smart card*](../secgloss/s-gly.md) interface è costituito da un set predefinito di servizi disponibili all'interno di un *smart card*, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.

Per quanto riguarda le smart card, il termine "interfaccia" è simile a come viene usato in COM, che a sua volta è simile nel concetto all'identificatore dell'applicazione ISO 7816/5, ma con un ambito diverso.

Ogni smart card interfaccia è identificata da un GUID. Ad esempio, potrebbe essere definita un'interfaccia che fornisce informazioni bioritmo al relativo titolare. Se un determinato smart card supporta questo servizio, può attestare di supportare tale GUID dell'interfaccia. Usando i GUID dell'interfaccia, un'applicazione può cercare un particolare set di interfacce, individuando qualsiasi scheda che supporta tale set, per completare un'attività.

Anche se un'interfaccia ha un GUID, potrebbe essere implementata in modo diverso in schede diverse. Ad esempio, l'interfaccia biorhythm citata in precedenza può avere diverse implementazioni, ma tutti fanno riferimento usando lo stesso GUID. Le diverse implementazioni non modificano l'interazione tra l'applicazione e l'smart card; Tuttavia, l'interazione tra [*il provider di servizi*](../secgloss/c-gly.md) e le smart card può variare a seconda dell'implementazione dell'interfaccia.

Il set di interfacce supportate da un smart card viene definito durante l smart card in introduzione (vedere Introduzione alle [smart card nel sistema](introducing-smart-cards-to-the-system.md)).

 

 
