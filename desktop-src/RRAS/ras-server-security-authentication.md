---
title: Autenticazione della sicurezza del server RAS
description: Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione RasSecurityDialogBegin della DLL di sicurezza RAS registrata, se disponibile.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044622"
---
# <a name="ras-server-security-authentication"></a>Autenticazione della sicurezza del server RAS

Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) della DLL di sicurezza RAS registrata, se disponibile. Questa chiamata notifica alla DLL di sicurezza di iniziare l'autenticazione dell'utente remoto. Il server RAS chiama **RasSecurityDialogBegin** prima di eseguire l'autenticazione PPP o RAS.

La chiamata [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa le informazioni seguenti alla DLL di sicurezza:

-   Handle di porta per identificare la connessione.
-   Puntatori ai buffer da usare durante la comunicazione con l'utente remoto.
-   Puntatore a una funzione [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) da chiamare al termine dell'autenticazione.

Il punto di controllo della porta e i puntatori del buffer sono validi finché la DLL di sicurezza non chiama [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) per terminare la transazione di autenticazione.

Il [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica al server RAS i risultati dell'autenticazione della DLL di sicurezza dell'utente remoto. Se la DLL di sicurezza segnala l'esito positivo, il server RAS procede con l'autenticazione PPP e RAS dell'utente remoto. Se la DLL di sicurezza segnala che l'utente remoto non è riuscito a eseguire l'autenticazione o si è verificato un errore, il server RAS si blocca e registra l'errore o l'autenticazione non riuscita nel registro eventi.

 

 




