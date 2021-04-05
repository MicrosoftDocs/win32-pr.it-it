---
title: Supporto host sicurezza RAS
description: Windows NT 4,0 fornisce un modo per una DLL di sicurezza RAS di terze parti per migliorare le funzionalità di protezione RAS predefinite. Windows 95 non fornisce questo supporto.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Supporto host, RAS
- Supporto host sicurezza, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711740"
---
# <a name="ras-security-host-support"></a>Supporto host sicurezza RAS

Windows NT 4,0 fornisce un modo per una DLL di sicurezza RAS di terze parti per migliorare le funzionalità di protezione RAS predefinite. Windows 95 non fornisce questo supporto.

Un server RAS Windows NT/Windows 2000 fornisce meccanismi di sicurezza per la convalida dell'accesso alla rete degli utenti remoti. Quando un server RAS riceve una chiamata, convalida le credenziali dell'utente nel database di account locale o di dominio. RAS supporta inoltre la sicurezza da richiamare, in cui il server RAS si blocca e quindi richiama l'utente remoto per stabilire la connessione. Per le reti in cui questo livello di protezione non è sufficiente, è possibile installare una DLL di protezione RAS di terze parti. La DLL di sicurezza può quindi autenticare un utente remoto leggendo le informazioni di sicurezza da un database diverso dal database degli account utente standard.

Quando il server RAS riceve una chiamata, richiama la DLL di sicurezza per autenticare l'utente remoto. Il supporto dell'host di sicurezza RAS fornisce un meccanismo per la comunicazione tra la DLL di sicurezza e l'utente remoto tramite una finestra del terminale nel computer remoto. In uno scenario tipico, la DLL di sicurezza richiede il nome di accesso dell'utente remoto. La DLL usa quindi il database di sicurezza privato per formulare una richiesta di invio al terminale remoto. Ad esempio, la richiesta può essere un codice che l'utente deve fornire come input a un lettore cardkey. Il lettore cardkey Visualizza quindi una risposta che l'utente remoto digita nella finestra del terminale. La DLL di sicurezza convalida quindi la risposta in base alle informazioni dell'utente nel database di sicurezza privata.

Se la DLL di sicurezza autentica l'utente remoto, il server RAS esegue la propria autenticazione. In questo modo si garantisce che la sicurezza RAS esegua sempre l'autenticazione di un utente remoto, anche se è installata una DLL di sicurezza che concede l'accesso a tutti gli utenti.

> [!Note]  
> Windows NT/Windows 2000 fornisce attualmente il supporto per gli host di sicurezza RAS solo per le connessioni asincrone del modem. altri tipi di connessioni, ad esempio Ethernet (che non è una connessione modem), VPN (che non è anche una connessione modem) o ISDN (sincrono) non sono supportati.

 

 

 




