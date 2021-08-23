---
description: Attributi dell'evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Attributi evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600511"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Attributi evento (Microsoft Media Foundation)

Gli attributi seguenti si applicano agli eventi.



| Attributo                                                                                                        | Descrizione                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_DIRADAMENTO DELLE DO DI \_ EVENTI MF \_**](mf-event-do-thinning-attribute.md)                                                | Quando un'origine multimediale richiede una nuova velocità di riproduzione, specifica se anche l'origine richiede un thinning.                |
| [**NODO DI OUTPUT DEGLI EVENTI MF \_ \_ \_**](mf-event-output-node-attribute.md)                                                | Identifica il nodo della topologia per un sink di flusso.                                                                       |
| [**MF \_ EVENT \_ PRESENTATION \_ TIME \_ OFFSET**](mf-event-presentation-time-offset-attribute.md)                     | Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.                                              |
| [**TEMPO DI \_ \_ SCRUBSAMPLE DELL'EVENTO MF \_**](mf-event-scrubsample-time-attribute.md)                                      | Ora di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.                                                     |
| [**MF \_ EVENT \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)                                                 | Contiene flag che definiscono le funzionalità della sessione multimediale, in base alla presentazione corrente.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md)                                    | Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente. |
| [**AVVIO EFFETTIVO \_ \_ DELL'ORIGINE \_ EVENTO \_ MF**](mf-event-source-actual-start-attribute.md)                               | Contiene l'ora di inizio del riavvio di un'origine multimediale dalla posizione corrente.                                       |
| [**CARATTERISTICHE \_ DELL'ORIGINE EVENTO MF \_ \_**](mf-event-source-characteristics-attribute.md)                          | Specifica le caratteristiche correnti dell'origine multimediale.                                                            |
| [**CARATTERISTICHE \_ DELL'ORIGINE EVENTO MF \_ \_ \_ PRECEDENTE**](mf-event-source-characteristics-old-attribute.md)                 | Specifica le caratteristiche precedenti dell'origine multimediale.                                                           |
| [**AVVIO FALSO \_ \_ DELL'ORIGINE EVENTO \_ MF \_**](mf-event-source-fake-start-attribute.md)                                   | Specifica se la topologia del segmento corrente è vuota.                                                              |
| [**MF \_ EVENT \_ SOURCE \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | Specifica l'ora di inizio per una topologia di segmento.                                                                      |
| [**TOPOLOGIA \_ \_ DELL'ORIGINE \_ EVENTO MF \_ ANNULLATA**](mf-event-source-topology-canceled-attribute.md)                     | Specifica se l'origine sequencer ha annullato una topologia.                                                           |
| [**ORA DI \_ INIZIO \_ PRESENTAZIONE \_ DELL'EVENTO \_ MF**](mf-event-start-presentation-time-attribute.md)                       | Ora di inizio della presentazione, in unità di 100 nanosecondi, misurata dall'orologio della presentazione.               |
| [**ORA DI INIZIO PRESENTAZIONE DELL'EVENTO MF \_ \_ \_ \_ \_ \_ ALL'OUTPUT**](mf-event-start-presentation-time-at-output-attribute.md) | Ora di presentazione in cui i sink multimediali eseguiranno il rendering del primo esempio della nuova topologia.                      |
| [**STATO DELLA TOPOLOGIA \_ \_ DI EVENTI MF \_**](mf-event-topology-status-attribute.md)                                        | Specifica lo stato di una topologia durante la riproduzione.                                                                   |
| [**ORA \_ \_ OCCORRENZA EVENTO APPROX \_ \_ SESSIONE \_ MF**](mf-session-approx-event-occurrence-time-attribute.md)        | Ora approssimativa in cui la sessione multimediale ha generato un evento.                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 



