---
title: Flag di query della tabella di routing
description: Usare queste costanti per le query della tabella router.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Flag di query della tabella di routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 307dd91e9b3d248e5b2b69869ee1e7d14ae17834f7fe57d9e136da16ba3f6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787449"
---
# <a name="routing-table-query-flags"></a>Flag di query della tabella di routing

Usare queste costanti per le query della tabella router.



| Costante              | Valore      | Descrizione                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM \_ MATCH \_ NONE      | 0x00000000 | Non corrisponde a nessuno dei criteri. Vengono restituite tutte le route per la destinazione. |
| RTM \_ MATCH \_ OWNER     | 0x00000001 | Corrisponde alle route con lo stesso proprietario.                                            |
| RTM \_ MATCH MATCH PIÙ \_ ADATTA | 0x00000002 | Trova la corrispondenza delle route con lo stesso router adiacente.                                     |
| RTM \_ MATCH \_ PREF      | 0x00000004 | Corrisponde alle route che hanno la stessa preferenza.                              |
| RTM \_ MATCH \_ NEXTHOP   | 0x00000008 | Corrisponde alle route con lo stesso hop successivo.                                |
| INTERFACCIA DI CORRISPONDENZA RTM \_ \_ | 0x00000010 | Corrisponde alle route che si trova nella stessa interfaccia.                             |
| RTM \_ MATCH \_ FULL      | 0x0000FFFF | Trova la corrispondenza delle route con tutti i criteri.                                          |
| RTM \_ BEST \_ PROTOCOL   | 0          | Restituisce una route indipendentemente dal protocollo proprietario.                      |
| RTM \_ THIS \_ PROTOCOL   | ~0         | Restituisce la route migliore per il protocollo chiamante.                           |



 

 

 




