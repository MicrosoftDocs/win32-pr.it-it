---
description: Per recuperare gli elementi di un percorso, chiamare la funzione PdhParseCounterPath. La funzione analizza gli elementi di un percorso del contatore e li restituisce in una struttura PDH \_ COUNTER \_ PATH \_ ELEMENTS.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Recupero di elementi del percorso del contatore da un percorso del contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c8df5c7176684fc439f632a22f829afe5afae202f7595579350450ee30c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143974"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Recupero di elementi del percorso del contatore da un percorso del contatore

Per recuperare gli elementi di un percorso, chiamare la [**funzione PdhParseCounterPath.**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) La funzione analizza gli elementi di un percorso del contatore e li restituisce in una [**struttura PDH \_ COUNTER PATH \_ \_ ELEMENTS.**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)

Se si dispone di un nome di istanza complesso ( che contiene un'istanza padre e un indice di istanza), è possibile chiamare la funzione [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) per estrarre il nome dell'istanza, l'indice dell'istanza e il nome padre.

 

 



