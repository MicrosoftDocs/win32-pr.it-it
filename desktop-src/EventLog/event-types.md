---
description: Esistono cinque tipi di eventi che possono essere registrati. Tutti questi dati hanno dati comuni ben definiti e possono includere facoltativamente dati specifici dell'evento.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipi di evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e94ae69445f660e54c630734b93297acad593c127f32b9d3abfa94f9cd2fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069561"
---
# <a name="event-types"></a>Tipi di evento

Esistono cinque tipi di eventi che possono essere registrati. Tutti questi dati hanno dati comuni ben definiti e possono includere facoltativamente dati specifici dell'evento.

L'applicazione indica il tipo di evento quando segnala un evento. Ogni evento deve essere di un singolo tipo. Il Visualizzatore eventi visualizza un'icona diversa per ogni tipo nella visualizzazione elenco del registro eventi.

Nella tabella seguente vengono descritti i cinque tipi di evento utilizzati nella registrazione degli eventi.



| Tipo di evento        | Descrizione                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error (Errore) (Error (Errore)e)**         | Evento che indica un problema significativo, ad esempio la perdita di dati o la perdita di funzionalità. Ad esempio, se un servizio non viene caricato durante l'avvio, viene registrato un evento Error.                                                                                                                           |
| **Avviso**       | Evento non necessariamente significativo, ma che può indicare un possibile problema futuro. Ad esempio, quando lo spazio su disco è insufficiente, viene registrato un evento Avviso. Se un'applicazione può eseguire il ripristino da un evento senza perdita di funzionalità o dati, in genere può classificare l'evento come evento di avviso.     |
| **Informazioni**   | Evento che descrive il corretto funzionamento di un'applicazione, un driver o un servizio. Ad esempio, quando un driver di rete viene caricato correttamente, potrebbe essere appropriato registrare un evento Di informazioni. Si noti che non è in genere appropriato per un'applicazione desktop registrare un evento a ogni avvio. |
| **Controllo con esito positivo** | Evento che registra un tentativo di accesso di sicurezza con esito positivo. Ad esempio, il tentativo riuscito di un utente di accedere al sistema viene registrato come evento success audit.                                                                                                                        |
| **Controllo con esito negativo** | Evento che registra un tentativo di accesso di sicurezza controllato che ha esito negativo. Ad esempio, se un utente tenta di accedere a un'unità di rete e non riesce, il tentativo viene registrato come evento di controllo degli errori.                                                                                                                   |



 

È possibile tenere traccia delle attività selezionate degli utenti controllando gli eventi di sicurezza e inserendo le voci nel registro di sicurezza di un computer.

 

 



