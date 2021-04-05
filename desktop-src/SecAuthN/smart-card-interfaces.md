---
description: Un'interfaccia smart card è costituita da un set predefinito di servizi disponibili all'interno di una smart card, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfacce smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758390"
---
# <a name="smart-card-interfaces"></a>Interfacce smart card

Un'interfaccia [*Smart Card*](../secgloss/s-gly.md) è costituita da un set predefinito di servizi disponibili all'interno di una *Smart Card*, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.

Per quanto riguarda le smart card, il termine "Interface" è simile a quello usato in COM, che a sua volta è un concetto simile all'identificatore dell'applicazione ISO 7816/5 ma con un ambito diverso.

Ogni interfaccia smart card è identificata da un GUID. Ad esempio, è possibile definire un'interfaccia che fornisce informazioni Biorhythm al suo titolare. Se una determinata smart card supporta questo servizio, potrebbe richiedere di supportare il GUID dell'interfaccia. Usando i GUID di interfaccia, un'applicazione può cercare un particolare set di interfacce, individuando qualsiasi scheda che supporta tale set, per completare un'attività.

Sebbene un'interfaccia disponga di un solo GUID, può essere implementata in modo diverso in schede diverse. Ad esempio, l'interfaccia Biorhythm menzionata in precedenza può includere diverse implementazioni, ma viene fatto riferimento a tutti con lo stesso GUID. Le diverse implementazioni non modificano l'interazione tra l'applicazione e la smart card; Tuttavia, l'interazione tra il [*provider di servizi*](../secgloss/c-gly.md) e le smart card può variare in base all'implementazione dell'interfaccia.

Il set di interfacce supportato da una smart card viene definito durante l'introduzione della smart card (vedere [introduzione di smart card al sistema](introducing-smart-cards-to-the-system.md)).

 

 
