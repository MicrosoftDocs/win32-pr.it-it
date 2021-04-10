---
title: Interfaccia (RRAS)
description: Un'interfaccia è una connessione logica a una rete. Ogni interfaccia è identificata da un indice univoco. I protocolli di routing multicast (ad esempio MOSPF) gestiscono tutti i tipi di interfacce in modo analogo.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963658"
---
# <a name="interface-rras"></a>Interfaccia (RRAS)

Un'interfaccia è una connessione logica a una rete. Ogni interfaccia è identificata da un indice univoco. I protocolli di routing multicast (ad esempio MOSPF) gestiscono tutti i tipi di interfacce in modo analogo.

Nel caso di un'interfaccia LAN, l'interfaccia corrisponde a un dispositivo fisico reale nel computer (scheda LAN). Nel caso di un'interfaccia WAN, viene eseguito il mapping dell'interfaccia a una porta quando viene stabilita una connessione. Le interfacce WAN possono essere basate sui tunnel e la porta potrebbe essere una porta di rete privata virtuale (VPN).

I sistemi operativi Windows 2000 e versioni successive supportano un'interfaccia "da punto a multipoint". Questo tipo di interfaccia può essere visualizzato come una raccolta di collegamenti Point-to-Point che condividono un singolo punto di terminazione.

Per identificare in modo univoco un collegamento esatto in un'interfaccia Point-to-multipoint, l'API MGM usa l'indirizzo hop successivo dell'ID di interfaccia. Per supportare questa identificazione, l'API MGM usa un ID di interfaccia esteso, che include un indirizzo [hop successivo](next-hop.md) .

 

 




