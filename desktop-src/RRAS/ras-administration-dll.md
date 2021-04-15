---
title: Informazioni sulle DLL di amministrazione RAS
description: La DLL di amministrazione RAS Esporta le funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- Amministrazione RAS RRAS, DLL di amministrazione RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104516531"
---
# <a name="about-ras-administration-dlls"></a>Informazioni sulle DLL di amministrazione RAS

La DLL di amministrazione RAS Esporta le funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi. Di seguito sono riportati alcuni dei possibili utilizzi di una DLL di amministrazione RAS:

-   Decidere se consentire a un utente di connettersi al server. La DLL di amministrazione può fornire un controllo di sicurezza oltre all'autenticazione utente RAS standard.
-   Registrare l'ora in cui ogni utente si connette e si disconnette dal server. Questa operazione può essere utile a scopo di fatturazione o controllo.
-   Assegnare un indirizzo IP a ogni utente. Questa funzionalità è utile per la sicurezza, perché questa funzionalità viene utilizzata per eseguire il mapping della connessione di un utente a un computer specifico.

Il percorso della DLL di amministrazione RAS è specificato nel registro di sistema. vedere [configurazione del registro di sistema della DLL di amministrazione RAS](ras-administration-dll-registry-setup.md).

RAS supporta più DLL di amministrazione. Il registro di sistema supporta più percorsi DLL. RAS chiama le funzioni nelle DLL nell'ordine in cui le dll sono elencate nel registro di sistema. vedere [configurazione del registro di sistema della DLL di amministrazione RAS](ras-administration-dll-registry-setup.md).

**Server Windows 2000:** RAS non supporta più dll.

Una DLL di amministrazione RAS deve implementare ed esportare tutte le funzioni seguenti:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

Inoltre, la DLL di amministrazione RAS deve implementare ed esportare uno dei due

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

oppure

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Se tutte le funzioni obbligatorie non sono implementate, non è possibile avviare RAS.

**Server Windows 2000:** Una DLL di amministrazione deve implementare le funzioni [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) . Se la DLL implementa una di queste funzioni, è necessario implementare anche l'altra.

RAS chiama la funzione [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) quando il servizio Routing e accesso remoto viene avviato per la prima volta. La funzione **MprAdminInitializeDll** offre un'opportunità per la dll di amministrazione di eseguire qualsiasi inizializzazione necessaria. Analogamente, RAS chiama il servizio [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) quando il servizio Routing e accesso remoto viene arrestato. Questa funzione consente alla DLL di amministrazione di eseguire le operazioni di pulizia necessarie prima di uscire.

Le funzioni [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MPRADMINCONNECTIONHANGUPNOTIFICATION**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) consentono alla DLL di controllare le connessioni utente al server. Un server RAS chiama la funzione **MprAdminAcceptNewConnection** ogni volta che un utente tenta di connettersi. Questa funzione rende possibile impedire all'utente di connettersi. La funzione **MprAdminAcceptNewConnection** può anche generare voci di log per la fatturazione o il controllo. Quando l'utente si disconnette, il server RAS chiama la funzione **MprAdminConnectionHangupNotification** , che consente di registrare l'ora in cui l'utente è stato disconnesso.

Le funzioni [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) sono simili a **MprAdminAcceptNewConnection** e [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification). Tuttavia, quando RAS chiama le funzioni **MprAdminAcceptNewConnection2** e **MprAdminConnectionHangupNotification2** , RAS passa un parametro aggiuntivo di tipo [**RAS \_ Connection \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

RAS supporta più DLL di amministrazione. L'utente di accesso remoto può connettersi solo se l'implementazione della funzione [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) in ogni dll accetta la connessione. In altre parole, ogni DLL deve accettare la connessione per consentire all'utente di connettersi.

È possibile che una singola connessione RAS utilizzi più collegamenti quando si connette a un server RAS. Le funzioni [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) e [**MPRADMINLINKHANGUPNOTIFICATION**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) consentono alla DLL di amministrazione di gestire singoli collegamenti in una connessione. RAS chiama **MprAdminAcceptNewLink** ogni volta che viene stabilito un nuovo collegamento per una connessione. Poiché tutte le connessioni coinvolgono almeno un collegamento, RAS chiama sempre **MprAdminAcceptNewLink** una volta immediatamente dopo la restituzione di [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) , purché [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) abbia accettato la connessione. RAS chiama **MprAdminLinkHangupNotification** ogni volta che un collegamento per una connessione viene arrestato.

Poiché RAS supporta più DLL di amministrazione, l'utente di accesso remoto può connettersi solo se l'implementazione della funzione [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) in ogni dll accetta la connessione. In altre parole, ogni DLL deve accettare il collegamento affinché venga stabilito il collegamento.

Dopo che il server RAS ha autenticato un utente, chiama la funzione [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) per ottenere un indirizzo IP per il client remoto. Questa funzione fornisce uno schema alternativo per il mapping di un indirizzo IP a un utente con connessione remota. Se **MprAdminGetIpAddressForUser** non è implementato, un server RAS associa l'utente remoto a un indirizzo IP selezionato da un pool statico di indirizzi IP o uno selezionato da un server Dynamic Host Configuration Protocol (DHCP). La funzione **MprAdminGetIpAddressForUser** consente alla DLL di eseguire l'override di questo indirizzo IP predefinito e specificare un indirizzo IP specifico per ogni utente. La funzione **MprAdminGetIpAddressForUser** può impostare un flag che fa in modo che RAS chiami la funzione [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) quando l'utente si disconnette. La DLL può quindi usare **MprAdminReleaseIpAddress** per aggiornare il mapping da utente a indirizzo IP.

RAS supporta più DLL di amministrazione, ma chiama le funzioni [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) solo nella prima dll che le implementa ed Esporta. RAS ignora le implementazioni di queste funzioni nelle altre dll. RAS controlla le dll per queste funzioni nell'ordine in cui sono elencate nel [Registro di sistema](ras-administration-dll-registry-setup.md).

RAS serializza le chiamate nella DLL di amministrazione. Una chiamata a una delle funzioni della DLL per un determinato client RAS non ha la precedenza su una chiamata a tale funzione per un client RAS diverso; RAS non chiama la funzione per l'altro client finché la chiamata iniziale non viene completata. Inoltre, la serializzazione si estende a determinati gruppi di funzioni. Le funzioni degli indirizzi IP vengono serializzate come gruppo. una chiamata a [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) o [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) blocca le chiamate in entrambe le funzioni fino a quando non viene restituita la chiamata iniziale. [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) vengono inoltre serializzati come gruppo.

RAS esegue le funzioni che assegnano indirizzi IP in un unico processo; le funzioni per le notifiche di connessione e disconnessione vengono eseguite in un altro processo. Di conseguenza, la DLL non dipende dai dati condivisi tra questi due set di funzioni.

Non chiamare [funzioni di amministrazione RAS](ras-administration-functions.md) o [funzioni di amministrazione dell'utente RAS](ras-user-administration-functions.md) dall'interno di una funzione di callout. Le chiamate a queste funzioni non restituiranno quando viene eseguita dall'interno di una funzione di callout.

Il server RAS registra un errore nel registro eventi di sistema se si verifica un errore durante il tentativo di caricamento di una DLL di amministrazione RAS o quando viene chiamata una delle funzioni della DLL. Questo può accadere, ad esempio, se la DLL ha specificato il nome errato per una funzione esportata o se non include il nome della funzione nel file DEF. La voce nel registro eventi indica il motivo dell'errore.

**Windows 2000/NT:** Non sono supportate più DLL di amministrazione.

 

 




