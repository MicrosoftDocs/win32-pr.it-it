---
title: Ruolo di Network List Manager
description: Ruolo di Network List Manager
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec37d0cf157b87bf43fe12e9aa3a33eb316b7800474dd75ef3a6d4e23bb6189d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780491"
---
# <a name="the-role-of-network-list-manager"></a>Ruolo di Network List Manager

Prima di Windows XP e Windows Server 2003, le applicazioni dovevano chiamare diverse API non correlate per ottenere dati sugli attributi di rete, ad esempio l'indirizzo IP, il controller di dominio o il Domain Name System (DNS). A partire da Windows XP e Windows Server 2003, l'API Winsock di Riconoscimento percorso di rete presentava un set limitato di funzionalità di percorso di rete. In Windows Server 2008 e Windows Vista, il servizio di riconoscimento della rete acquisisce gli attributi di rete in un'unica posizione e consente alle applicazioni di eseguire query e recuperare reti e attributi specifici. Network List Manager sostituisce la funzionalità dell'API Winsock precedente (disponibile come provider di spazio dei nomi Winsock) mantenendo la compatibilità con le applicazioni precedenti usando l'API Winsock.

 

 




