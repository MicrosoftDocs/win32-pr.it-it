---
title: Ruolo di Network List Manager
description: Ruolo di Network List Manager
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856941"
---
# <a name="the-role-of-network-list-manager"></a>Ruolo di Network List Manager

Prima di Windows XP e Windows Server 2003, era necessario che le applicazioni chiamassero diverse API non correlate per ottenere i dati sugli attributi di rete, ad esempio l'indirizzo IP, il controller di dominio o il Domain Name System (DNS). A partire da Windows XP e Windows Server 2003, l'API Winsock di riconoscimento del percorso di rete include un set limitato di funzionalità relative al percorso di rete. In Windows Server 2008 e Windows Vista, il servizio Network Awareness acquisisce gli attributi di rete in un'unica posizione e consente alle applicazioni di eseguire query e recuperare specifiche reti e attributi. Network List Manager sostituisce la funzionalità dell'API Winsock precedente (disponibile come provider di spazio dei nomi Winsock) mantenendo la compatibilità con le applicazioni meno recenti tramite l'API Winsock.

 

 




