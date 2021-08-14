---
title: Hop successivi
description: Alle route sono associati uno o più hop successivi.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a8d73a0d553773537ca2efd67457498ff9710cf9e7834d6952fcf2a81c5c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790101"
---
# <a name="next-hops"></a>Hop successivi

Alle route sono associati uno o più hop successivi. Se la destinazione non si trova in una rete connessa direttamente, l'hop successivo è l'indirizzo del router (o rete) successivo nella rete in uscita in grado di indirizzare al meglio i dati alla destinazione. La route migliore è quella con il costo minimo, in base ai criteri di routing in uso. Ogni hop successivo può essere usato per inoltrare i dati nel percorso alla destinazione. Tutte le route di proprietà di un client condividono un set comune di voci di hop successivo aggiunte dal client.

Ogni hop successivo è identificato in modo univoco dall'indirizzo dell'hop successivo e dall'indice di interfaccia usato per raggiungere l'hop successivo.

Se l'hop successivo non è connesso direttamente, viene contrassegnato come hop successivo "remoto". In questo caso, il server d'inoltro deve eseguire un'altra ricerca usando l'indirizzo di rete dell'hop successivo. Questa ricerca è necessaria per trovare l'hop successivo "locale" usato per raggiungere l'hop successivo remoto e la destinazione.

Una voce dell'hop successivo nella tabella di routing include:

-   Indirizzo di rete dell'hop successivo
-   Proprietario dell'hop successivo
-   Identificatore dell'interfaccia in uscita
-   Stato dell'hop successivo
-   Flag associati all'hop successivo
-   Informazioni private per il proprietario dell'hop successivo
-   Handle per la destinazione corrispondente all'hop successivo remoto

 

 




