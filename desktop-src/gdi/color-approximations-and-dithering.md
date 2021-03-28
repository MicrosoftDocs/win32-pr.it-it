---
description: Sebbene un'applicazione possa usare il colore senza considerare le funzionalità di colore del dispositivo, l'output risultante potrebbe non essere informativo e piacevole come output per il quale viene scelto attentamente il colore.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Approssimazioni di colori e dithering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130823"
---
# <a name="color-approximations-and-dithering"></a>Approssimazioni di colori e dithering

Sebbene un'applicazione possa usare il colore senza considerare le funzionalità di colore del dispositivo, l'output risultante potrebbe non essere informativo e piacevole come output per il quale viene scelto attentamente il colore. Alcuni dispositivi garantiscono una corrispondenza esatta per ogni possibile valore di colore. di conseguenza, se un'applicazione richiede un colore che il dispositivo non può generare, il sistema si avvicina al colore usando un colore che il dispositivo può generare. Se, ad esempio, un'applicazione tenta di creare una penna rossa per una stampante nera e bianca, riceverà una penna nera, ma il sistema utilizzerà il nero come approssimazione per il rosso.

Un'applicazione è in grado di rilevare se il sistema apparirà approssimativamente un determinato colore utilizzando la funzione [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) . La funzione accetta un valore di colore e restituisce il valore del colore del colore corrispondente più vicino che il dispositivo può generare. Il metodo utilizzato dal sistema per determinare l'approssimazione dipende dal driver di dispositivo e dalle relative funzionalità di colore. Nella maggior parte dei casi, l'intensità complessiva del colore approssimativo è più vicina a quella del colore richiesto.

Quando un'applicazione crea una penna o imposta il colore per il testo, il sistema è sempre approssimato a un colore se non esiste alcuna corrispondenza esatta. Quando un'applicazione crea un pennello a tinta unita, il sistema può tentare di simulare il colore richiesto eseguendo la dithering. La *dithering* simula un colore alternando due o più colori in un modello. Ad esempio, è possibile simulare diverse sfumature di rosa alternando diverse combinazioni di rosso e bianco. A seconda dei colori e del modello, la dithering può produrre simulazioni ragionevoli. È particolarmente utile per i dispositivi monocromi, perché espande il numero di "colori" disponibili oltre il semplice bianco e nero.

Il metodo utilizzato per creare colori con divariato dipende dal driver di dispositivo. La maggior parte dei driver di dispositivo utilizza un algoritmo di rethering standard, che genera un modello basato sui valori di intensità dei colori rosso, verde e blu richiesti. In generale, qualsiasi colore richiesto che non può essere generato dal dispositivo è soggetto alla simulazione, ma un'applicazione non viene notificata quando il sistema simula un colore. Inoltre, un'applicazione non può modificare o modificare l'algoritmo di rethering del driver di dispositivo. Un'applicazione, tuttavia, può ignorare l'algoritmo creando e usando pennelli modello. In questo modo, l'applicazione crea i propri colori digitati combinando colori a tinta unita nella bitmap utilizzata per creare il pennello.

 

 



