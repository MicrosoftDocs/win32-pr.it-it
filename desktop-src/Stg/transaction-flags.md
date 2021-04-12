---
title: Flag di transazione
description: Un oggetto può essere aperto in modalità diretta o transazionale.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221599"
---
# <a name="transaction-flags"></a>Flag di transazione

Un oggetto può essere aperto in modalità diretta o transazionale. Quando un oggetto viene aperto in modalità diretta, le modifiche vengono apportate immediatamente e in modo permanente. Quando un oggetto viene aperto in modalità transazionale, le modifiche vengono memorizzate nel buffer, in modo che sia possibile eseguirne il commit o il ripristino in modo esplicito al termine della modifica. Le modifiche di cui è stato eseguito il commit vengono salvate nell'oggetto mentre le modifiche ripristinate vengono eliminate. La modalità diretta è la modalità di accesso predefinita.

La modalità transazionale non è necessaria in un oggetto di archiviazione padre per poterla utilizzare in un elemento annidato. Una transazione per un elemento annidato, tuttavia, è annidata all'interno della transazione per il relativo oggetto di archiviazione padre. Di conseguenza, non è possibile eseguire il commit delle modifiche apportate a un oggetto figlio fino a quando non viene eseguito il commit delle modifiche apportate all'elemento padre e non viene eseguito il commit di entrambe le modifiche fino a quando l'oggetto di archiviazione radice (l'elemento padre di livello superiore) In altre parole, le modifiche si spostano verso l'esterno: gli oggetti interni pubblicano le modifiche apportate alle transazioni dei contenitori immediati.

 

 




