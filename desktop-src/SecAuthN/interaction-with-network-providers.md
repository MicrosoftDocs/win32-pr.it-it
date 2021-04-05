---
description: Illustra le interazioni tra i provider di rete e Winlogon.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interazione con i provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884501"
---
# <a name="interaction-with-network-providers"></a>Interazione con i provider di rete

È possibile configurare un sistema per supportare zero o più provider di rete. Ognuno di questi provider di rete può specificare di richiedere l'elaborazione interattiva speciale. Questa funzionalità consente alle reti installate di raccogliere informazioni di identificazione e autenticazione specifiche per ogni rete, ma consente loro di raccoglierle durante il normale accesso e sotto l'ombrello sicuro del [*contesto*](../secgloss/c-gly.md) e del desktop di [*Winlogon*](../secgloss/w-gly.md) .

Winlogon chiama i provider di rete in diverse circostanze. Dopo un accesso riuscito, Winlogon chiama i provider di rete in modo che possano raccogliere le [*credenziali*](../secgloss/c-gly.md) e autenticare l'utente per la rete. Winlogon chiama anche i provider di rete quando gli utenti cambiano le password. Questo consente a ogni utente di mantenere una singola password per l'uso in tutte le reti.

La struttura delle [**\_ informazioni di \_ notifica \_ di WLX MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) viene usata per fornire informazioni di identificazione e autenticazione nelle funzioni Gina pertinenti. Questa struttura include i membri seguenti.



| Membro             | Descrizione                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Nome dell'account dell'utente connesso.                                                                                                                                                      |
| **pszDomain**      | Nome di dominio dell'utente connesso. Non tutti i modelli di autenticazione hanno un concetto di dominio (o l'equivalente), pertanto questo membro può essere **null**.                                              |
| **pszPassword**    | Quando l'utente ha assegnato una password in testo non crittografato durante l'autenticazione, la fornisce qui consente agli altri provider di rete di usare la stessa password (per ottenere l'accesso singolo) senza richiedere conferma all'utente.    |
| **pszOldPassword** | Dopo una modifica della password, fornendo qui la password originale e la nuova password nel membro **pszPassword** , consente ai provider di rete di aggiornare le password senza richiedere conferma all'utente. |



 

Non è necessario che [*Gina*](../secgloss/g-gly.md) fornisca tali informazioni ai provider di rete. Se viene passato un puntatore **null** anziché un puntatore di struttura valido, i provider di rete richiederanno all'utente le informazioni.

 

 
