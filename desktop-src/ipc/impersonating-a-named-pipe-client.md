---
description: La rappresentazione è la capacità di esecuzione di un thread in un contesto di sicurezza diverso da quello del processo a cui appartiene il thread.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Rappresentazione di un client named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305722"
---
# <a name="impersonating-a-named-pipe-client"></a>Rappresentazione di un client named pipe

La *rappresentazione* è la capacità di esecuzione di un thread in un contesto di sicurezza diverso da quello del processo a cui appartiene il thread. La rappresentazione consente al thread del server di eseguire azioni per conto del client, ma entro i limiti del contesto di sicurezza del client. Il client ha in genere un livello inferiore di diritti di accesso. Per ulteriori informazioni, vedere [rappresentazione](/windows/desktop/SecAuthZ/client-impersonation).

Un thread del server named pipe può chiamare la funzione [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) per presupporre che il token di accesso dell'utente sia connesso all'estremità client della pipe. Un server named pipe, ad esempio, può fornire l'accesso a un database o file system a cui il server pipe dispone di accesso con privilegi. Quando un client pipe invia una richiesta al server, il server rappresenta il client e tenta di accedere al database protetto. Il sistema concede o nega l'accesso del server, in base al livello di sicurezza del client. Al termine del server, viene usata la funzione [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) per ripristinare il token di sicurezza originale.

Il [livello di rappresentazione](/windows/desktop/SecAuthZ/impersonation-levels) determina le operazioni che il server può eseguire durante la rappresentazione del client. Per impostazione predefinita, un server rappresenta il livello di rappresentazione SecurityImpersonation. Tuttavia, quando il client chiama la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per la fine client della pipe, il client può utilizzare il flag di sicurezza \_ SQOS \_ presente per controllare il livello di rappresentazione del server.

 

 
