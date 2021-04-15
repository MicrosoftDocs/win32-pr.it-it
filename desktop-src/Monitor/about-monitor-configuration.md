---
title: Informazioni sulla configurazione del monitoraggio
description: Informazioni sulla configurazione del monitoraggio
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitoraggio, informazioni
- monitoraggio, calibrazione colore
- monitoraggio, regolazione dell'area di visualizzazione del monitoraggio
- monitorare, salvare le impostazioni di monitoraggio
- monitoraggio, ripristino delle impostazioni di monitoraggio
- monitoraggio, funzionalità fornitore
- calibrazione colore
- regolazione dell'area di visualizzazione del monitoraggio
- salvataggio delle impostazioni di monitoraggio
- ripristino delle impostazioni di monitoraggio
- funzionalità fornitore
- configurazione del monitoraggio, calibrazione del colore
- configurazione del monitoraggio, informazioni
- configurazione del monitoraggio, regolazione dell'area di visualizzazione del monitoraggio
- monitorare la configurazione, salvare le impostazioni di monitoraggio
- configurazione del monitoraggio, ripristino delle impostazioni di monitoraggio
- monitorare la configurazione, le funzionalità del fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515682"
---
# <a name="about-monitor-configuration"></a>Informazioni sulla configurazione del monitoraggio

Gli utilizzi per le funzioni di configurazione di monitoraggio includono:

-   Calibrazione del colore. Un monitoraggio correttamente calibrato riproduce correttamente i colori. In genere, un'applicazione di calibrazione colori Visualizza un criterio di test e dispone di controlli per modificare un'impostazione di monitoraggio. L'utente modifica l'impostazione fino a quando non viene soddisfatta una condizione e ripete questo processo per ogni impostazione di monitoraggio fino a quando non viene calibrato il monitor.
-   Regolazione dell'area di visualizzazione del monitoraggio. Le funzioni di configurazione del monitoraggio possono essere utilizzate per modificare le dimensioni e la posizione dell'area di visualizzazione di un monitor. Ad esempio, quando un monitor LCD è connesso a un computer usando un connettore analogico, viene ottenuta la migliore qualità dell'immagine quando è presente un mapping uno-a-uno tra i pixel nel buffer frame della scheda grafica e i pixel sul monitor LCD.
-   Salvataggio e ripristino delle impostazioni di monitoraggio. Alcuni utenti necessitano di più set di impostazioni di monitoraggio, perché diversi scenari richiedono impostazioni di monitoraggio diverse. Ad esempio, le impostazioni di monitoraggio ottimali per le applicazioni desktop non sono ottimali per la visione della televisione.
-   Utilizzo delle funzionalità di monitoraggio specifiche del fornitore. Utilizzando le funzioni di configurazione del monitoraggio, i produttori possono creare applicazioni che utilizzano le funzionalità specifiche del fornitore del monitoraggio.

Le funzioni di configurazione del monitoraggio sono divise in funzioni di alto livello e di basso livello. Le funzioni di alto livello sono più facili da utilizzare rispetto alle funzioni di basso livello. Per utilizzare le funzioni di alto livello, non è necessario conoscere l'interfaccia del comando Visualizza canale dati (DDC/CI). Tuttavia, le funzioni di alto livello non consentono di accedere alle funzionalità specifiche del fornitore del monitoraggio.

Le funzioni di basso livello sono un wrapper sottile intorno ai comandi DDC/CI. Per usare le funzioni di basso livello, è necessario avere familiarità con lo standard DDC/CI e anche con lo standard MCCS (VESA Monitor Control Command Set). In genere, è consigliabile utilizzare le funzioni di alto livello, a meno che non sia necessario utilizzare funzionalità disponibili solo nelle funzioni di basso livello.

Le funzioni di configurazione di monitoraggio di alto livello sono progettate in modo che un'applicazione non possa mettere un monitoraggio in uno stato inutilizzabile. È possibile utilizzare le funzioni di basso livello per inviare codici VCP al monitoraggio. Tuttavia, tenere presente che alcuni codici VCP possono disabilitare funzionalità importanti o impostare il monitoraggio in uno stato in cui l'utente non è in grado di visualizzare l'immagine di visualizzazione. Per ulteriori informazioni, vedere lo standard MCCS (VESA Monitor Control Command Set).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del monitoraggio](monitor-configuration.md)
</dt> </dl>

 

 




