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
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="292cd-104">Recupero di elementi del percorso del contatore da un percorso del contatore</span><span class="sxs-lookup"><span data-stu-id="292cd-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="292cd-105">Per recuperare gli elementi di un percorso, chiamare la funzione [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) .</span><span class="sxs-lookup"><span data-stu-id="292cd-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="292cd-106">La funzione analizza gli elementi di un percorso del contatore e li restituisce in una [**struttura \_ \_ \_ degli elementi del percorso del contatore PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .</span><span class="sxs-lookup"><span data-stu-id="292cd-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="292cd-107">Se si dispone di un nome di istanza complesso, ovvero uno contenente un'istanza padre e un indice dell'istanza, è possibile chiamare la funzione [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) per estrarre il nome dell'istanza, l'indice dell'istanza e il nome padre.</span><span class="sxs-lookup"><span data-stu-id="292cd-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



