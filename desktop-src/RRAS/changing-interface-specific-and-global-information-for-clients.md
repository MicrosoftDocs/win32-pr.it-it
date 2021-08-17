---
title: Modifica Interface-Specific e informazioni globali per i client
description: Per modificare le informazioni sull'interfaccia per un client specifico, ad esempio NAT, usare prima il valore appropriato \ 0034; GetInfo \ 0034; funzione per recuperare le informazioni correnti.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcea02c6d70e7d7e2da53926854879f1ca5b76526a83185b786b0074b8098434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791754"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Modifica Interface-Specific e informazioni globali per i client

Per modificare le informazioni sull'interfaccia per un client specifico, ad esempio NAT, usare prima di tutto la funzione "GetInfo" appropriata per recuperare le informazioni correnti. Se il router è in esecuzione, usare [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Se il router non è in esecuzione, usare [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Questa chiamata recupera le informazioni per tutti i client in esecuzione sull'interfaccia specificata. Ad esempio, se OSPF e RIP sono in esecuzione su una particolare interfaccia, questa chiamata recupera le informazioni sull'interfaccia per entrambi. Usare la [**funzione MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) per individuare il blocco di informazioni corrispondente al client da modificare. Usare quindi la [**funzione MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) per eseguire le modifiche. Infine, usare [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) o [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) per apportare le modifiche al router in esecuzione o alla configurazione del router nel Registro di sistema.

Le informazioni globali sul client sono informazioni che non sono specifiche di alcuna particolare interfaccia in cui il client è in esecuzione. Usare una procedura simile per modificare le informazioni globali per un client specifico. Recuperare innanzitutto le informazioni globali per tutti i client [**usando MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) [**o MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). Usare quindi le funzioni MprInfo per modificare le informazioni. Usare infine le funzioni [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) o [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) per salvare nuovamente le informazioni modificate nel router in esecuzione o nel Registro di sistema.

Le chiamate alle funzioni di amministrazione precedenti passano attraverso Dynamic Interface Manager (DIM) e alla fine vengono convertite in chiamate dal gestore router ai client stessi. Tutti i client, indipendentemente dal fatto che siano protocolli di routing, devono essere conformi all'interfaccia descritta nella sezione [Interfaccia del protocollo router](about-routing-protocol-interface.md). Come parte di questa interfaccia, il protocollo di routing deve supportare le funzioni seguenti (tra le altre):

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Il gestore router chiama [**le funzioni GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) per ognuno dei client per raccogliere le informazioni restituite da una chiamata a [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Analogamente, quando il gestore router riceve informazioni aggiornate tramite la chiamata [**MprAdminInterfaceTransportSetInfo,**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) usa le [**funzioni SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) per aggiornare le informazioni sull'interfaccia per ogni client.

 

 




