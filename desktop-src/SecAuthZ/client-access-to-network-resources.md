---
description: Illustra le strategie per l'accesso alle risorse di rete.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Accesso client alle risorse di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8886f474876080703d190efb3419d099027f24af17dd735736957452318e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783077"
---
# <a name="client-access-to-network-resources"></a>Accesso client alle risorse di rete

Un server può usare le strategie seguenti per accedere alle risorse di rete:

-   Se il server ha il nome account e la password di un client, [](/windows/desktop/SecGloss/c-gly) può chiamare [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con le credenziali del client per eseguire il mapping di una lettera di unità locale a una condivisione di rete.
-   Dopo aver [**chiamato LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) con le credenziali client, il server può chiamare la [**funzione CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per creare [un processo per il client](processes-in-the-client-security-context.md). Questo nuovo processo client può accedere alle risorse di rete usando il contesto [*di sicurezza del*](/windows/desktop/SecGloss/s-gly)client. Ad esempio, il processo può chiamare [**la funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un file in un computer remoto. Il sistema usa il token primario del client [*per*](/windows/desktop/SecGloss/p-gly) controllare i tentativi di accesso da parte del processo client.
-   Un server può chiamare [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con credenziali Null per stabilire una connessione a una risorsa di rete con accesso al server o una connessione predefinita. Se il server è in esecuzione come account LocalSystem, esegue l'autenticazione alla risorsa di rete nel contesto [*di sicurezza*](/windows/desktop/SecGloss/s-gly) del server di dominio. Se il server è in esecuzione con un account del servizio, viene autenticato come tale account. Per altre informazioni, vedere l'account [LocalSystem.](/windows/desktop/Services/localsystem-account)

Per informazioni sulla protezione delle password, vedere [Gestione delle password.](/windows/desktop/SecBP/handling-passwords) Per informazioni sull'acquisizione delle credenziali, vedere [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
