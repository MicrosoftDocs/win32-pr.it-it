---
title: Informazioni sugli errori estesi per l'utente
description: Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sull'errore esteso devono semplificare la ricerca del problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d2c7a67bb678472fbd3abbf90e0885590c795e2ffc46213a7acbb397da149c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021306"
---
# <a name="extended-error-information-for-the-user"></a>Informazioni sugli errori estesi per l'utente

Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sull'errore esteso devono semplificare la ricerca del problema. Il primo passaggio consiste nell'esaminare l'ultimo record di errore esteso e determinare in quale computer e quale processo ha avuto origine il problema. Questa è spesso la causa dell'errore \_ RPC \_ \* S. Trovare la posizione di rilevamento e determinare il significato dei parametri per questa posizione di rilevamento. In genere indicano un errore di una chiamata di funzione o di un controllo specifico. Da qui, determinare il motivo per cui la funzione o il controllo ha esito negativo ed eseguire un'azione correttiva.

I record precedenti all'ultimo record indicano il percorso in base al quale è arrivato l'errore e in genere fungono da controllo di autenticità anziché da aiutante nel processo di risoluzione dei problemi.

 

 




