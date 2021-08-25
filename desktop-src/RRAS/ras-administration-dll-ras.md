---
title: DLL di amministrazione RAS
description: La DLL esporta le funzioni chiamate dal server RAS ogni volta che un utente tenta di connettersi o disconnettersi.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6be479d00175750fb4d6ffce73aab4439d2c7df9e6e07f97e9964f267ce82a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909921"
---
# <a name="ras-administration-dll"></a>DLL di amministrazione RAS

La DLL esporta le funzioni chiamate dal server RAS ogni volta che un utente tenta di connettersi o disconnettersi. È possibile usare la DLL per eseguire le funzioni amministrative seguenti:

-   Decidere se consentire a un utente di connettersi al server. Ciò può fornire un controllo di sicurezza oltre all'autenticazione utente RAS standard.
-   Registrare l'ora in cui ogni utente si connette e si disconnette dal server. Ciò può essere utile a scopo di fatturazione o controllo.
-   Assegnare un indirizzo IP a ogni utente. Ciò può essere utile per motivi di sicurezza per eseguire il mapping della connessione di un utente a un computer specifico.

Quando si sviluppa una DLL di amministrazione del server RAS, implementare le funzioni seguenti.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Una DLL di amministrazione RAS deve implementare ed esportare tutte le funzioni precedenti. Se una delle funzioni non viene implementata, il servizio di accesso remoto non verrà avviato.

Le [**funzioni RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) consentono alla DLL di controllare le connessioni utente al server. Un server WINDOWS NT/Windows 2000 chiama la funzione **RasAdminAcceptNewConnection** ogni volta che un utente tenta di connettersi. La funzione può impedire all'utente di connettersi. È anche possibile usare la funzione per generare una voce in un log per la fatturazione o il controllo. Quando l'utente si disconnette, il server RAS chiama la funzione **RasAdminConnectionHangupNotification,** che può registrare l'ora in cui l'utente si è disconnesso.

Dopo che il server RAS ha autenticato un chiamante, chiama la funzione [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) per ottenere un indirizzo IP per il client remoto. La DLL può usare questa funzione per fornire uno schema alternativo per il mapping di un indirizzo IP a un utente connesso. Se **RasAdminGetIpAddressForUser** non è implementato, un server RAS connette un utente remoto a un indirizzo IP selezionato da un pool statico di indirizzi IP o da un server Dynamic Host Configuration Protocol (DHCP). La **funzione RasAdminGetIpAddressForUser** consente alla DLL di eseguire l'override di questo indirizzo IP predefinito e di specificare un indirizzo IP specifico per ogni utente. La **funzione RasAdminGetIpAddressForUser** può impostare un flag che fa in modo che RAS chiami la funzione [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) quando l'utente si disconnette. La DLL può usare [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) per aggiornare la mappa da utente a indirizzo IP.

RAS serializza le chiamate nella DLL di amministrazione. Una chiamata a una delle funzioni della DLL per un determinato client RAS non verrà mai sottuta da una chiamata a tale funzione per un client RAS diverso. È garantito che la chiamata iniziale venga completata prima che RAS chiami la funzione per l'altro client. Inoltre, la serializzazione si estende a determinati gruppi di funzioni. Le funzioni degli indirizzi IP vengono serializzate come gruppo. Una chiamata a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) o [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloccherà le chiamate in entrambi fino al completamento della chiamata iniziale. [**Anche RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) vengono serializzati come gruppo.

RAS esegue le funzioni per l'assegnazione di indirizzi IP in un processo ed esegue le funzioni per le notifiche di connessione e disconnessione in un altro processo. Di conseguenza, la DLL non deve dipendere da dati condivisi tra i due set di funzioni.

Il server RAS registra un errore nel registro eventi di sistema se si verifica un errore quando tenta di caricare una DLL di amministrazione RAS o quando si chiama una delle funzioni della DLL. Ciò può verificarsi, ad esempio, se la DLL ha specificato il nome errato per una funzione esportata o se non include il nome della funzione nel file def. La voce nel registro eventi indica il motivo dell'errore.

**Windows 2000 Server e versioni successive:** Le DLL di amministrazione RAS che implementano questa interfaccia di funzione non funzionano più. Usare invece l'interfaccia della funzione MprAdmin fornita con le versioni più recenti di Windows. Per altre informazioni, vedere le informazioni [di riferimento sull'amministrazione RAS](remote-access-service-administration-reference.md) nella documentazione relativa a Routing e RAS.

 

 




