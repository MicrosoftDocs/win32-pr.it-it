---
description: API di gestione delle credenziali
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API di gestione delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757289"
---
# <a name="credential-management-api"></a>API di gestione delle credenziali

Le funzioni di gestione delle credenziali costituiscono il set di funzioni che devono essere implementate da Gestione credenziali. Si tratta di:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), una funzione del gestore eventi chiamata da MPR quando un utente esegue l'accesso.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), una funzione del gestore eventi chiamata da MPR quando viene modificata la password di un account.

Le funzioni di gestione delle credenziali vengono sempre chiamate nel contesto di sistema (LocalSystem), anziché nel contesto utente.

Per ulteriori informazioni su come creare e registrare un'applicazione Gestione credenziali, vedere [Implementing a Credential Manager](implementing-a-credential-manager.md) e [Registering Network providers and Credential](registering-network-providers-and-credential-managers.md)managers.

 

 



