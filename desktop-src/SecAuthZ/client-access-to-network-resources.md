---
description: Illustra le strategie per l'accesso alle risorse di rete.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Accesso client alle risorse di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308655"
---
# <a name="client-access-to-network-resources"></a>Accesso client alle risorse di rete

Un server può utilizzare le strategie seguenti per accedere alle risorse di rete:

-   Se il server ha il nome account e la password di un client, può chiamare [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con le [*credenziali*](/windows/desktop/SecGloss/c-gly) del client per eseguire il mapping di una lettera di unità locale a una condivisione di rete.
-   Dopo aver chiamato [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) con le credenziali client, il server può chiamare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per [creare un processo per il client](processes-in-the-client-security-context.md). Questo nuovo processo client può accedere alle risorse di rete usando il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly)del client. Ad esempio, il processo può chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un file in un computer remoto. Il sistema usa il [*token primario*](/windows/desktop/SecGloss/p-gly) del client per controllare i tentativi di accesso da parte del processo client.
-   Un server può chiamare [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con credenziali null per stabilire una connessione a una risorsa di rete con accesso al server o una connessione predefinita. Se il server è in esecuzione con l'account LocalSystem, viene autenticato nella risorsa di rete nel [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) del server di dominio. Se il server è in esecuzione con un account del servizio, viene autenticato con l'account. Per ulteriori informazioni, vedere l' [account LocalSystem](/windows/desktop/Services/localsystem-account).

Per informazioni sulla protezione delle password, vedere [gestione delle password](/windows/desktop/SecBP/handling-passwords). Per informazioni sull'acquisizione di credenziali, vedere [richiesta di credenziali all'utente](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
