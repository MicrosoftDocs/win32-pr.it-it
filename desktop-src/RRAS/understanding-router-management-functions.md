---
title: Informazioni sulle funzioni di gestione del router
description: Nelle sezioni seguenti vengono illustrati i diversi tipi di funzioni di gestione del router e le informazioni necessarie per utilizzarle in modo efficace.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b1891bc55b80a18a6d0dd928044da1e0e9709
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300270"
---
# <a name="understanding-router-management-functions"></a>Informazioni sulle funzioni di gestione del router

Nelle sezioni seguenti vengono illustrati i diversi tipi di funzioni di gestione del router e le informazioni necessarie per utilizzarle in modo efficace.

Tutte le funzioni di gestione del router richiedono privilegi di amministratore. Un utente nel gruppo Power User non dispone di privilegi sufficienti per utilizzare le funzioni di gestione del router.

## <a name="the-different-classes-of-router-management-functions"></a>Classi diverse di funzioni di gestione del router

Le funzioni di gestione del router possono essere divise nelle funzioni di amministrazione e nelle funzioni di configurazione. Le [funzioni di amministrazione](router-administration-functions.md) hanno un prefisso MprAdmin e le [funzioni di configurazione](router-configuration-functions.md) hanno il prefisso MprConfig. Nonostante la denominazione, entrambi i set di funzioni vengono utilizzati per la gestione del router. Le funzioni MprAdmin funzionano direttamente sul router in esecuzione. Le funzioni MprConfig hanno funzionalità simili, ma operano sulla configurazione del router archiviata nel registro di sistema. Entrambi i tipi di funzioni passano i [blocchi di informazioni](router-information-functions.md).

Le funzioni di gestione del router possono inoltre essere divise in base ai componenti del router gestiti, ovvero interfacce, gestori router o client di gestione router.

Le [funzioni di interfaccia del router](router-interface-functions.md) hanno un prefisso MprAdminInterface o MprConfigInterface. Usare queste funzioni per accedere alle interfacce. Le [funzioni di gestione router](router-manager-transport-functions.md) hanno un prefisso MprAdminTransport o MprConfigTransport. Utilizzare queste funzioni per accedere ai gestori di router. Infine, le [funzioni client di gestione router](router-manager-client-interfacetransport-functions.md) hanno un prefisso MprAdminInterfaceTransport o MprConfigInterfaceTransport. Usare queste funzioni per accedere ai client in esecuzione nel router.

Un subset di funzioni MprAdmin sono le [funzioni MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). Queste operazioni funzionano anche solo sulla Route in esecuzione. Tuttavia, queste funzioni non passano i blocchi di informazioni. Queste funzioni forniscono flessibilità aggiuntiva a progettazione protocolli, in particolare per il recupero di informazioni non di configurazione, ad esempio le statistiche.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Verificare che le modifiche vengano eseguite immediatamente e che siano permanenti

Uno sviluppatore può apportare modifiche alla configurazione del router direttamente usando le [funzioni di configurazione del router](router-configuration-functions.md). Tuttavia, le modifiche apportate alla configurazione diventano effettive solo dopo il riavvio del router, dal momento che questa è l'unica volta in cui DIM legge la configurazione dal registro di sistema.

Uno sviluppatore può apportare modifiche al router in esecuzione utilizzando le [funzioni di amministrazione del router](router-administration-functions.md). Tuttavia, queste modifiche non sono persistenti: poiché non sono state scritte nel registro di sistema, andranno perse se il router viene riavviato.

Per apportare modifiche immediate e permanenti, lo sviluppatore deve usare sia le funzioni di configurazione del router sia quelle di configurazione del router. Se il router non è in esecuzione, lo sviluppatore deve solo chiamare le funzioni di configurazione del router appropriate.

Per eseguire query sulle informazioni del router in esecuzione, utilizzare le funzioni di amministrazione del router. Se il router non è in esecuzione, le informazioni sulle query utilizzano le funzioni di configurazione del router.

Le funzioni [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) supportano la struttura di [**MPR \_ Interface \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) . Tuttavia, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) e [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) non lo sono. Per creare un'interfaccia di connessione a richiesta persistente dopo un riavvio, chiamare **MprAdminInterfaceCreate** con l' **interfaccia MPR \_ \_ 2**, quindi chiamare **MprConfigInterfaceCreate** con l'interfaccia [**MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) o [**MPR \_ Interface \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1). Analogamente, per apportare modifiche permanenti a un'interfaccia di connessione a richiesta, chiamare **MprAdminInterfaceSetInfo** con l' **\_ interfaccia MPR \_ 2**, quindi chiamare **MprConfigInterfaceSetInfo** con l'interfaccia **MPR \_ \_ 0** o **MPR \_ Interface \_ 1**.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Uso delle funzioni di amministrazione e configurazione del router in modalità remota

La maggior parte delle funzioni di amministrazione e configurazione del router può essere chiamata in un computer diverso da quello amministrato. Queste funzioni accettano come parametro, un handle per il servizio router o la configurazione da amministrare. Le funzioni di amministrazione utilizzano RPC (Remote Procedure Call) per comunicare con il servizio di routing specificato dall'handle. Le funzioni di configurazione scrivono e leggono dal registro di sistema del computer specificato dall'handle.

Per amministrare il servizio di routing in un computer remoto, chiamare prima [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) per verificare che il servizio sia in esecuzione. Chiamare quindi [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) per ottenere l'handle. Se il servizio router non è in esecuzione nel computer remoto, tutte le chiamate di amministrazione router (MprAdmin) hanno esito negativo.

Per apportare modifiche alla configurazione del router in un computer remoto, ottenere un handle chiamando la funzione [**MprConfigServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) .

 

 