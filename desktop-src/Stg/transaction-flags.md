---
title: Flag di transazione
description: Un oggetto può essere aperto in modalità diretta o transazione.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a3f389def4bdbb9d0cabf92500b316ae354878ec5f790b44e9f01121aeb57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886783"
---
# <a name="transaction-flags"></a>Flag di transazione

Un oggetto può essere aperto in modalità diretta o transazione. Quando un oggetto viene aperto in modalità diretta, le modifiche vengono apportate immediatamente e definitivamente. Quando un oggetto viene aperto in modalità transazione, le modifiche vengono memorizzate nel buffer in modo da poter essere esplicitamente salvate o ripristinate al termine della modifica. Le modifiche di cui è stato eseguito il commit vengono salvate nell'oggetto mentre le modifiche ripristinate vengono rimosse. La modalità diretta è la modalità di accesso predefinita.

La modalità transazionale non è necessaria in un oggetto di archiviazione padre per poterla usare in un elemento annidato. Una transazione per un elemento annidato, tuttavia, è annidata all'interno della transazione per l'oggetto di archiviazione padre. Pertanto, non è possibile eseguire il commit delle modifiche apportate a un oggetto figlio fino a quando non viene eseguito il commit di quelle apportate all'oggetto padre ed entrambe rimangono di cui non è stato eseguito il commit fino a quando l'oggetto di archiviazione radice (padre di primo livello) non viene effettivamente scritto su disco. In altre parole, le modifiche si spostano verso l'esterno: gli oggetti interni pubblicano le modifiche alle transazioni dei contenitori immediati.

 

 




