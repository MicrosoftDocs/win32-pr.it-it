---
description: Anche se un'applicazione può usare il colore indipendentemente dalle funzionalità di colore del dispositivo, l'output risultante potrebbe non essere informativo e gradevole come output per cui il colore viene scelto con attenzione.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Approssimazioni dei colori e dithering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9733259aff787856ac9c6fed68f708c3b580c6200b65652424264eef3c73d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761968"
---
# <a name="color-approximations-and-dithering"></a>Approssimazioni dei colori e dithering

Anche se un'applicazione può usare il colore indipendentemente dalle funzionalità di colore del dispositivo, l'output risultante potrebbe non essere informativo e gradevole come output per cui il colore viene scelto con attenzione. Pochi, se presenti, dispositivi garantiscono una corrispondenza esatta per ogni valore di colore possibile; Pertanto, se un'applicazione richiede un colore che il dispositivo non può generare, il sistema approssima tale colore usando un colore che il dispositivo può generare. Ad esempio, se un'applicazione tenta di creare una penna rossa per una stampante in bianco e nero, riceverà una penna nera invece il sistema usa il nero come approssimazione per il rosso.

Un'applicazione può individuare se il sistema approssima un determinato colore usando la [**funzione GetNearestColor.**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) La funzione accetta un valore di colore e restituisce il valore del colore corrispondente più vicino che il dispositivo può generare. Il metodo utilizzato dal sistema per determinare questa approssimazione dipende dal driver di dispositivo e dalle relative funzionalità di colore. Nella maggior parte dei casi, l'intensità complessiva del colore approssimativo è più vicina a quella del colore richiesto.

Quando un'applicazione crea una penna o imposta il colore per il testo, il sistema approssima sempre un colore se non esiste alcuna corrispondenza esatta. Quando un'applicazione crea un pennello a tinta unita, il sistema può tentare di simulare il colore richiesto tramite dithering. *Il dithering* simula un colore alternando due o più colori in un motivo. Ad esempio, diverse sfumature di rosa possono essere simulate alternando combinazioni diverse di rosso e bianco. A seconda dei colori e del modello, il dithering può produrre simulazioni ragionevoli. È particolarmente utile per i dispositivi monocromatici, perché espande il numero di "colori" disponibili ben oltre il semplice bianco e nero.

Il metodo usato per creare colori con dithering dipende dal driver di dispositivo. La maggior parte dei driver di dispositivo usa un algoritmo di dithering standard, che genera un modello basato sui valori di intensità dei colori rosso, verde e blu richiesti. In generale, qualsiasi colore richiesto che non può essere generato dal dispositivo è soggetto a simulazione, ma un'applicazione non viene notificata quando il sistema simula un colore. Inoltre, un'applicazione non può modificare l'algoritmo di dithering del driver di dispositivo. Un'applicazione, tuttavia, può ignorare l'algoritmo creando e usando pennelli per modelli. In questo modo, l'applicazione crea i propri colori con dithering combinando i colori a tinta unita nella bitmap che usa per creare il pennello.

 

 



