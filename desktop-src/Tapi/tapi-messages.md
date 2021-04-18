---
description: I messaggi vengono utilizzati per notificare all'applicazione gli eventi asincroni. Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Messaggi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316022"
---
# <a name="tapi-messages"></a>Messaggi TAPI

I messaggi vengono utilizzati per notificare all'applicazione gli eventi asincroni. Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).

Il messaggio contiene sempre un handle per l'oggetto pertinente (telefono, riga o chiamata), che può essere utilizzato dall'applicazione per determinare il tipo di messaggio.

Alcuni messaggi vengono utilizzati per notificare all'applicazione la modifica dello stato di un oggetto. Questi messaggi forniscono l'handle dell'oggetto e indicano l'elemento di stato modificato. L'applicazione può chiamare la funzione "Get status" appropriata dell'oggetto per ottenere lo stato completo dell'oggetto.

Quando si verifica un evento, i messaggi possono essere inviati a zero, a una o più applicazioni. Le applicazioni di destinazione per un messaggio sono determinate da diversi fattori, tra cui il significato del messaggio, il privilegio dell'applicazione per l'oggetto, indipendentemente dal fatto che l'applicazione abbia avviato la richiesta per la quale il messaggio è un risultato diretto e la maschera dei messaggi impostata dall'applicazione. Tenere presente i seguenti punti relativi ai messaggi:

-   I messaggi di risposta asincroni vengono inviati solo all'applicazione che ha originato la richiesta e non possono essere mascherati.
-   I messaggi che segnalano il completamento della generazione di numeri o toni o la raccolta di cifre vengono inviati solo all'applicazione che ha richiesto la generazione di numeri o toni.
-   I messaggi che indicano le modifiche dello stato della riga o dell'indirizzo vengono inviati a tutte le applicazioni che hanno aperto la riga, a condizione che il messaggio sia stato abilitato tramite [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   I messaggi che indicano le modifiche allo stato della chiamata e alle informazioni sulle chiamate vengono inviati a tutte le applicazioni che dispongono di un handle per la chiamata.
-   I messaggi che segnalano il rilevamento di una cifra, il rilevamento di un tono o il rilevamento del tipo di supporto vengono inviati alle applicazioni che hanno richiesto il monitoraggio dell'evento.

Questa sezione contiene le informazioni di riferimento per i messaggi TAPI seguenti:

-   [Messaggi di telefonia assistita](assisted-telephony-messages.md)
-   [Messaggi del Call Center](call-center-messages.md)
-   [Messaggi di errore formattati](formatted-error-messages.md)
-   [Messaggi linea dispositivo](line-device-messages.md)
-   [Messaggi del dispositivo telefonico](phone-device-messages.md)

 

 



