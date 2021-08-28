---
description: Questa sezione illustra l'uso dei dati dei sensori di luce ambientale e come ottimizzare le funzionalità dell'interfaccia utente e il contenuto del programma per molte condizioni di illuminazione.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Creazione Light-Aware interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd97bb304c3a8718ae4b32d8b9100a1e7eb7a18240b9089c112272f588ee209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890291"
---
# <a name="creating-light-aware-user-interfaces"></a>Creazione Light-Aware interfacce utente

Questa sezione illustra l'uso dei dati dei sensori di luce ambientale e come ottimizzare le funzionalità dell'interfaccia utente e il contenuto del programma per molte condizioni di illuminazione.

I sensori di luce ambientale espongono dati che possono essere usati per determinare vari aspetti delle condizioni di illuminazione in cui si trova il sensore. I sensori di luce ambientale possono esporre la luminosità complessiva di un ambiente (illuminazione) e altri aspetti della luce circostante, ad esempio la cromaticità o la temperatura del colore.

I computer possono essere più utili in diversi modi quando il sistema risponde alle condizioni di illuminazione. Questi includono il controllo della luminosità dello schermo del computer (una nuova funzionalità completamente supportata in Windows 7), la regolazione automatica del livello di illuminazione delle tastiere illuminate e anche il controllo della luminosità per altre luci (ad esempio illuminazione dei pulsanti, luci di attività e così via).

I programmi per l'utente finale possono anche trarre vantaggio dai sensori di luce. I programmi possono applicare un tema appropriato per una particolare condizione di illuminazione, ad esempio un tema esterno specifico e un tema di interni. Probabilmente l'aspetto più importante dell'integrazione dei sensori di luce con i programmi è la leggibilità e le ottimizzazioni di leggibilità basate sulle condizioni di illuminazione.

L'API Sensor consente di creare tali programmi. Si consideri lo scenario seguente.

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Scenario: Uso del portatile per passare a un ristorante

Si supponga di voler usare il computer per passare a un nuovo ristorante. Si inizia da casa, si cerca l'indirizzo del ristorante e si pianifica l'itinerario. Lo screenshot seguente illustra come il programma di navigazione può ottimizzare l'interfaccia utente per visualizzare informazioni dettagliate nelle condizioni di illuminazione degli interni.

![interfaccia utente progettata per l'illuminazione di interni.](images/nav-normal.png)

Quando si va all'esterno dell'auto, si verificano problemi diretti che rendono difficile la lettura dello schermo del portatile. Lo screenshot seguente mostra come il programma potrebbe modificare l'interfaccia utente per ottimizzare la leggibilità/leggibilità in luce diretta. In questa visualizzazione gran parte dei dettagli è stata omessa e il contrasto è ingrandito.

![interfaccia utente progettata per condizioni di illuminazione diretta.](images/nav-contrast.png)

Quando ci si avvicina al ristorante, la sera si avvicina e diventa scura all'esterno. Nello screenshot seguente l'interfaccia utente per il programma di navigazione è stata ottimizzata per la visualizzazione poco chiaro. Grazie all'uso generale di colori più scuri, questa interfaccia utente è facile da vedere nell'auto scura.

![interfaccia utente progettata per la visualizzazione poco chiaro.](images/nav-lowlight.png)

Nella parte restante di questa sezione verranno esaminate alcune operazioni che è possibile eseguire per ottimizzare i programmi per diverse condizioni di illuminazione e come è possibile usare l'API Sensor per abilitare l'interfaccia utente che rileva la luce.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Nozioni fondamentali Light-Aware utente](fundamentals-of-light-aware-user-interfaces.md)
-   [Esempi di Light-Aware utente](examples-of-light-aware-user-interfaces.md)
-   [Ottimizzazione dell'esperienza utente](optimizing-the-user-experience.md)
-   [Comprensione e interpretazione dei valori di Unis](understanding-and-interpreting-lux-values.md)
-   [Uso dei dati dei sensori di luce](handling-data-from-multiple-light-sensors.md)

 

 



