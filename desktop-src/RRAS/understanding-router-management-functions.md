---
title: Informazioni sulle funzioni di gestione dei router
description: Le sezioni seguenti illustrano i diversi tipi di funzioni di gestione dei router e cosa è necessario sapere per usarle in modo efficace.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85aac5cc2ec0167527f07c04459ec0aed7dbc248bed727fb4a949765c2fdcc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025401"
---
# <a name="understanding-router-management-functions"></a>Informazioni sulle funzioni di gestione dei router

Le sezioni seguenti illustrano i diversi tipi di funzioni di gestione dei router e cosa è necessario sapere per usarle in modo efficace.

Tutte le funzioni di gestione del router richiedono privilegi di amministratore. Un utente del gruppo Power User non dispone di privilegi sufficienti per usare le funzioni di gestione del router.

## <a name="the-different-classes-of-router-management-functions"></a>Le diverse classi di funzioni di gestione router

Le funzioni di gestione del router possono essere suddivise in funzioni di amministrazione e funzioni di configurazione. Le [funzioni di amministrazione](router-administration-functions.md) hanno un prefisso MprAdmin e le funzioni di [configurazione](router-configuration-functions.md) hanno un prefisso MprConfig. Nonostante la denominazione, entrambi i set di funzioni vengono usati per la gestione dei router. Le funzioni MprAdmin operano direttamente sul router in esecuzione. Le funzioni MprConfig hanno funzionalità simili, ma operano sulla configurazione del router archiviata nel Registro di sistema. Entrambi i tipi di funzioni passano [blocchi di informazioni](router-information-functions.md).

Le funzioni di gestione dei router possono anche essere suddivise in base ai componenti del router che gestiscono: interfacce, gestori di router o client di gestione router.

Le [funzioni dell'interfaccia router](router-interface-functions.md) hanno un prefisso MprAdminInterface o MprConfigInterface. Usare queste funzioni per accedere alle interfacce. Le [funzioni di gestione router](router-manager-transport-functions.md) hanno un prefisso MprAdminTransport o MprConfigTransport. Usare queste funzioni per accedere ai gestori router. Infine, le funzioni [client di Gestione router](router-manager-client-interfacetransport-functions.md) hanno un prefisso MprAdminInterfaceTransport o MprConfigInterfaceTransport. Usare queste funzioni per accedere ai client in esecuzione nel router.

Un subset di funzioni MprAdmin sono [le funzioni MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). Questi operano anche solo sulla route in esecuzione. Tuttavia, queste funzioni non passano blocchi di informazioni. Queste funzioni offrono maggiore flessibilità alla finestra di progettazione del protocollo, in particolare per il recupero di informazioni non di configurazione, ad esempio le statistiche.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Verifica che le modifiche si verifichino immediatamente e siano persistenti

Uno sviluppatore può apportare modifiche alla configurazione del router direttamente usando le funzioni [di configurazione del router](router-configuration-functions.md). Tuttavia, le modifiche apportate alla configurazione non vengono applicate fino al riavvio del router, poiché è l'unica volta che DIM legge la configurazione dal Registro di sistema.

Uno sviluppatore può apportare modifiche al router in esecuzione usando le funzioni [di amministrazione del router](router-administration-functions.md). Queste modifiche, tuttavia, non sono persistenti: poiché non sono state scritte nel Registro di sistema, vengono perse se il router viene riavviato.

Per apportare modifiche immediate e persistenti, uno sviluppatore deve usare sia l'amministrazione del router che le funzioni di configurazione del router. Se il router non è in esecuzione, lo sviluppatore deve chiamare solo le funzioni di configurazione del router appropriate.

Per eseguire query sulle informazioni dal router in esecuzione, usare le funzioni di amministrazione del router. Se il router non è in esecuzione, eseguire query sulle informazioni usando le funzioni di configurazione del router.

Le [**funzioni MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) supportano la [**struttura MPR INTERFACE \_ \_ 2.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) Tuttavia, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) e [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) non lo fanno. Per creare un'interfaccia di connessione a richiesta persistente dopo un riavvio, chiamare **MprAdminInterfaceCreate** con **MPR \_ INTERFACE \_ 2,** quindi **chiamare MprConfigInterfaceCreate** con [**MPR INTERFACE \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) o [**MPR INTERFACE \_ \_ 1.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1) Analogamente, per apportare modifiche persistenti a un'interfaccia di connessione a richiesta, chiamare **MprAdminInterfaceSetInfo** con **MPR \_ INTERFACE \_ 2,** quindi **chiamare MprConfigInterfaceSetInfo** con **MPR INTERFACE \_ \_ 0** o **MPR INTERFACE \_ \_ 1.**

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Uso remoto delle funzioni di configurazione e amministrazione del router

La maggior parte delle funzioni di configurazione e amministrazione del router può essere chiamata in un computer diverso da quello amministrato. Queste funzioni accettano come parametro, un handle per il servizio router o la configurazione da amministrare. Le funzioni di amministrazione usano RPC (Remote Procedure Call) per comunicare con il servizio di routing specificato dall'handle. Le funzioni di configurazione scrivono e leggono dal Registro di sistema del computer specificato dall'handle.

Per amministrare il servizio di routing in un computer remoto, chiamare [**prima MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) per verificare che il servizio sia in esecuzione. Chiamare quindi [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) per ottenere l'handle. Se il servizio router non è in esecuzione nel computer remoto, tutte le chiamate di amministrazione del router (MprAdmin) hanno esito negativo.

Per apportare modifiche alla configurazione del router in un computer remoto, ottenere un handle chiamando la [**funzione MprConfigServerConnect.**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect)

 

 