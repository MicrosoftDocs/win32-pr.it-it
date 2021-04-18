---
description: Per recuperare gli elementi di un percorso, chiamare la funzione PdhParseCounterPath. La funzione analizza gli elementi di un percorso del contatore e li restituisce in una \_ \_ struttura degli elementi del percorso del contatore PDH \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Recupero di elementi del percorso del contatore da un percorso del contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312156"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Recupero di elementi del percorso del contatore da un percorso del contatore

Per recuperare gli elementi di un percorso, chiamare la funzione [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) . La funzione analizza gli elementi di un percorso del contatore e li restituisce in una [**struttura \_ \_ \_ degli elementi del percorso del contatore PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .

Se si dispone di un nome di istanza complesso, ovvero uno contenente un'istanza padre e un indice dell'istanza, è possibile chiamare la funzione [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) per estrarre il nome dell'istanza, l'indice dell'istanza e il nome padre.

 

 



