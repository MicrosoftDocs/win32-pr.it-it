---
title: Problemi di autenticazione per ADSI con ASP
description: A seconda della configurazione della rete Intranet, è possibile che si verifichino problemi di autenticazione quando il codice ADSI viene eseguito da una pagina ASP.
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI, pagine ASP, problemi di autenticazione
- ADSI, autenticazione, problemi ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730202"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>Problemi di autenticazione per ADSI con ASP

A seconda della configurazione della rete Intranet, è possibile che si verifichino problemi di autenticazione quando il codice ADSI viene eseguito da una pagina ASP.

L'autenticazione per l'accesso al controller di dominio può essere assegnata utilizzando la delega. La delega consente a un servizio di agire come l'utente, in modo che possa accedere a una risorsa di rete utilizzando le credenziali dell'utente. Se la Intranet segue questa configurazione, è necessario configurare IIS per l'uso della delega. Impostare il meccanismo di autenticazione IIS come anonimo o NTLM. Se si sceglie Anonimo, verrà eseguito il mapping del contesto di sicurezza all' \_ account del computer IUSR. Se si seleziona NTLM, il contesto di sicurezza cambierà, a seconda dell'utente che accede al sito Web. Per ulteriori informazioni e istruzioni per la configurazione del server IIS per la delega, vedere la pagina relativa al [Resource Kit di Windows 2000](https://support.microsoft.com/kb/927229).

Se si usa un server IIS che usa la richiesta di verifica/risposta NT o un client browser che non supporta Kerberos, l'autenticazione a doppio hop non è supportata. L'autenticazione a doppio hop indica che le credenziali utente vengono passate dal client browser al server IIS e quindi il server IIS passa le credenziali al server back-end. In questa situazione, è possibile utilizzare una delle soluzioni seguenti per consentire l'accesso alla directory dalla pagina ASP:

-   Usare [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) per passare le credenziali a Active Directory. La pagina Web autentica l'utente connesso sul server IIS. Quando l'utente è stato autenticato, la pagina Web può usare OpenDSObject o ADsOpenObject per passare un nome utente e una password al servizio directory per ottenere l'autenticazione al server back-end. La pagina Web può quindi accedere ai dati dalla directory.
-   Aggiungere il codice a un oggetto COM e inserire questo oggetto in un' [applicazione com+](../cossdk/com--application-overview.md) , denominata in precedenza pacchetto MTS. L'applicazione COM+ può quindi essere eseguita come [account utente di dominio](/windows/desktop/AD/domain-user-accounts).
-   Usare più pagine ASP, in cui una pagina autentica il client e un'altra pagina passa le credenziali alla directory usando l'autenticazione anonima per un account utente di dominio.

Questi metodi implicano l'autenticazione del client Web e la modifica delle credenziali quando si contatta la directory perché non è possibile eseguire l'autenticazione a doppio hop con le stesse credenziali.

 

 