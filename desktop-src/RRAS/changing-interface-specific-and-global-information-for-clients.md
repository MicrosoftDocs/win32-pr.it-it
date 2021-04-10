---
title: Modifica Interface-Specific e informazioni globali per i client
description: Per modificare le informazioni sull'interfaccia per un client specifico, ad esempio NAT, usare prima il valore appropriato \ 0034; GetInfo \ 0034; funzione per recuperare le informazioni correnti.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c8f2ef3c37d75db1cc7686a67108530b16b28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955470"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Modifica Interface-Specific e informazioni globali per i client

Per modificare le informazioni sull'interfaccia per un client specifico, ad esempio NAT, usare prima la funzione "GetInfo" appropriata per recuperare le informazioni correnti. Se il router è in esecuzione, usare [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Se il router non è in esecuzione, usare [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Questa chiamata recupera le informazioni relative a tutti i client in esecuzione nell'interfaccia specificata. Se, ad esempio, OSPF e RIP sono in esecuzione in un'interfaccia particolare, questa chiamata recupera le informazioni sull'interfaccia per entrambi. Utilizzare la funzione [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) per individuare il blocco di informazioni che corrisponde al client che si desidera modificare. Usare quindi la funzione [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) per eseguire le modifiche. Infine, utilizzare [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) per apportare le modifiche alla configurazione del router o del router in esecuzione nel registro di sistema.

Le informazioni sul client globali sono informazioni non specifiche di una particolare interfaccia in cui il client è in esecuzione. Usare una procedura simile per modificare le informazioni globali per un client specifico. Recuperare innanzitutto le informazioni globali per tutti i client che usano [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) o [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). Usare quindi le funzioni MprInfo per modificare le informazioni. Infine, usare le funzioni [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) o [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) per salvare di nuovo le informazioni modificate nel router o nel registro di sistema in esecuzione.

Le chiamate alle funzioni di amministrazione precedenti passano attraverso gestione interfaccia dinamica (DIM) e, infine, vengono convertite in chiamate da Gestione router ai client stessi. Tutti i client, indipendentemente dal fatto che siano protocolli di routing, devono essere conformi all'interfaccia descritta nella sezione [interfaccia del protocollo router](about-routing-protocol-interface.md). Come parte di questa interfaccia, il protocollo di routing deve supportare le seguenti funzioni (tra le altre):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Gestione router chiama le funzioni [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) per ogni client per raccogliere le informazioni restituite da una chiamata a [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Analogamente, quando Gestione router riceve informazioni aggiornate tramite la chiamata a [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) , USA le funzioni [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) per aggiornare le informazioni sull'interfaccia per ogni client.

 

 




