---
title: Utilizzo di Network Monitor per visualizzare i file ETL
description: Network Monitor 3,3 consente agli utenti di analizzare, filtrare e visualizzare un file ETL (utilizzando Windows Vista o versione successiva).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "103968793"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Utilizzo di Network Monitor per visualizzare i file ETL

[Network Monitor 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) consente agli utenti di analizzare, filtrare e visualizzare un file ETL (utilizzando Windows Vista o versione successiva). Se si utilizza Network Monitor 3,2, sarà necessario scaricare e installare parser aggiuntivi da [codeplex](https://www.codeplex.com/NMParsers) per eseguire il rendering degli eventi di traccia di rete.

I file ETL correlati raggruppano insieme gli eventi rilevanti. Il ScrollBar seguente mostra un file correlato aperto in Network Monitor, con la conversazione abilitata.

![Screenshot che mostra la Network Monitor, con eventi correlati evidenziati nella finestra a sinistra e UTEvent evidenziati dall'elenco a discesa.](images/ut-netmon1.png)

Gli eventi correlati vengono raggruppati per attività nel riquadro sinistro. È possibile selezionare un evento nel riquadro Riepilogo Frame, quindi fare clic con il pulsante destro del mouse per selezionare la conversazione a livello di evento di rete. Verrà visualizzata un'attività correlata nel riquadro sinistro.

Se si seleziona una determinata attività dal riquadro a sinistra per espanderla, verrà visualizzato l'elenco dei provider per gli eventi correlati.

![Screenshot che mostra la Network Monitor con un'attività selezionata nel riquadro sinistro e gli eventi corrispondenti a tale evento nel riquadro di destra.](images/ut-netmon2.png)

Quando si seleziona un provider specifico nel riquadro a sinistra, nel riquadro Riepilogo frame verrà visualizzato un elenco di eventi specifici del provider e dell'attività.

![Screenshot che mostra un provider specifico selezionato nel riquadro a sinistra e un elenco di eventi specifici del provider evidenziato nel riquadro superiore destro.](images/ut-netmon3.png)

I filtri possono essere applicati in Network Monitor per semplificare la visualizzazione e la ricerca degli eventi o dei pacchetti corretti. Ad esempio, è possibile applicare un filtro agli eventi di errore selezionati (ad esempio, **UTEvent. Header. Descriptor. Level = = 2**) per visualizzarli in un determinato colore.

![Screenshot che mostra la finestra di dialogo "modifica filtro colori".](images/ut-netmon4.png)

I filtri possono essere applicati anche per contrassegnare diversi provider in colori diversi, in modo da semplificare la visualizzazione dei risultati.

![Screenshot che mostra un esempio di provider diversi contrassegnati con colori diversi.](images/ut-netmon5.png)

Per applicare un filtro, fare clic su **ColorFilters** nel menu **filtri** .

Nella tabella seguente vengono illustrati alcuni esempi di filtri utili.



| Filtra                                                                        | Descrizione                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent. Header. Descriptor. Level = = 2                                          | Filtra solo gli eventi di errore.                                        |
| UTEvent. Header. Descriptor. Level = = 3                                          | Filtra solo gli eventi di avviso.                                      |
| UTEvent.Header.Descriptor.Id = = 2001                                          | Filtra solo gli eventi con ID evento 2001.                           |
| \_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN                                          | Filtra solo gli eventi del servizio WLAN.                            |
| \_MicrosoftWindowsNWiFi N802                                                   | Filtra solo gli eventi dal driver WiFi nativo.                  |
| WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG e UTEvent.Header.Descriptor.ID = = 2001 | Filtra solo gli eventi con ID evento 2001 generati dal servizio WLAN. |



 

 

 




