---
description: Un gestore di credenziali è simile a un provider di rete in quanto fornisce punti di ingresso chiamati dal router a più provider(MPR). In realtà, alcuni provider di rete sono anche gestori di credenziali.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a33b1a47ff17123a1974823d7fee1421df7755850d46d2992fec51f62f5fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008829"
---
# <a name="credential-manager"></a>Gestione credenziali

Un gestore di credenziali è simile a un provider di rete in quanto fornisce punti di ingresso chiamati dal router a più provider(MPR). [](/windows/desktop/SecGloss/m-gly) In realtà, alcuni provider di rete sono anche gestori di credenziali.

L'implementazione delle funzioni di gestione delle credenziali nella stessa DLL delle funzioni del provider di rete dipende dai requisiti dell'applicazione. I gestori delle credenziali ricevono notifiche quando le informazioni di autenticazione vengono cambiate. Ad esempio, i gestori delle credenziali vengono informati quando un utente esegue l'accesso o viene modificata la password di un account. Quando un processo di accesso, ad esempio [*Winlogon*](/windows/desktop/SecGloss/w-gly), esegue l'accesso o la modifica della password per un account, chiama la funzione MPR Windows Networking (WNet) appropriata. La MPR chiama quindi il punto di ingresso appropriato per ogni gestore di credenziali. Queste funzioni di gestione delle credenziali verranno sempre chiamate nel contesto di sistema, LocalSystem, anziché nel contesto utente. Per altre informazioni sulle funzioni WNet, vedere Windows [Networking](/windows/desktop/WNet/windows-networking-wnet-). Per altre informazioni sull'interfaccia che i gestori di credenziali devono implementare, vedere [**Credential API Gestione**](credential-management-api.md).

 

 
