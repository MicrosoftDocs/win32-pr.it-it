---
title: Amministrazione utenti RAS
description: Un server RAS usa un database di account utente che contiene informazioni su un set di account utente.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- Amministrazione RAS RRAS , amministrazione utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e4916a9cf6138ebb6c201e9301feacbe332649036e7eb18075df621512a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028641"
---
# <a name="ras-user-administration"></a>Amministrazione utenti RAS

Un server RAS usa un database di account utente che contiene informazioni su un set di account utente. Le informazioni includono i privilegi RAS di un utente, ovvero un set di flag di bit che determinano la modalità di risposta del server RAS quando l'utente chiama per connettersi. Le funzioni di amministrazione del server RAS individuano il database dell'account utente e ottengono e impostano i privilegi RAS per gli account utente.

Un server RAS può far parte di un dominio del sistema operativo o può essere un computer autonomo che esegue il server o la versione professionale del sistema operativo. Per un server che fa parte di un dominio, il database degli account utente viene archiviato nel server che rappresenta il controller di dominio primario (PDC). Un server autonomo archivia il proprio database dell'account utente locale. Per ottenere il nome del server in cui è archiviato il database dell'account utente utilizzato da un server RAS specificato, è possibile chiamare la [**funzione MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) È quindi possibile usare il nome del server account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti in un database dell'account utente. È anche possibile usare il nome del server nelle chiamate alle funzioni [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) per ottenere e impostare i privilegi RAS per un account utente specificato.

Le [**funzioni MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usano la struttura [**RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) per specificare i privilegi RAS di un utente e il numero di telefono di chiamata. I privilegi RAS indicano le informazioni seguenti:

-   Indica se l'utente può stabilire una connessione remota al server o al dominio a cui appartiene il server.
-   Indica se l'utente stabilisce una connessione tramite una chiamata, in cui il server RAS si blocca e quindi richiama l'utente per stabilire la connessione.

Ogni account utente specifica uno dei flag seguenti per indicare i privilegi di richiamo dell'utente.



| Valore                      | Significato                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | Il server RAS non richiama l'utente per stabilire una connessione.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Quando l'utente chiama, il server RAS si blocca e chiama un numero di telefono di chiamata predefinito archiviato nel database dell'account utente. Il **membro szPhoneNumber** della struttura [**RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contiene il numero di telefono di chiamata dell'utente.                       |
| RASPRIV \_ CallerSetCallback | Quando l'utente chiama, il server RAS offre la possibilità di specificare un numero di telefono a cui richiamare l'utente. L'utente può anche scegliere di connettersi immediatamente senza la chiamata. Il **membro szPhoneNumber** contiene un numero predefinito di cui l'utente può eseguire l'override. |



 

 

 