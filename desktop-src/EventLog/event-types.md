---
description: Sono disponibili cinque tipi di eventi che è possibile registrare. Tutti questi contengono dati comuni ben definiti e possono facoltativamente includere dati specifici degli eventi.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipi di evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880889"
---
# <a name="event-types"></a>Tipi di evento

Sono disponibili cinque tipi di eventi che è possibile registrare. Tutti questi contengono dati comuni ben definiti e possono facoltativamente includere dati specifici degli eventi.

L'applicazione indica il tipo di evento quando segnala un evento. Ogni evento deve essere di un solo tipo. Il Visualizzatore eventi Visualizza un'icona diversa per ogni tipo nella visualizzazione elenco del registro eventi.

Nella tabella seguente vengono descritti i cinque tipi di eventi utilizzati nella registrazione degli eventi.



| Tipo di evento        | Descrizione                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error (Errore) (Error (Errore)e)**         | Evento che indica un problema significativo, ad esempio la perdita di dati o la perdita di funzionalità. Se, ad esempio, un servizio non viene caricato durante l'avvio, viene registrato un evento di errore.                                                                                                                           |
| **Avviso**       | Un evento che non è necessariamente significativo, ma potrebbe indicare un possibile problema futuro. Ad esempio, quando lo spazio su disco è insufficiente, viene registrato un evento di avviso. Se un'applicazione può eseguire il ripristino da un evento senza perdita di funzionalità o dati, in genere può classificare l'evento come un evento di avviso.     |
| **Informazioni**   | Evento che descrive il funzionamento corretto di un'applicazione, un driver o un servizio. Ad esempio, quando un driver di rete viene caricato correttamente, potrebbe essere opportuno registrare un evento informativo. Si noti che in genere non è appropriato che un'applicazione desktop registri un evento ogni volta che viene avviato. |
| **Controllo con esito positivo** | Un evento che registra un tentativo di accesso di sicurezza controllato che ha avuto esito positivo. Ad esempio, un tentativo dell'utente di accedere al sistema viene registrato come evento di controllo con esito positivo.                                                                                                                        |
| **Controllo con esito negativo** | Un evento che registra un tentativo di accesso di sicurezza controllato che ha esito negativo. Se, ad esempio, un utente tenta di accedere a un'unità di rete e ha esito negativo, il tentativo viene registrato come evento di controllo non riuscito.                                                                                                                   |



 

Le attività selezionate degli utenti possono essere rilevate tramite il controllo degli eventi di sicurezza e quindi l'inserimento di voci nel registro di sicurezza di un computer.

 

 



