---
title: Amministrazione dell'account utente RAS
description: Un Windows NT server RAS 4.0 usa un database di account utente che contiene informazioni su un set di account utente.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6254a2d4066c6b4b4e1f1167ec842cd86c07d8122b0683c985cbea0a8ca7f2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028731"
---
# <a name="ras-user-account-administration"></a>Amministrazione dell'account utente RAS

Un Windows NT server RAS 4.0 usa un database di account utente che contiene informazioni su un set di account utente. Le informazioni includono i privilegi RAS di un utente, ovvero un set di flag di bit che determinano la modalità di risposta del server RAS quando l'utente chiama per connettersi. Le funzioni di amministrazione del server RAS consentono di individuare il database degli account utente e di ottenere e impostare i privilegi RAS per gli account utente.

Un server RAS Windows NT 4.0 può far parte di un dominio di Windows NT/Windows 2000 oppure può essere un server Windows NT autonomo o una workstation che non fa parte di un dominio. Per un server che fa parte di un dominio, il database degli account utente viene archiviato nel server che rappresenta il controller di dominio primario (PDC). Un server autonomo archivia il proprio database dell'account utente locale. Per ottenere il nome del server in cui è archiviato il database dell'account utente usato da un server RAS specificato, è possibile chiamare la [**funzione RasAdminGetUserAccountServer.**](rasadmingetuseraccountserver.md) È quindi possibile usare il nome del server account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti in un database dell'account utente. È anche possibile usare il nome del server nelle chiamate alle funzioni [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) per ottenere e impostare i privilegi RAS per un account utente specificato.

Le [**funzioni RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) usano la struttura [**RAS USER \_ \_ 0**](ras-user-0-str.md) per specificare i privilegi RAS di un utente e il numero di telefono di chiamata. I privilegi RAS indicano le informazioni seguenti:

-   Indica se l'utente può stabilire una connessione remota al server o al dominio a cui appartiene il server.
-   Indica se l'utente può stabilire una connessione tramite un call-back, in cui il server RAS si blocca e quindi richiama l'utente per stabilire la connessione.

Ogni account utente specifica uno dei flag seguenti per indicare il privilegio di richiamo dell'utente.



| Valore                      | Significato                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | Il server RAS non chiamerà l'utente per stabilire una connessione.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Quando l'utente chiama, il server RAS si blocca e chiama un numero di telefono di chiamata predefinito archiviato nel database dell'account utente. Il **membro szPhoneNumber** della struttura [**RAS USER \_ \_ 0**](ras-user-0-str.md) contiene il numero di telefono di chiamata dell'utente. |
| RASPRIV \_ CallerSetCallback | Quando l'utente chiama, il server RAS offre la possibilità di specificare un numero di telefono di chiamata. L'utente può anche scegliere di connettersi immediatamente senza alcuna chiamata. Il **membro szPhoneNumber** contiene un numero predefinito di cui l'utente può eseguire l'override.      |



 

 

 