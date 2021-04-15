---
description: Attributi dell'evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Attributi evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524530"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Attributi evento (Microsoft Media Foundation)

Gli attributi seguenti si applicano agli eventi.



| Attributo                                                                                                        | Descrizione                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF \_ evento \_ do \_ assottigliamento**](mf-event-do-thinning-attribute.md)                                                | Quando un'origine multimediale richiede una nuova velocità di riproduzione, specifica se l'origine richiede anche l'assottigliamento.                |
| [**\_nodo di \_ output \_ evento MF**](mf-event-output-node-attribute.md)                                                | Identifica il nodo della topologia per un sink di flusso.                                                                       |
| [**\_ \_ \_ offset ora presentazione evento \_ MF**](mf-event-presentation-time-offset-attribute.md)                     | Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.                                              |
| [**\_tempo di \_ SCRUBSAMPLE \_ evento MF**](mf-event-scrubsample-time-attribute.md)                                      | Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.                                                     |
| [**\_SESSIONCAPS evento \_ MF**](mf-event-sessioncaps-attribute.md)                                                 | Contiene i flag che definiscono le funzionalità della sessione multimediale in base alla presentazione corrente.                  |
| [**\_ \_ Delta SESSIONCAPS evento \_ MF**](mf-event-sessioncaps-delta-attribute.md)                                    | Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente. |
| [**\_ \_ \_ inizio effettivo origine evento \_ MF**](mf-event-source-actual-start-attribute.md)                               | Contiene l'ora di inizio del riavvio di un'origine multimediale dalla posizione corrente.                                       |
| [**\_caratteristiche dell' \_ origine \_ evento MF**](mf-event-source-characteristics-attribute.md)                          | Specifica le caratteristiche correnti dell'origine multimediale.                                                            |
| [**\_ \_ caratteristiche origine evento \_ MF \_ obsolete**](mf-event-source-characteristics-old-attribute.md)                 | Specifica le caratteristiche precedenti dell'origine multimediale.                                                           |
| [**\_ \_ \_ inizio Fake origine evento \_ MF**](mf-event-source-fake-start-attribute.md)                                   | Specifica se la topologia del segmento corrente è vuota.                                                              |
| [**\_origine evento \_ MF \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | Specifica l'ora di inizio per una topologia di segmento.                                                                      |
| [**\_ \_ topologia di origine evento MF \_ \_ annullata**](mf-event-source-topology-canceled-attribute.md)                     | Specifica se l'origine del sequencer ha annullato una topologia.                                                           |
| [**\_ora di \_ presentazione di inizio evento \_ MF \_**](mf-event-start-presentation-time-attribute.md)                       | Ora di inizio per la presentazione, in unità di 100 nanosecondi, misurata dal clock di presentazione.               |
| [**\_ \_ \_ \_ ora di presentazione dell'avvio \_ dell'evento MF nell' \_ output**](mf-event-start-presentation-time-at-output-attribute.md) | Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.                      |
| [**\_ \_ stato topologia evento MF \_**](mf-event-topology-status-attribute.md)                                        | Specifica lo stato di una topologia durante la riproduzione.                                                                   |
| [**\_tempo di \_ \_ \_ ricorrenza \_ evento MF Session approx**](mf-session-approx-event-occurrence-time-attribute.md)        | Ora approssimativa in cui la sessione multimediale ha generato un evento.                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



