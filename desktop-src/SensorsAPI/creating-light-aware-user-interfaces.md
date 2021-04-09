---
description: Questa sezione illustra l'uso dei dati del sensore luce di ambiente e il modo in cui le funzionalità dell'interfaccia utente e il contenuto del programma possono essere ottimizzati per molte condizioni di illuminazione.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Creazione di interfacce utente Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968005"
---
# <a name="creating-light-aware-user-interfaces"></a>Creazione di interfacce utente Light-Aware

Questa sezione illustra l'uso dei dati del sensore luce di ambiente e il modo in cui le funzionalità dell'interfaccia utente e il contenuto del programma possono essere ottimizzati per molte condizioni di illuminazione.

I sensori di ambiente chiaro espongono i dati che possono essere usati per determinare i vari aspetti delle condizioni di illuminazione in cui si trova il sensore. I sensori di luce di ambiente possono esporre la luminosità complessiva di un ambiente (illuminazione) e di altri aspetti della luce circostante, ad esempio la cromaticità o la temperatura dei colori.

I computer possono essere più utili in diversi modi quando il sistema risponde alle condizioni di illuminazione. Questi includono il controllo della luminosità dello schermo del computer (una nuova funzionalità completamente supportata in Windows 7), la regolazione automatica del livello di illuminazione delle tastiere illuminate e anche il controllo della luminosità per altre luci, ad esempio l'illuminazione dei pulsanti, le luci delle attività e così via.

I programmi per gli utenti finali possono trarre vantaggio anche dai sensori leggeri. I programmi possono applicare un tema appropriato per una particolare condizione di illuminazione, ad esempio un tema esterno specifico e un tema interno. Forse l'aspetto più importante dell'integrazione dei sensori di luce con i programmi è la leggibilità e le ottimizzazioni di leggibilità basate sulle condizioni di illuminazione.

L'API Sensor consente di creare programmi di questo tipo. Si consideri lo scenario seguente.

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Scenario: uso del computer portatile per passare a un ristorante

Si supponga di voler usare il computer per accedere a un nuovo ristorante. Si inizia a casa, si cerca l'indirizzo del ristorante e si pianifica il percorso. Lo screenshot seguente mostra in che modo il programma di navigazione potrebbe ottimizzare l'interfaccia utente per visualizzare informazioni dettagliate sulle condizioni di illuminazione interna.

![interfaccia utente progettata per l'illuminazione interna.](images/nav-normal.png)

Quando si esce dalla propria auto, viene visualizzato il sole diretto, che rende difficile la lettura dello schermo del portatile. Lo screenshot seguente illustra il modo in cui il programma potrebbe modificare l'interfaccia utente per ottimizzare la leggibilità e la leggibilità con la luce diretta. In questa visualizzazione, gran parte del dettaglio è stata omessa e il contrasto è ingrandito.

![interfaccia utente progettata per le condizioni di illuminazione diretta.](images/nav-contrast.png)

Man mano che ci si avvicina al ristorante, la sera si avvicina e diventa scura al di fuori. Nello screenshot seguente, l'interfaccia utente per il programma di navigazione è stata ottimizzata per la visualizzazione di bassa luminosità. Usando i colori più scuri nel suo complesso, questa interfaccia utente è facile da guardare nell'auto scura.

![interfaccia utente progettata per la visualizzazione a bassa luminosità.](images/nav-lowlight.png)

Nella parte restante di questa sezione si esamineranno alcune operazioni che è possibile eseguire per ottimizzare i programmi per diverse condizioni di illuminazione e come usare l'API del sensore per abilitare l'interfaccia utente che supporta la luce.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Nozioni fondamentali sulle interfacce utente Light-Aware](fundamentals-of-light-aware-user-interfaces.md)
-   [Esempi di interfacce utente Light-Aware](examples-of-light-aware-user-interfaces.md)
-   [Ottimizzazione dell'esperienza utente](optimizing-the-user-experience.md)
-   [Informazioni e interpretazione dei valori Lux](understanding-and-interpreting-lux-values.md)
-   [Uso dei dati del sensore chiaro](handling-data-from-multiple-light-sensors.md)

 

 



