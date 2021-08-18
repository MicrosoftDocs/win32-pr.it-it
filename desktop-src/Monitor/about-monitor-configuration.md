---
title: Informazioni sulla configurazione del monitoraggio
description: Informazioni sulla configurazione del monitoraggio
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitor,about
- monitor, calibrazione dei colori
- monitoraggio, regolazione dell'area di visualizzazione del monitor
- monitoraggio, salvataggio delle impostazioni di monitoraggio
- monitoraggio,ripristino delle impostazioni di monitoraggio
- monitoraggio, funzionalità del fornitore
- calibrazione dei colori
- regolazione dell'area di visualizzazione del monitor
- salvataggio delle impostazioni del monitoraggio
- ripristino delle impostazioni di monitoraggio
- funzionalità del fornitore
- monitorare la configurazione, calibrazione dei colori
- monitorare la configurazione, informazioni
- configurazione del monitoraggio, regolazione dell'area di visualizzazione del monitor
- monitorare la configurazione, salvataggio delle impostazioni di monitoraggio
- monitorare la configurazione, ripristino delle impostazioni di monitoraggio
- monitorare la configurazione, funzionalità del fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5f3d8c56521c07d704fe586f486298d0e679d1bfc33e25a29d943aa92dd66e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146184"
---
# <a name="about-monitor-configuration"></a>Informazioni sulla configurazione del monitoraggio

Gli usi per le funzioni di configurazione del monitoraggio includono:

-   Calibrazione del colore. Un monitor calibrato correttamente riproduce correttamente i colori. In genere, un'applicazione di calibrazione dei colori visualizza un modello di test e dispone di controlli per modificare un'impostazione di monitoraggio. L'utente modifica l'impostazione fino a quando non viene soddisfatta una condizione e ripete questo processo per ogni impostazione di monitoraggio fino a quando il monitoraggio non viene calibrato.
-   Regolazione dell'area di visualizzazione del monitor. Le funzioni di configurazione del monitoraggio possono essere usate per modificare le dimensioni e la posizione dell'area di visualizzazione di un monitor. Ad esempio, quando un monitor LCD è connesso a un computer usando un connettore analogico, si ottiene la migliore qualità dell'immagine quando è presente un mapping uno-a-uno tra i pixel nel buffer dei fotogrammi della scheda grafica e i pixel sul monitor LCD.
-   Salvataggio e ripristino delle impostazioni del monitoraggio. Alcuni utenti necessitano di più set di impostazioni di monitoraggio, perché scenari diversi richiedono impostazioni di monitoraggio diverse. Ad esempio, le impostazioni di monitoraggio ottimali per le applicazioni desktop non sono ottimali per guardare la tv.
-   Uso delle funzionalità di monitoraggio specifiche del fornitore. Usando le funzioni di configurazione del monitoraggio, i produttori possono creare applicazioni che usano le funzionalità specifiche del fornitore del monitoraggio.

Le funzioni di configurazione del monitoraggio sono suddivise in funzioni di alto e basso livello. Le funzioni di alto livello sono più facili da usare rispetto alle funzioni di basso livello. Per usare le funzioni di alto livello, non è necessario conoscere l'interfaccia DDC/CI (Display Data Channel Command Interface). Tuttavia, le funzioni di alto livello non consentono l'accesso alle funzionalità specifiche del fornitore del monitoraggio.

Le funzioni di basso livello sono un thin wrapper per i comandi DDC/CI. Per usare le funzioni di basso livello, è necessario avere familiarità con lo standard DDC/CI e con lo standard VESA Monitor Control Command Set (MCCS). In genere, è consigliabile usare le funzioni di alto livello, a meno che non sia necessario usare funzionalità disponibili solo nelle funzioni di basso livello.

Le funzioni di configurazione di monitoraggio di alto livello sono progettate in modo che un'applicazione non possa inserire un monitoraggio in uno stato inutilizzabile. Le funzioni di basso livello possono essere usate per inviare codici VCP al monitoraggio. Tenere tuttavia presente che alcuni codici VCP possono disabilitare funzionalità importanti o impostare il monitoraggio in uno stato in cui l'utente non può visualizzare l'immagine visualizzata. Per altre informazioni, vedere lo standard VESA Monitor Control Command Set (MCCS).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitorare la configurazione](monitor-configuration.md)
</dt> </dl>

 

 




