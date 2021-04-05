---
title: Informazioni estese sull'errore per l'utente
description: Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sugli errori estesi devono facilitare l'individuazione del problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856302"
---
# <a name="extended-error-information-for-the-user"></a>Informazioni estese sull'errore per l'utente

Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sugli errori estesi devono facilitare l'individuazione del problema. Il primo passaggio consiste nel rivedere l'ultimo record degli errori esteso e determinare in quale computer e in quale processo ha avuto origine il problema. Si tratta spesso della cause dell'errore della \_ RPC \_ \* . Trovare il percorso di rilevamento e determinare quali sono i parametri per la posizione di rilevamento. In genere indicano un errore di una chiamata di funzione o di un particolare controllo. Da qui, determinare il motivo per cui la funzione o il controllo ha esito negativo e intraprendere un'azione correttiva.

I record prima dell'ultimo record indicano il percorso in base al quale è arrivato l'errore e in genere vengono usati come controllo di integrità anziché come un assistente nel processo di risoluzione dei problemi.

 

 




