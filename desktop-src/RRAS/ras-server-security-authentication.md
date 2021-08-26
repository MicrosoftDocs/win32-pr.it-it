---
title: Autenticazione di sicurezza del server RAS
description: Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione RasSecurityDialogBegin della DLL di sicurezza RAS registrata, se presente.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028741"
---
# <a name="ras-server-security-authentication"></a>Autenticazione di sicurezza del server RAS

Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) della DLL di sicurezza RAS registrata, se presente. Questa chiamata notifica alla DLL di sicurezza di avviare l'autenticazione dell'utente remoto. Il server RAS chiama **RasSecurityDialogBegin prima** di eseguire l'autenticazione PPP o RAS.

La [**chiamata RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa le informazioni seguenti alla DLL di sicurezza:

-   Handle di porta per identificare la connessione.
-   Puntatori ai buffer da utilizzare durante la comunicazione con l'utente remoto.
-   Puntatore a una [**funzione RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) da chiamare al termine dell'autenticazione.

L'handle di porta e i puntatori del buffer sono validi fino a quando la DLL di sicurezza non chiama [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) per terminare la transazione di autenticazione.

[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica al server RAS i risultati dell'autenticazione dell'utente remoto da parte della DLL di sicurezza. Se la DLL di sicurezza segnala l'esito positivo, il server RAS procede con l'autenticazione PPP e RAS dell'utente remoto. Se la DLL di sicurezza segnala che l'utente remoto non ha superato l'autenticazione o che si è verificato un errore, il server RAS si blocca e registra l'errore o l'autenticazione non riuscita nel registro eventi.

 

 




