---
description: I messaggi vengono usati per notificare all'applicazione gli eventi asincroni. Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Messaggi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd0a73a5ed845901d3cbe937a366a357c149541e8973a423310345dc241b92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002729"
---
# <a name="tapi-messages"></a>Messaggi TAPI

I messaggi vengono usati per notificare all'applicazione gli eventi asincroni. Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in [**lineInitializeEx.**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)

Il messaggio contiene sempre un handle per l'oggetto pertinente (telefono, linea o chiamata), che l'applicazione può usare per determinare il tipo di messaggio.

Alcuni messaggi vengono usati per notificare all'applicazione una modifica dello stato di un oggetto. Questi messaggi forniscono l'handle di oggetto e indicano quale elemento di stato è stato modificato. L'applicazione può chiamare la funzione appropriata "get status" dell'oggetto per ottenere lo stato completo dell'oggetto.

Quando si verifica un evento, i messaggi possono essere inviati a zero, una o più applicazioni. Le applicazioni di destinazione per un messaggio sono determinate da diversi fattori, tra cui il significato del messaggio, il privilegio dell'applicazione per l'oggetto, se l'applicazione ha avviato o meno la richiesta per cui il messaggio è un risultato diretto e la maschera del messaggio impostata dall'applicazione. Tenere presente quanto segue sui messaggi:

-   I messaggi di risposta asincroni vengono inviati solo all'applicazione che ha originato la richiesta e non possono essere mascherati.
-   I messaggi che segnalano il completamento della generazione di cifre o toni o la raccolta di cifre vengono inviati solo all'applicazione che ha richiesto la generazione di cifre o toni.
-   I messaggi che indicano le modifiche dello stato della riga o dell'indirizzo vengono inviati a tutte le applicazioni che hanno aperto la riga, purché il messaggio sia stato abilitato tramite [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   I messaggi che indicano lo stato della chiamata e le modifiche alle informazioni sulle chiamate vengono inviati a tutte le applicazioni che hanno un handle per la chiamata.
-   I messaggi che segnalano il rilevamento di una cifra, del tono o del tipo di supporto vengono inviati alle applicazioni che hanno richiesto il monitoraggio dell'evento.

Questa sezione contiene le informazioni di riferimento per i messaggi TAPI seguenti:

-   [Messaggi di telefonia assistita](assisted-telephony-messages.md)
-   [Messaggi del call center](call-center-messages.md)
-   [Messaggi di errore formattati](formatted-error-messages.md)
-   [Messaggi del dispositivo line](line-device-messages.md)
-   [Telefono Messaggi del dispositivo](phone-device-messages.md)

 

 



