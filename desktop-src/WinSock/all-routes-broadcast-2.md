---
description: Una trasmissione generale tramite Internet viene ottenuta impostando i campi \_ nodenum sa netnum e sa su valori binari \_ (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Tutte le route trasmesse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322722"
---
# <a name="all-routes-broadcast"></a>Tutte le route trasmesse

Una trasmissione generale tramite Internet viene ottenuta impostando i campi **\_ nodenum sa** **\_ netnum** e sa su valori binari (1). Il provider di servizi converte la richiesta in un pacchetto di tipo 20, che i router IPX riconoscono e inoltrano. Il pacchetto visita tutte le subnet e può essere duplicato più volte. I ricevitori devono gestire diverse copie duplicate del datagramma.

L'uso di questo tipo di trasmissione non è popolare tra gli amministratori di rete, quindi l'uso di questo tipo di trasmissione dovrebbe essere estremamente limitato. Molti router disabilitano questo tipo di trasmissione, lasciando parti della subnet invisibili al pacchetto.

 

 



