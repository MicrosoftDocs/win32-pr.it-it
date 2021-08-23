---
title: Device-Dependent colori
description: La maggior parte degli spazi colori dipende dal dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Sistema colori (WCS), spazi colori dipendenti dal dispositivo
- WCS (Windows Color System), spazi colori dipendenti dal dispositivo
- gestione dei colori delle immagini, spazi colori dipendenti dal dispositivo
- gestione dei colori, spazi colori dipendenti dal dispositivo
- colori, spazi colori dipendenti dal dispositivo
- spazi colori, dipendente dal dispositivo
- spazi colori dipendenti dal dispositivo
- punto bianco
- Coloranti
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe10ad9d48e750f9869b113a45f1235d2aa692532702ea4443ec3629d32276ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593621"
---
# <a name="device-dependent-color-spaces"></a>Device-Dependent colori

La maggior [parte degli spazi colori](c.md) dipende dal dispositivo. Anche se un particolare dispositivo, ad esempio una stampante, può usare lo spazio colori CMYK, i colori di cui esegue il rendering per valori CMYK specifici sono spesso leggermente diversi da tutti gli altri tipi di stampanti. È proprio per questo motivo che il sistema di gestione dei colori WCS 1.0 è così utile.

Tutti gli spazi colori hanno *un punto* bianco, definito come bianco più bianco che può essere prodotto in tale spazio colore. Poiché i dispositivi possono differire l'uno dall'altro, anche i punti vuoti possono essere diversi. Tutti i colori che un dispositivo può produrre sono relativi al punto bianco. Pertanto, un sistema di gestione dei colori deve essere in grado di eseguire il mapping del punto bianco di uno spazio colore in un altro e mantenere le posizioni relative di tutti i colori. Deve anche essere in grado di eseguire il mapping di un colore in uno spazio colori alla corrispondenza più vicina in un altro spazio colore indipendentemente dalle differenze nei punti bianchi. WCS 1.0 è in grado di eseguire entrambe queste attività.

Lo spazio colore RGB viene spesso usato sui monitor dei computer. Di conseguenza, dipende dal dispositivo. Le stampanti in [](c.md)genere usano coloranti CMYK . Ogni stampante implementa la propria versione dello spazio colore CMYK. Le immagini digitali potrebbero non archiviare effettivamente i colori in esse. Possono archiviare i numeri di indice in una tavolozza di colori. Il risultato è che è molto difficile per i singoli sviluppatori di applicazioni usare o fornire un metodo standardizzato per spostare le immagini a colori da un dispositivo a un altro. I professionisti della creazione di immagini in genere provano la frustrazione della creazione di un'immagine grafica sullo schermo di un computer e la sua visualizzazione in modo molto diverso quando viene stampata. WCS 1.0 consente di soddisfare queste esigenze di creazione dell'immagine.

 

 




