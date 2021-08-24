---
title: Uso Network Monitor per visualizzare i file ETL
description: Network Monitor 3.3 consente agli utenti di analizzare, filtrare e visualizzare un file ETL (usando Windows Vista o versioni successive).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8c794b04837cc9d32b265eb81bfeb08fa47bdc1730672971ff6824b31c8ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685697"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Uso Network Monitor per visualizzare i file ETL

[Network Monitor 3.3 consente](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) agli utenti di analizzare, filtrare e visualizzare un file ETL (usando Windows Vista o versioni successive). Se si usa Network Monitor 3.2, sarà necessario scaricare e installare parser aggiuntivi da [CodePlex](https://www.codeplex.com/NMParsers) per eseguire il rendering degli eventi di traccia di rete.

I file ETL correlati raggruppano gli eventi pertinenti. L'esempio seguente mostra un file correlato aperto in Network Monitor, con la conversazione abilitata.

![Screenshot che mostra la Network Monitor, con gli eventi correlati evidenziati nella finestra a sinistra e UTEvent evidenziati dall'elenco a discesa.](images/ut-netmon1.png)

Gli eventi correlati vengono raggruppati in base all'attività nel riquadro sinistro. È possibile selezionare un evento nel riquadro Riepilogo frame e quindi fare clic con il pulsante destro del mouse per selezionare la conversazione a livello di evento di rete. Verrà visualizzata un'attività correlata nel riquadro sinistro.

Se si seleziona un'attività specifica nel riquadro sinistro e la si espande, viene visualizzato l'elenco dei provider per gli eventi correlati.

![Screenshot che mostra la Network Monitor con un'attività selezionata nel riquadro sinistro e gli eventi corrispondenti a tale evento nel riquadro destro.](images/ut-netmon2.png)

Quando si seleziona un provider specifico nel riquadro sinistro, nel riquadro Riepilogo frame viene visualizzato un elenco di eventi specifici di tale provider e attività.

![Screenshot che mostra un provider specifico selezionato nel riquadro sinistro e un elenco di eventi specifici del provider evidenziato nel riquadro in alto a destra.](images/ut-netmon3.png)

I filtri possono essere applicati in Network Monitor per semplificare la visualizzazione e l'individuazione degli eventi o del pacchetto giusto. Ad esempio, è possibile applicare un filtro agli eventi di errore selezionati (ad **esempio, UTEvent.Header.Descriptor.Level == 2)** per visualizzarli con un determinato colore.

![Screenshot che mostra la finestra di dialogo "Modifica filtro colori".](images/ut-netmon4.png)

È anche possibile applicare filtri per contrassegnare provider diversi con colori diversi in modo che i risultati siano più facili da visualizzare.

![Screenshot che mostra un esempio di provider diversi contrassegnati con colori diversi.](images/ut-netmon5.png)

Per applicare un filtro, **scegliere ColorFilters** dal menu **Filtri.**

La tabella seguente mostra alcuni esempi di filtri utili.



| Filtra                                                                        | Descrizione                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent.Header.Descriptor.Level == 2                                          | Filtra solo gli eventi di errore.                                        |
| UTEvent.Header.Descriptor.Level == 3                                          | Filtra solo gli eventi di avviso.                                      |
| UTEvent.Header.Descriptor.Id == 2001                                          | Filtra solo gli eventi con ID evento 2001.                           |
| WLAN \_ MicrosoftWindowsWLANAutoConfig                                          | Filtra solo gli eventi del servizio WLAN.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtra solo gli eventi del driver Wi-Fi nativo.                  |
| WLAN \_ MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001 | Filtra solo gli eventi con ID evento 2001 generato dal servizio WLAN. |



 

 

 




