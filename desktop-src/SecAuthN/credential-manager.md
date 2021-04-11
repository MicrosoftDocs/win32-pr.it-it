---
description: Una gestione credenziali è simile a un provider di rete in quanto fornisce punti di ingresso che vengono chiamati dal router multi-provider (MPR). Alcuni provider di rete sono infatti anche gestori di credenziali.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050244"
---
# <a name="credential-manager"></a>Gestione credenziali

Una gestione credenziali è simile a un provider di rete in quanto fornisce punti di ingresso che vengono chiamati dal [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR). Alcuni provider di rete sono infatti anche gestori di credenziali.

Se si implementano le funzioni di gestione delle credenziali nella stessa DLL, le funzioni del provider di rete dipendono dai requisiti dell'applicazione. I gestori delle credenziali ricevono le notifiche quando vengono modificate le informazioni di autenticazione. Ad esempio, i gestori delle credenziali ricevono una notifica quando un utente esegue l'accesso o la password di un account viene modificata. Quando un processo di accesso, ad esempio [*Winlogon*](/windows/desktop/SecGloss/w-gly), sta eseguendo l'accesso o la modifica della password per un account, chiama la funzione WNet (MPR Windows Networking) appropriata. Il MPR chiama quindi il punto di ingresso appropriato per ogni gestore delle credenziali. Queste funzioni di gestione delle credenziali verranno sempre chiamate nel contesto di sistema, LocalSystem, anziché nel contesto utente. Per ulteriori informazioni sulle funzioni WNet, vedere la pagina relativa alla [rete Windows](/windows/desktop/WNet/windows-networking-wnet-). Per ulteriori informazioni sull'interfaccia che deve essere implementata dai responsabili delle credenziali, vedere [**API di gestione delle credenziali**](credential-management-api.md).

 

 
