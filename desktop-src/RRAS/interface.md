---
title: Interfaccia (RRAS)
description: Un'interfaccia è una connessione logica a una rete. Ogni interfaccia è identificata da un indice univoco. I protocolli di routing multicast , ad esempio MOSPF, si occupano di tutti i tipi di interfacce in modo analogo.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1347f1a8d9afd049dd8283e7199c6da7d8a9dce6990a1e7ea674943f32811f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030161"
---
# <a name="interface-rras"></a>Interfaccia (RRAS)

Un'interfaccia è una connessione logica a una rete. Ogni interfaccia è identificata da un indice univoco. I protocolli di routing multicast , ad esempio MOSPF, si occupano di tutti i tipi di interfacce in modo analogo.

Nel caso di un'interfaccia LAN, l'interfaccia corrisponde a un dispositivo fisico effettivo nel computer (scheda LAN). Nel caso di un'interfaccia WAN, l'interfaccia viene mappata a una porta quando viene stabilita una connessione. Le interfacce WAN possono essere basate su tunnel e la porta può essere una porta di rete privata virtuale (VPN).

Windows sistemi operativi 2000 e versioni successive supportano un'interfaccia da punto a multipunto. Questo tipo di interfaccia può essere visualizzato come una raccolta di collegamenti da punto a punto che condividono un singolo punto di terminazione.

Per identificare in modo univoco un collegamento esatto in un'interfaccia da punto a multipunto, l'API MGM usa l'indirizzo hop successivo dell'ID interfaccia. Per supportare questa identificazione, l'API MGM usa un ID di interfaccia estesa, che include un [indirizzo hop](next-hop.md) successivo.

 

 




