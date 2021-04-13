---
title: Amministrazione account utente RAS
description: Un server RAS Windows NT 4,0 utilizza un database di account utente che contiene informazioni su un set di account utente.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d090fc16e7d731525b79493119f3c604e043c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337806"
---
# <a name="ras-user-account-administration"></a>Amministrazione account utente RAS

Un server RAS Windows NT 4,0 utilizza un database di account utente che contiene informazioni su un set di account utente. Le informazioni includono i privilegi RAS di un utente, ovvero un set di flag di bit che determinano il modo in cui il server RAS risponde quando l'utente chiama per connettersi. Le funzioni di amministrazione del server RAS consentono di individuare il database degli account utente e di ottenere e impostare i privilegi RAS per gli account utente.

Un server RAS Windows NT 4,0 può far parte di un dominio Windows NT/Windows 2000 oppure può essere una workstation o un server Windows NT autonomo che non fa parte di un dominio. Per un server che fa parte di un dominio, il database degli account utente viene archiviato nel server che è il controller di dominio primario (PDC). Un server autonomo archivia il proprio database di account utente locale. Per ottenere il nome del server in cui è archiviato il database degli account utente utilizzato da un server RAS specificato, è possibile chiamare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) . È quindi possibile utilizzare il nome del server di account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti in un database di account utente. È anche possibile usare il nome del server nelle chiamate alle funzioni [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) per ottenere e impostare i privilegi RAS per un account utente specificato.

Le funzioni [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) usano la struttura [**RAS \_ User \_ 0**](ras-user-0-str.md) per specificare i privilegi RAS e il numero di telefono di un utente. I privilegi RAS indicano le seguenti informazioni:

-   Indica se l'utente può stabilire una connessione remota al server o al dominio a cui appartiene il server.
-   Indica se l'utente è in grado di stabilire una connessione tramite un callback, in cui il server RAS si blocca e quindi richiama l'utente per stabilire la connessione.

Ogni account utente specifica uno dei flag seguenti per indicare il privilegio di richiamata dell'utente.



| Valore                      | Significato                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NoCallback RASPRIV \_        | Il server RAS non chiamerà di nuovo l'utente per stabilire una connessione.                                                                                                                                                                                        |
| \_ADMINSETCALLBACK RASPRIV  | Quando l'utente chiama, il server RAS si blocca e chiama un numero di telefono di chiamata predefinito archiviato nel database degli account utente. Il membro **szPhoneNumber** della struttura [**RAS \_ User \_ 0**](ras-user-0-str.md) contiene il numero di telefono di chiamata dell'utente. |
| \_CALLERSETCALLBACK RASPRIV | Quando l'utente chiama, il server RAS fornisce la possibilità di specificare un numero di telefono di chiamata. L'utente può anche scegliere di connettersi immediatamente senza richiamarlo. Il membro **szPhoneNumber** contiene un numero predefinito di cui l'utente può eseguire l'override.      |



 

 

 