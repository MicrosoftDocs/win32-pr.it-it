---
title: Rendering degli Intent
description: Il International Color Consortium (ICC) ha definito quattro valori diversi, detti Intent di rendering.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), rendering Intent
- WCS (sistema di colori Windows), rendering Intent
- Gestione colori immagine, rendering Intent
- gestione dei colori, rendering degli Intent
- colori, rendering degli Intent
- rendering degli Intent
- International Color Consortium (ICC)
- IIC (International Color Consortium)
- Finalità immagine
- Finalità grafiche
- Finalità di prova
- Finalità della corrispondenza
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321012"
---
# <a name="rendering-intents"></a>Rendering degli Intent

Il International Color Consortium (ICC) ha definito quattro valori diversi, detti *Intent di rendering*. Rappresentano quattro diversi approcci alla creazione di un rendering dei colori. Questi quattro Intent e le costanti usate per fare riferimento a essi nel codice sono i seguenti.



| Finalità                            | Nome ICC              | Descrizione                    |
|-----------------------------------|-----------------------|--------------------------------|
| Immagine | Percettivo            | \_percettivo preventivo             |
| Graphic | Saturazione            | \_saturazione preventivo             |
| Proof     | Colorimetrico relativo | \_colorimetrico relativo per finalità \_ |
| Corrispondenza     | Colorimetrico assoluto | \_colorimetrico assoluto \_ preventivo |




 

La specifica del formato del profilo ICC versione 3,4, che descrive questi Intent, può essere scaricata da color.org.

## <a name="picture-intent"></a>Finalità immagine

Chiamata finalità percettiva nella clausola di specifica ICC 4,9, un intento dell'immagine causa la compressione o l'espansione della [gamma](./g.md) completa dell'immagine per riempire la gamma del dispositivo di destinazione, in modo che il bilanciamento del grigio venga mantenuto, ma l'accuratezza colorimetrico potrebbe non essere mantenuta.

In altre parole, se determinati colori in un'immagine non rientrano nell'intervallo di colori di cui il dispositivo di output può eseguire il rendering, lo scopo dell'immagine comporterà la regolazione di tutti i colori dell'immagine, in modo che ogni colore nell'immagine rientri nell'intervallo di cui è possibile eseguire il rendering e che la relazione tra i colori venga mantenuta il più possibile.

Questo scopo è particolarmente adatto per la visualizzazione di fotografie e immagini ed è in genere lo scopo predefinito.

## <a name="graphic-intent"></a>Finalità grafiche

La clausola ICC Specification 4,12 chiama lo scopo grafico a scopo di [saturazione](s.md) . Conserva il Chroma dei colori nell'immagine al possibile costo di [tonalità](h.md) e [luminosità](l.md).

L'implementazione di questa finalità rimane alquanto problematica e il TPI continua a funzionare sui metodi per ottenere gli effetti desiderati.

Questo scopo è particolarmente adatto per la grafica aziendale, ad esempio i grafici, in cui è più importante che i colori siano vividi e contrastino tra loro invece che con un colore specifico.

## <a name="proof-intent"></a>Finalità di prova

Il tentativo di prova, denominato intento colorimetrico nella specifica ICC, viene definito in modo tale che tutti i colori che non rientrano nell'intervallo di cui può essere eseguito il rendering del dispositivo di output vengano adattati al colore più vicino di cui è possibile eseguire il rendering, mentre tutti gli altri colori rimangono invariati.

Lo scopo della prova non mantiene il [punto bianco](w.md).

Ad esempio, il bianco bianco di un foglio è più giallo del bianco bianco di un monitor del computer. Un'immagine convertita nella gamma della stampante che usa la finalità colorimetrico relativa comporterebbe la maggiore ingiallimento di tutti i colori. Il punto bianco dell'immagine viene spostato in modo che corrisponda al punto bianco della stampante. Tutti gli altri colori nell'immagine mantengono la relativa posizione rispetto al punto bianco. In questo modo viene generata un'immagine che riflette più accuratamente l'aspetto dell'immagine stampata. Tuttavia, l'utente può riscontrare una discordanza visiva.

## <a name="match-intent"></a>Finalità della corrispondenza

In uno scopo di corrispondenza, tutti i colori che non rientrano nell'intervallo di cui è possibile eseguire il rendering del dispositivo di output vengono adattati al colore più vicino di cui è possibile eseguire il rendering, mentre tutti gli altri colori rimangono invariati. La specifica ICC chiama lo scopo di corrispondenza colorimetrico assoluto.

Lo scopo della corrispondenza conserva il punto bianco.

Ad esempio, il bianco bianco di un foglio è più giallo del bianco bianco di un monitor del computer. Un'immagine convertita nella [gamma](./g.md) della stampante con finalità di corrispondenza comporterebbe la conversione di tutti i colori e la corrispondenza nella gamma della stampante. Il punto bianco dell'immagine non viene spostato in modo che corrisponda al punto bianco della stampante. Pertanto, la distanza dei colori al punto bianco può variare. Questa operazione produce un'immagine che risulta meno visivamente disconcertante per l'utente, ma è anche una versione meno precisa dell'output della stampante.

 

 