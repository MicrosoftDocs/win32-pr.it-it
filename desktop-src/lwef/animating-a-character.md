---
title: Animazione di un carattere
description: Animazione di un carattere
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976781"
---
# <a name="animating-a-character"></a>Animazione di un carattere

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Dopo aver caricato un carattere, è possibile usare diversi metodi di Microsoft Agent per animare il carattere. Il primo che si usa è in genere il [**metodo Show.**](show-method.md) **Show** rende visibile il fotogramma del carattere e riproduce l'animazione assegnata allo stato **Showing del** carattere.

Quando il frame del carattere è visibile, è possibile usare il metodo [**Play,**](play-method.md) specificando il nome di un'animazione, per riprodurre l'animazione. I nomi delle animazioni sono specifici di una definizione di carattere. Durante la riproduzione di un'animazione, la forma della finestra cambia in modo da corrispondere all'immagine nel frame. Il risultato è un'immagine grafica mobile, o *sprite,* visualizzata sopra il desktop e tutte le finestre o in *ordine Z.*

Se il file del carattere è archiviato in locale, è sufficiente chiamare il [**metodo Play.**](play-method.md) In altri casi, ad esempio quando è stato caricato un oggetto . Carattere ACF da un server HTTP, è necessario usare il [**metodo Get**](get-method.md) (o [**Prepare)**](/windows/desktop/lwef/iagentcharacter--prepare)per recuperare prima i dati dell'animazione. In questo modo Agent richiederà il file di animazione al server e lo archivierà nel buffer del browser nel computer locale.

Il [**metodo Speak**](speak-method.md) consente di programmare il carattere per parlare, sincronizzando automaticamente l'output. Altri dettagli sono trattati nella sezione Output di questo documento.

È possibile usare il [**metodo MoveTo**](moveto-method.md) per posizionare il carattere in una nuova posizione. Quando si chiama il **metodo MoveTo,** Microsoft Agent riproduce automaticamente l'animazione appropriata in base alla posizione corrente del carattere, quindi sposta il frame del carattere. Analogamente, quando si chiama [**GestureAt**](gestureat-method.md), Microsoft Agent riproduce l'animazione di inserimento appropriata in base alla posizione del carattere e alla posizione specificata nella chiamata.

Per nascondere il carattere, chiamare il [metodo Hide.](hide-method.md) Viene riprodotto automaticamente il carattere associato allo stato **Nascondi** del carattere, quindi viene nascosta la cornice del carattere. Tuttavia, è anche possibile nascondere o visualizzare un carattere impostando la proprietà [**Visible del**](visible-property.md) carattere.

Microsoft Agent elabora tutte le chiamate di animazione, o *richiede*, in modo asincrono. Ciò consente al codice dell'applicazione di continuare a gestire altri eventi durante l'elaborazione della richiesta. Ad esempio, le chiamate al [**metodo Play**](play-method.md) posizionano l'animazione in una coda per il carattere in modo che le animazioni possano essere riprodotte in sequenza. Ciò significa tuttavia che non è possibile presupporre che una chiamata ad altre funzioni verrà necessariamente eseguita dopo un'animazione che segue nel codice. Ad esempio, in genere, un'istruzione che segue una chiamata a **Play** o [**MoveTo**](moveto-method.md) verrà eseguita prima del completamento dell'animazione.

È possibile sincronizzare il codice con le animazioni nella coda di un carattere creando un riferimento all'oggetto [](the-request-object.md) alla richiesta di animazione e, quando l'animazione viene avviata o completata, monitorando gli eventi Request che il server usa per notificare il carattere ai client. Ad esempio, se si vuole che venga visualizzata una finestra di messaggio quando il carattere termina un'animazione, è possibile inserire la chiamata della finestra di messaggio nella subroutine di gestione degli eventi [**RequestComplete,**](requestcomplete-event.md) verificando l'ID richiesta specifico.

Quando un carattere è nascosto, il server non riproduce animazioni. tuttavia, ancora accoda ed elabora la richiesta di animazione (riproduce l'animazione) e passa di nuovo uno stato della richiesta al client. Nello stato nascosto, il carattere non può diventare attivo per l'input. Tuttavia, se l'utente pronuncia il nome del carattere (quando l'input vocale è abilitato), il server visualizza automaticamente il carattere.

Quando l'applicazione client carica più caratteri contemporaneamente, i servizi di animazione di Microsoft Agent consentono di animare i caratteri in modo indipendente o di usare i metodi [**Wait,**](wait-method.md) [**Interrupt**](interrupt-method.md)o [**Stop**](stop-method.md) per sincronizzare l'animazione tra loro.

Microsoft Agent riproduce automaticamente anche altre animazioni. Ad esempio, se lo stato del carattere non è cambiato per diversi secondi, Agent inizia a riprodurre animazioni assegnate alle animazioni **idling del** carattere. Analogamente, quando l'input vocale è abilitato, Agent riproduce le animazioni **listening** del carattere e quindi le animazioni **Udi** quando viene rilevata un'espressione. Queste animazioni gestite dal server sono denominate *stati* e vengono definite quando viene creato un carattere. Per altre informazioni, vedere [Progettazione di caratteri per Microsoft Agent.](agent-states.md)

 

 