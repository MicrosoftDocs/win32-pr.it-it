---
title: Flag di query tabella di routing
description: Utilizzare queste costanti per le query di tabella router.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Flag di query tabella di routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857026"
---
# <a name="routing-table-query-flags"></a>Flag di query tabella di routing

Utilizzare queste costanti per le query di tabella router.



| Costante              | Valore      | Descrizione                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| \_Nessuna corrispondenza \_ RTM      | 0x00000000 | Corrisponde a nessuno dei criteri. vengono restituite tutte le route per la destinazione. |
| \_proprietario corrispondenza \_ RTM     | 0x00000001 | Corrisponde alle route con lo stesso proprietario.                                            |
| \_corrispondenza RTM corrispondente \_ | 0x00000002 | Corrisponde alle route con lo stesso adiacente.                                     |
| \_corrispondenze \_ RTM      | 0x00000004 | Corrisponde alle route con la stessa preferenza.                              |
| \_NEXTHOP corrispondenza \_ RTM   | 0x00000008 | Corrisponde alle route con lo stesso hop successivo.                                |
| \_interfaccia di corrispondenza RTM \_ | 0x00000010 | Corrisponde alle route che si trovano nella stessa interfaccia.                             |
| \_corrispondenza RTM \_ completa      | 0x0000FFFF | Corrisponde alle route con tutti i criteri.                                          |
| \_protocollo migliore \_ RTM   | 0          | Restituisce una route indipendentemente dal protocollo di cui è proprietario.                      |
| \_il \_ protocollo RTM   | ~0         | Restituisce la route migliore per il protocollo chiamante.                           |



 

 

 




