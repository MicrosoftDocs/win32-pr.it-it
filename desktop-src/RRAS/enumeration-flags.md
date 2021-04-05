---
title: Flag di enumerazione
description: Flag di enumerazione
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumerazione
- Flag di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955479"
---
# <a name="enumeration-flags"></a>Flag di enumerazione



| Costante               | Valore      | Descrizione                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_inizio enum \_ RTM       | 0x00000000 | Enumerare route o destinazioni a partire da 0/0.                                                                                                         |
| \_enumerazione RTM \_ successiva        | 0x00000001 | Enumera le route o le destinazioni a partire dalla lunghezza dell'indirizzo/maschera specificata (ad esempio, 10/8). L'enumerazione continua fino alla fine della tabella di routing. |
| \_intervallo enum \_ RTM       | 0x00000002 | Enumera le route o le destinazioni nel sottoalbero specificato dalla lunghezza dell'indirizzo/maschera, ad esempio 10/8.                                            |
| \_ \_ tutte le \_ DestS enum di RTM  | 0x00000000 | Restituisce tutte le destinazioni.                                                                                                                                  |
| \_DestS dell'enumerazione RTM \_ \_  | 0x01000000 | Restituire solo le destinazioni di proprietà del client.                                                                                                      |
| \_ \_ tutte le route di enum RTM \_ | 0x00000000 | Restituisce tutte le route.                                                                                                                                        |
| \_ \_ route personalizzate enum \_ RTM | 0x00010000 | Restituisce solo le route di proprietà del client.                                                                                                            |



 

 

 




