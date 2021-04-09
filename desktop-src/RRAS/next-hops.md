---
title: Hop successivi
description: Alle route sono associati uno o più hop successivi.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044193"
---
# <a name="next-hops"></a>Hop successivi

Alle route sono associati uno o più hop successivi. Se la destinazione non si trova in una rete connessa direttamente, l'hop successivo è l'indirizzo del router (o rete) successivo nella rete in uscita che può indirizzare i dati alla destinazione in modo ottimale. Il percorso migliore è la route con il costo inferiore, in base ai criteri di routing in uso. Ogni hop successivo può essere utilizzato per l'invio dei dati nel percorso alla destinazione. Tutte le route di proprietà di un client condividono un insieme comune di voci di hop successivo aggiunte dal client.

Ogni hop successivo viene identificato in modo univoco dall'indirizzo dell'hop successivo e dall'indice dell'interfaccia utilizzato per raggiungere l'hop successivo.

Se l'hop successivo non è direttamente connesso, viene contrassegnato come hop successivo "remoto". In questo caso, il server d'esecuzione deve eseguire un'altra ricerca usando l'indirizzo di rete dell'hop successivo. Questa ricerca è necessaria per trovare l'hop successivo "locale" usato per raggiungere l'hop successivo remoto e la destinazione.

Una voce di hop successivo nella tabella di routing include:

-   Indirizzo di rete dell'hop successivo
-   Proprietario dell'hop successivo
-   Identificatore dell'interfaccia in uscita.
-   Stato dell'hop successivo
-   Flag associati all'hop successivo
-   Informazioni private del proprietario dell'hop successivo
-   Handle per la destinazione corrispondente all'hop successivo remoto

 

 




