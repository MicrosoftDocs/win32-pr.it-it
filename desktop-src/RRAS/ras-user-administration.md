---
title: Amministrazione utenti RAS
description: Un server RAS utilizza un database di account utente che contiene informazioni su un set di account utente.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- Amministrazione RAS RRAS, amministrazione utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3e357ef813a60c67f991b6e5829879d3e1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300302"
---
# <a name="ras-user-administration"></a>Amministrazione utenti RAS

Un server RAS utilizza un database di account utente che contiene informazioni su un set di account utente. Le informazioni includono i privilegi RAS di un utente, ovvero un set di flag di bit che determinano il modo in cui il server RAS risponde quando l'utente chiama per connettersi. Le funzioni di amministrazione del server RAS individuano il database degli account utente e ottengono e impostano i privilegi RAS per gli account utente.

Un server RAS può far parte di un dominio del sistema operativo oppure può essere un computer autonomo che esegue la versione server o Professional del sistema operativo. Per un server che fa parte di un dominio, il database degli account utente viene archiviato nel server che è il controller di dominio primario (PDC). Un server autonomo archivia il proprio database di account utente locale. Per ottenere il nome del server in cui è archiviato il database degli account utente utilizzato da un server RAS specificato, è possibile chiamare la funzione [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) . È quindi possibile utilizzare il nome del server di account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti in un database di account utente. È anche possibile usare il nome del server nelle chiamate alle funzioni [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) per ottenere e impostare i privilegi RAS per un account utente specificato.

Le funzioni [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usano la struttura [**RAS \_ User \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) per specificare i privilegi RAS e il numero di telefono di un utente. I privilegi RAS indicano le seguenti informazioni:

-   Indica se l'utente può stabilire una connessione remota al server o al dominio a cui appartiene il server.
-   Indica se l'utente stabilisce una connessione tramite una chiamata, in cui il server RAS si blocca e quindi richiama l'utente per stabilire la connessione.

Ogni account utente specifica uno dei flag seguenti per indicare i privilegi di richiamata dell'utente.



| Valore                      | Significato                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NoCallback RASPRIV \_        | Il server RAS non richiama l'utente per stabilire una connessione.                                                                                                                                                                                                          |
| \_ADMINSETCALLBACK RASPRIV  | Quando l'utente chiama, il server RAS si blocca e chiama un numero di telefono di chiamata predefinito archiviato nel database degli account utente. Il membro **szPhoneNumber** della struttura [**RAS \_ User \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contiene il numero di telefono di chiamata dell'utente.                       |
| \_CALLERSETCALLBACK RASPRIV | Quando l'utente chiama, il server RAS fornisce la possibilità di specificare un numero di telefono in cui richiamare l'utente. L'utente può anche scegliere di connettersi immediatamente senza richiamarlo. Il membro **szPhoneNumber** contiene un numero predefinito di cui l'utente può eseguire l'override. |



 

 

 