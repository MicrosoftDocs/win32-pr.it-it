---
description: Credenziali API Gestione
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: Credenziali API Gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008839"
---
# <a name="credential-management-api"></a>Credenziali API Gestione

Le funzioni di gestione delle credenziali costituiscono il set di funzioni che un gestore di credenziali deve implementare. Si tratta di:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), una funzione del gestore eventi chiamata dall'MPR quando un utente accede.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), una funzione del gestore eventi chiamata dalla reimpostazione della password dell'account quando viene modificata la password di un account.

Le funzioni di gestione delle credenziali vengono sempre chiamate nel contesto di sistema (LocalSystem) anziché nel contesto utente.

Per altre informazioni su come creare e registrare un'applicazione di gestione delle credenziali, [vedere Implementing a Gestione credenziali](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).

 

 



