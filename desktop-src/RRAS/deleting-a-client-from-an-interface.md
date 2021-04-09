---
title: Eliminazione di un client da un'interfaccia
description: Per eliminare un client, ad esempio un protocollo di routing, da un'interfaccia particolare, utilizzare MprAdminInterfaceTransportGetInfo o MprConfigInterfaceTransportGetInfo per recuperare tutte le informazioni sul client per l'interfaccia.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955631"
---
# <a name="deleting-a-client-from-an-interface"></a>Eliminazione di un client da un'interfaccia

Per eliminare un client, ad esempio un protocollo di routing, da un'interfaccia particolare, utilizzare [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) o [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) per recuperare tutte le informazioni sul client per l'interfaccia. Usare [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) per rimuovere il blocco di informazioni per il client da eliminare. Usare quindi [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) per aggiungere un blocco di lunghezza zero per il client da eliminare. Infine, utilizzare [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) per salvare di nuovo le informazioni nel router o nel registro di sistema in esecuzione.

Se il gestore router riceve un blocco di informazioni sull'interfaccia di lunghezza zero per un client, è in grado di eliminare il client dall'interfaccia. Gestione router Elimina il client chiamando l'implementazione del client di [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Si noti l'importante differenza tra il passaggio di un'intestazione di informazioni che non contiene un blocco di informazioni per un client e il passaggio di un'intestazione di informazioni contenente un blocco di informazioni di lunghezza zero per il client. Nel primo caso, gestione router non esegue alcuna azione rispetto al client. Nel secondo caso, gestione router Elimina il client dall'interfaccia.

 

 




