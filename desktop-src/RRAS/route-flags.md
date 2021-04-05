---
title: Flag di route
description: Flag di route
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Route
- Flag di route
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1711ef4ed621d55cc00302cca181676a3892c030
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955201"
---
# <a name="route-flags"></a>Flag di route

## <a name="state-of-the-route-constants"></a>Stato delle costanti di route



| Costante                    | Valore | Descrizione             |
|-----------------------------|-------|-------------------------|
| \_stato route \_ RTM \_ creato  | 0     | Route creata. |
| \_ \_ eliminazione dello stato della route RTM \_ | 1     | È in corso l'eliminazione della route. |
| \_stato route \_ RTM \_ eliminato  | 2     | Route eliminata. |



 

## <a name="route-update-flags"></a>Flag di aggiornamento Route



| Costante                  | Valore      | Descrizione                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ modifica prima route \_ RTM | 0x01       | Indica che il servizio di gestione delle tabelle di routing non deve verificare il membro **vicino** della struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) quando si determina quando due route sono uguali. |
| \_ \_ modifica nuova route \_ RTM   | 0x02       | Restituito da Gestione tabelle di routing per indicare che è stata creata una nuova route.                                                                                                                 |
| \_modifica della route RTM \_ \_ migliore  | 0x00010000 | Restituito da Gestione tabelle di routing per indicare che la route aggiunta o aggiornata è stata il percorso migliore o che, a causa della modifica, una nuova route è diventata la strada migliore.           |



 

## <a name="unicast-flags"></a>Flag unicast



| Costante                  | Valore  | Descrizione                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| \_flag route \_ RTM \_ locale  | 0x0010 | Indica che la destinazione si trova in una rete raggiungibile direttamente.            |
| \_flag route \_ RTM \_ remoto | 0x0020 | Indica che la destinazione non si trova in una rete raggiungibile direttamente. |
| \_flag route \_ RTM \_ | 0x0040 | Indica che la destinazione è uno degli indirizzi del router.            |



 

## <a name="broadcast-and-multicast-flags"></a>Flag broadcast e multicast



| Costante                           | Valore  | Descrizione                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_flag di route RTM \_ \_ mcast           | 0x0100 | Indica che questa route è una route per un indirizzo multicast.                                                                                                                                               |
| \_ \_ \_ mcast locali flag di route RTM \_    | 0x0200 | Indica che questa route è una route per un indirizzo multicast locale.                                                                                                                                         |
| \_flag route \_ RTM \_ Limited \_ BC     | 0x0400 | Indica che questa route è un indirizzo di broadcast limitato. I pacchetti a questa destinazione non devono essere inoltrati.                                                                                             |
| \_flag route \_ RTM \_ zeri \_ NETBC    | 0x1000 | Indica che la destinazione corrisponde all'indirizzo di trasmissione all-zero di un'interfaccia. Se l'invio broadcast è abilitato, i pacchetti devono essere ricevuti e inviati a tutte le interfacce appropriate.               |
| \_flag route \_ RTM \_ zeri \_ SUBNETBC | 0x2000 | Indica che la destinazione corrisponde all'indirizzo di trasmissione della subnet all-zero di un'interfaccia. Se l'invio della trasmissione della subnet è abilitato, i pacchetti devono essere ricevuti e inviati a tutte le interfacce appropriate. |
| \_flag di route RTM \_ \_ \_ NETBC     | 0x4000 | Indica che la destinazione corrisponde a tutti gli indirizzi di trasmissione di un'interfaccia. Se l'invio broadcast è abilitato, i pacchetti devono essere ricevuti e inviati a tutte le interfacce appropriate.                |
| \_flag di route RTM \_ \_ \_ SUBNETBC  | 0x8000 | Indica che la destinazione corrisponde a un indirizzo di broadcast di tutte le subnet di un'interfaccia. Se l'invio della trasmissione della subnet è abilitato, i pacchetti devono essere ricevuti e inviati a tutte le interfacce appropriate.  |



 

## <a name="grouping-of-flags"></a>Raggruppamento di flag



| Group                            | Membri                                                                                                                                                                  | Descrizione                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| \_ \_ inoltro flag di route RTM \_    | i flag di \_ route RTM \_ \_ Martian, RTM Route Flags \_ \_ \_ Blackhole, RTM \_ route \_ flags \_ scarto, RTM Route Flags \_ \_ \_ inattivo                                                        | Specifica tutti i flag di invio.                          |
| \_tutti i flag di route RTM sono \_ \_ \_ unicast  | i \_ flag \_ di route RTM \_ local, RTM \_ route \_ flags \_ remote, RTM \_ route \_ flags \_ Myself                                                                                           | Specifica i flag unicast.                             |
| la \_ route RTM \_ contrassegna \_ qualsiasi \_ mcast    | i \_ \_ flag di route RTM \_ mcast, i \_ flag di route RTM \_ \_ Local \_ mcast                                                                                                                | Specifica i flag unicast.                             |
| \_ \_ \_ gettati subnet flag route \_ RTM | \_flag di route RTM quelli della \_ \_ \_ subnet \_ BC, i \_ flag di route RTM \_ \_ azzerano \_ SUBNETBC                                                                                                  | Specifica i flag di broadcast della subnet.                    |
| \_flag di route RTM \_ \_ net \_ gettati    | i \_ \_ flag di route RTM \_ quelli \_ NETBC, RTM \_ route \_ flags \_ zero \_ NETBC                                                                                                          | Specifica i flag di trasmissione a livello di rete.                  |
| la \_ route RTM \_ contrassegna \_ qualsiasi \_ gettati    | i \_ \_ flag di route RTM \_ Limited \_ BC, i flag di \_ route RTM \_ \_ quelli \_ NETBC, i \_ flag di route RTM quelli della \_ \_ \_ subnet \_ BC, i flag di \_ route RTM \_ \_ zero \_ NETBC, i \_ flag di route RTM \_ \_ zero \_ SUBNETBC | Specifica uno dei flag di trasmissione della subnet o della rete a livello di rete. |



 

 

 




