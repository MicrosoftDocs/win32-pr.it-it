---
description: Una trasmissione generale attraverso Internet viene eseguita impostando i campi SA \_ netnum e sa \_ nodenum su quelli binari (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Tutte le route trasmesse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484964"
---
# <a name="all-routes-broadcast"></a>Tutte le route trasmesse

Una trasmissione generale attraverso Internet viene eseguita impostando i campi **sa \_ netnum** e **sa \_ nodenum** su quelli binari (1). Il provider di servizi traduce la richiesta in un pacchetto di tipo-20, che i router IPX riconoscono e inoltrano. Il pacchetto visita tutte le subnet e può essere duplicato più volte. I ricevitori devono gestire diverse copie duplicate del datagramma.

L'uso di questo tipo di trasmissione non è popolare tra gli amministratori di rete, quindi il suo utilizzo dovrebbe essere estremamente limitato. Molti router disabilitano questo tipo di trasmissione, lasciando le parti della subnet invisibili al pacchetto.

 

 



