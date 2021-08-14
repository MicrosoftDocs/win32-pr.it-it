---
title: Flag hop successivo
description: Flag hop successivo
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Prossima
- Flag hop successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dbad78f5f10d7a9d7bf42f694f7e2fb3109c03b92dccdb5f31697f5cf8988c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790394"
---
# <a name="next-hop-flags"></a>Flag hop successivo

## <a name="next-hop-state-flags"></a>Flag di stato hop successivo



| Costante                     | Valore | Descrizione                              |
|------------------------------|-------|------------------------------------------|
| RTM \_ NEXTHOP \_ STATE \_ CREATED | 0     | Indica che è stato creato l'hop successivo. |
| RTM \_ NEXTHOP \_ STATE \_ DELETED | 1     | Indica che l'hop successivo è stato eliminato. |



 

## <a name="next-hop-flags"></a>Flag hop successivo



| Costante                    | Valore  | Descrizione                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ NEXTHOP \_ FLAG \_ REMOTE | 0x0001 | Questo hop successivo punta a una destinazione remota non direttamente raggiungibile. Per ottenere il percorso completo, il client deve eseguire una ricerca ricorsiva. |
| FLAG \_ NEXTHOP RTM \_ \_ DOWN   | 0x0002 | Questo flag è riservato per un uso futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Hop successivo aggiunto



| Costante                  | Valore | Descrizione                 |
|---------------------------|-------|-----------------------------|
| RTM \_ NEXTHOP \_ CHANGE \_ NEW | 0x01  | È stato creato un nuovo hop successivo. |



 

 

 




