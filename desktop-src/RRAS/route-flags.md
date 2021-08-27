---
title: Flag di route
description: Flag di route
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Route
- Flag di route
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1476742f1204eb14dd2bb96b289825d179a58e5bec01ff0aee18bcfbdb13a9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081241"
---
# <a name="route-flags"></a>Flag di route

## <a name="state-of-the-route-constants"></a>Stato delle costanti di route



| Costante                    | Valore | Descrizione             |
|-----------------------------|-------|-------------------------|
| STATO DELLA ROUTE RTM \_ \_ \_ CREATO  | 0     | La route è stata creata. |
| ELIMINAZIONE DELLO STATO DELLA ROUTE RTM \_ \_ \_ | 1     | È in corso l'eliminazione della route. |
| STATO ROUTE RTM \_ \_ \_ ELIMINATO  | 2     | La route è stata eliminata. |



 

## <a name="route-update-flags"></a>Flag di aggiornamento route



| Costante                  | Valore      | Descrizione                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODIFICA DELLA ROUTE RTM \_ \_ PER \_ PRIMA | 0x01       | Indica che il gestore delle tabelle di routing non deve controllare il membro **Di** vicinato della struttura [**RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) per determinare quando due route sono uguali. |
| MODIFICA DELLA ROUTE RTM \_ \_ \_ NUOVA   | 0x02       | Restituito dal gestore tabelle di routing per indicare che è stata creata una nuova route.                                                                                                                 |
| MODIFICA MIGLIORE DELLA ROUTE RTM \_ \_ \_  | 0x00010000 | Restituito dal gestore tabelle di routing per indicare che la route aggiunta o aggiornata è la route migliore o che, a causa della modifica, una nuova route è diventata la route migliore.           |



 

## <a name="unicast-flags"></a>Flag unicast



| Costante                  | Valore  | Descrizione                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| FLAG DI ROUTE RTM \_ \_ \_ LOCALI  | 0x0010 | Indica che una destinazione si trova in una rete direttamente raggiungibile.            |
| FLAG DI ROUTE RTM \_ \_ \_ REMOTI | 0x0020 | Indica che la destinazione non si trova in una rete direttamente raggiungibile. |
| FLAG DI ROUTE RTM \_ \_ \_ | 0x0040 | Indica che la destinazione è uno degli indirizzi del router.            |



 

## <a name="broadcast-and-multicast-flags"></a>Flag broadcast e multicast



| Costante                           | Valore  | Descrizione                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCAST \_ DEI FLAG DI ROUTE RTM \_ \_           | 0x0100 | Indica che questa route è una route a un indirizzo multicast.                                                                                                                                               |
| MCAST \_ LOCALE DEI FLAG \_ \_ DI ROUTE \_ RTM    | 0x0200 | Indica che questa route è una route a un indirizzo multicast locale.                                                                                                                                         |
| FLAG DI ROUTE RTM \_ \_ LIMITATI \_ \_ BC     | 0x0400 | Indica che questa route è un indirizzo broadcast limitato. I pacchetti a questa destinazione non devono essere inoltrati.                                                                                             |
| FLAG DI ROUTE RTM \_ \_ ZERO \_ \_ NETBC    | 0x1000 | Indica che la destinazione corrisponde all'indirizzo broadcast all-zeros di un'interfaccia. Se l'inoltro broadcast è abilitato, i pacchetti devono essere ricevuti e inviati nuovamente a tutte le interfacce appropriate.               |
| FLAG DI ROUTE RTM \_ \_ \_ ZEROS \_ SUBNETBC | 0x2000 | Indica che la destinazione corrisponde all'indirizzo di trasmissione della subnet all-zeros di un'interfaccia. Se l'inoltro di broadcast della subnet è abilitato, i pacchetti devono essere ricevuti e inviati nuovamente a tutte le interfacce appropriate. |
| FLAG DI ROUTE RTM \_ \_ QUELLI \_ \_ NETBC     | 0x4000 | Indica che la destinazione corrisponde all'indirizzo di trasmissione tutti i tipi di interfaccia. Se l'inoltro broadcast è abilitato, i pacchetti devono essere ricevuti e inviati nuovamente a tutte le interfacce appropriate.                |
| FLAG DI ROUTE RTM \_ \_ ONES \_ \_ SUBNETBC  | 0x8000 | Indica che la destinazione corrisponde all'indirizzo di trasmissione tutte le subnet di un'interfaccia. Se l'inoltro di broadcast della subnet è abilitato, i pacchetti devono essere ricevuti e inviati nuovamente a tutte le interfacce appropriate.  |



 

## <a name="grouping-of-flags"></a>Raggruppamento di flag



| Group                            | Membri                                                                                                                                                                  | Descrizione                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| INOLTRO DI \_ FLAG DI ROUTE \_ \_ RTM    | FLAG DI ROUTE RTM \_ \_ \_ MARTIAN, FLAG DI ROUTE RTM \_ \_ \_ BLACKHOLE, FLAG DI ROUTE RTM \_ \_ \_ DISCARD, FLAG DI ROUTE RTM \_ \_ \_ INATTIVI                                                        | Specifica i flag di inoltro.                          |
| FLAG DI ROUTE RTM \_ \_ QUALSIASI \_ \_ UNICAST  | FLAG DI ROUTE RTM \_ \_ \_ LOCALI, FLAG DI ROUTE RTM \_ \_ \_ REMOTI, FLAG DI ROUTE RTM \_ \_ \_                                                                                           | Specifica tutti i flag unicast.                             |
| FLAG DI ROUTE RTM \_ \_ PER QUALSIASI \_ \_ MCAST    | MCAST \_ FLAG DI ROUTE RTM, FLAG DI ROUTE \_ \_ RTM \_ \_ \_ \_ MCAST LOCALE                                                                                                                | Specifica tutti i flag unicast.                             |
| BCAST \_ DELLA SUBNET DEI FLAG DI ROUTE \_ \_ \_ RTM | RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC                                                                                                  | Specifica tutti i flag di trasmissione della subnet.                    |
| FLAG DI ROUTE RTM \_ \_ NET \_ \_ BCAST    | FLAG DI ROUTE RTM \_ \_ QUELLI \_ \_ NETBC, FLAG DI ROUTE RTM \_ ZERO \_ \_ \_ NETBC                                                                                                          | Specifica tutti i flag broadcast a livello di rete.                  |
| FLAG DI ROUTE RTM \_ \_ QUALSIASI \_ \_ BCAST    | RTM \_ ROUTE \_ FLAGS \_ LIMITED \_ BC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ONES \_ SUBNET \_ BC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ NETBC, RTM \_ ROUTE \_ FLAGS \_ ZEROS \_ SUBNETBC | Specifica uno dei flag di trasmissione a livello di subnet o di rete. |



 

 

 




