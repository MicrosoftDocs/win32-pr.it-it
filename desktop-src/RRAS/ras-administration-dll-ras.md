---
title: DLL di amministrazione RAS
description: La DLL esporta funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0908032e0916f0937e964408b1551d3f1515dea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335668"
---
# <a name="ras-administration-dll"></a>DLL di amministrazione RAS

La DLL esporta funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi. È possibile utilizzare la DLL per eseguire le funzioni amministrative seguenti:

-   Decidere se consentire a un utente di connettersi al server. Questo può fornire un controllo di sicurezza oltre all'autenticazione utente RAS standard.
-   Registrare l'ora in cui ogni utente si connette e si disconnette dal server. Questa operazione può essere utile a scopo di fatturazione o controllo.
-   Assegnare un indirizzo IP a ogni utente. Questa operazione può essere utile a scopo di sicurezza per eseguire il mapping della connessione di un utente a un computer specifico.

Implementare le funzioni seguenti durante lo sviluppo di una DLL di amministrazione del server RAS.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Una DLL di amministrazione RAS deve implementare ed esportare tutte le funzioni descritte in precedenza. Se una delle funzioni non è implementata, il servizio di accesso remoto non verrà avviato.

Le funzioni [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RASADMINCONNECTIONHANGUPNOTIFICATION**](rasadminconnectionhangupnotification.md) consentono alla DLL di controllare le connessioni utente al server. Un server RAS Windows NT/Windows 2000 chiama la funzione **RasAdminAcceptNewConnection** ogni volta che un utente tenta di connettersi. La funzione può impedire all'utente di connettersi. È anche possibile usare la funzione per generare una voce in un log per la fatturazione o il controllo. Quando l'utente si disconnette, il server RAS chiama la funzione **RasAdminConnectionHangupNotification** , che consente di registrare l'ora in cui l'utente è stato disconnesso.

Dopo che il server RAS ha autenticato un chiamante, chiama la funzione [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) per ottenere un indirizzo IP per il client remoto. La DLL può usare questa funzione per fornire uno schema alternativo per il mapping di un indirizzo IP a un utente di connessione remota. Se **RasAdminGetIpAddressForUser** non è implementato, un server RAS connette un utente remoto a un indirizzo IP selezionato da un pool statico di indirizzi IP o uno selezionato da un server Dynamic Host Configuration Protocol (DHCP). La funzione **RasAdminGetIpAddressForUser** consente alla DLL di eseguire l'override di questo indirizzo IP predefinito e specificare un indirizzo IP specifico per ogni utente. La funzione **RasAdminGetIpAddressForUser** può impostare un flag che fa in modo che RAS chiami la funzione [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) quando l'utente si disconnette. La DLL può usare [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) per aggiornare la mappa da utente a indirizzo IP.

RAS serializza le chiamate nella DLL di amministrazione. Una chiamata a una delle funzioni della DLL per un determinato client RAS non verrà mai superata da una chiamata a tale funzione per un client RAS diverso; la chiamata iniziale può essere completata prima che RAS chiami la funzione per l'altro client. Inoltre, la serializzazione si estende a determinati gruppi di funzioni. Le funzioni degli indirizzi IP vengono serializzate come gruppo. una chiamata a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) o [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloccherà le chiamate in entrambi i casi finché la chiamata iniziale non sarà completa. [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) vengono inoltre serializzati come gruppo.

RAS esegue le funzioni per l'assegnazione di indirizzi IP in un processo ed esegue le funzioni per le notifiche di connessione e disconnessione in un altro processo. Di conseguenza, la DLL non deve dipendere da dati condivisi tra i due set di funzioni.

Il server RAS registra un errore nel registro eventi di sistema se si verifica un errore durante il tentativo di caricamento di una DLL di amministrazione RAS o quando viene chiamata una delle funzioni della DLL. Questo può accadere, ad esempio, se la DLL ha specificato il nome errato per una funzione esportata o se non include il nome della funzione nel file def. La voce nel registro eventi indica il motivo dell'errore.

**Windows 2000 Server e versioni successive:** Le DLL di amministrazione RAS che implementano questa interfaccia di funzione non funzionano più. Usare invece l'interfaccia della funzione MprAdmin fornita con le versioni più recenti di Windows. Per ulteriori informazioni, vedere le informazioni di [riferimento sull'amministrazione RAS](remote-access-service-administration-reference.md) nella documentazione relativa a routing e RAS.

 

 




