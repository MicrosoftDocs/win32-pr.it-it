---
description: Illustra le interazioni tra Winlogon e i provider di rete.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interazione con i provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab78e17536df4446ac1f57291ec77bc6ba273a825b4911e4c8bee10d389e008f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015741"
---
# <a name="interaction-with-network-providers"></a>Interazione con i provider di rete

È possibile configurare un sistema per supportare zero o più provider di rete. Ognuno di questi provider di rete può specificare che richiede un'elaborazione dell'autenticazione interattiva speciale. Questa funzionalità consente alle reti installate di raccogliere informazioni di identificazione e autenticazione specifiche per ogni rete, ma consente di raccoglierle durante il normale accesso e sotto l'ombrello sicuro del contesto e del desktop di [*Winlogon.*](../secgloss/w-gly.md) [](../secgloss/c-gly.md)

Winlogon chiama i provider di rete in diverse circostanze. Dopo un accesso riuscito, Winlogon chiama i provider di rete in modo che possano raccogliere [*le credenziali*](../secgloss/c-gly.md) e autenticare l'utente per la propria rete. Winlogon chiama anche i provider di rete quando gli utenti modificano le password. Ciò consente a ogni utente di mantenere una singola password da usare in tutte le reti.

La [**struttura WLX \_ MPR NOTIFY \_ \_ INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) viene usata per fornire informazioni di identificazione e autenticazione nelle funzioni GINA pertinenti. Questa struttura include i membri seguenti.



| Membro             | Descrizione                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Nome dell'account dell'utente connesso.                                                                                                                                                      |
| **pszDomain**      | Nome di dominio dell'utente connesso. Non tutti i modelli di autenticazione hanno un concetto di dominio (o il relativo equivalente), quindi questo membro può essere **NULL.**                                              |
| **pszPassword**    | Quando l'utente ha fornito una password in testo non crittografato durante l'autenticazione, specificandola in questo caso consente ad altri provider di rete di usare la stessa password (per ottenere l'accesso singolo) senza chiedere conferma all'utente.    |
| **pszOldPassword** | Dopo una modifica della password, specificando qui la password originale e la nuova password nel membro **pszPassword,** i provider di rete possono aggiornare le password senza chiedere conferma all'utente. |



 

[*Un'istanza DIA*](../secgloss/g-gly.md) non deve fornire queste informazioni ai provider di rete. Se viene **passato un puntatore NULL** anziché un puntatore di struttura valido, i provider di rete richiederanno informazioni all'utente.

 

 
