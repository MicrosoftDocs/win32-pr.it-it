---
title: Eliminazione di un client da un'interfaccia
description: Per eliminare un client, ad esempio un protocollo di routing, da una determinata interfaccia, usare MprAdminInterfaceTransportGetInfo o MprConfigInterfaceTransportGetInfo per recuperare tutte le informazioni client per l'interfaccia.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e5b93e062f5971f6e43ad1d7c08f7a0c2ef3bff72e66849815a053b342b13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127891"
---
# <a name="deleting-a-client-from-an-interface"></a>Eliminazione di un client da un'interfaccia

Per eliminare un client, ad esempio un protocollo di routing, da una determinata interfaccia, usare [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) o [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) per recuperare tutte le informazioni client per l'interfaccia. Usare [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) per rimuovere il blocco di informazioni per il client da eliminare. Usare quindi [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) per aggiungere un blocco di lunghezza zero per l'eliminazione del client. Usare infine [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) per salvare nuovamente le informazioni nel router in esecuzione o nel Registro di sistema.

Se il gestore router riceve un blocco di informazioni sull'interfaccia di lunghezza zero per un client, sa di eliminare tale client dall'interfaccia. Il gestore router elimina il client chiamando l'implementazione del client [**di DeleteInterface.**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface) Si noti l'importante distinzione tra il passaggio di un'intestazione di informazioni che non contiene un blocco di informazioni per un client e il passaggio di un'intestazione di informazioni che contiene un blocco di informazioni di lunghezza zero per il client. Nel primo caso, il gestore del router non prende alcuna azione rispetto al client. Nel secondo caso, gestione router elimina il client dall'interfaccia.

 

 




