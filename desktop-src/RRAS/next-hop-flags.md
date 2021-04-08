---
title: Flag di hop successivo
description: Flag di hop successivo
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Prossima
- Flag di hop successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045200"
---
# <a name="next-hop-flags"></a>Flag di hop successivo

## <a name="next-hop-state-flags"></a>Flag di stato hop successivo



| Costante                     | Valore | Descrizione                              |
|------------------------------|-------|------------------------------------------|
| \_stato NEXTHOP \_ RTM \_ creato | 0     | Indica che è stato creato l'hop successivo. |
| \_stato NEXTHOP \_ RTM \_ eliminato | 1     | Indica che l'hop successivo è stato eliminato. |



 

## <a name="next-hop-flags"></a>Flag di hop successivo



| Costante                    | Valore  | Descrizione                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_flag NEXTHOP RTM in \_ \_ remoto | 0x0001 | L'hop successivo punta a una destinazione remota non direttamente raggiungibile. Per ottenere il percorso completo, il client deve eseguire una ricerca ricorsiva. |
| \_flag NEXTHOP \_ RTM \_ inattivo   | 0x0002 | Questo flag è riservato per un utilizzo futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Hop successivo aggiunto



| Costante                  | Valore | Descrizione                 |
|---------------------------|-------|-----------------------------|
| \_ \_ nuova modifica di NEXTHOP RTM \_ | 0x01  | È stato creato un nuovo hop successivo. |



 

 

 




