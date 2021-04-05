---
title: Animazione di un carattere
description: Animazione di un carattere
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed47b30a9bcfcdb5e305b87ced5f02526ae0056
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046621"
---
# <a name="animating-a-character"></a>Animazione di un carattere

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Una volta caricato un carattere, è possibile usare diversi metodi di Microsoft Agent per animare il carattere. Il primo da usare è in genere il metodo [**show**](show-method.md) . **Mostra** rende visibile il frame del carattere e riproduce l'animazione assegnata allo stato di **visualizzazione** del carattere.

Quando il frame del carattere è visibile, è possibile usare il metodo [**Play**](play-method.md) , specificando il nome di un'animazione, per riprodurre tale animazione. I nomi di animazione sono specifici della definizione di un carattere. Quando un'animazione viene riprodotta, la forma della finestra viene modificata in modo che corrisponda all'immagine nel frame. Si ottiene quindi un'immagine grafica mobile, o *sprite*, visualizzata sopra il desktop e tutte le finestre o l' *ordine z*.

Se il file del carattere viene archiviato localmente, è possibile chiamare semplicemente il metodo [**Play**](play-method.md) . In altri casi, ad esempio quando è stato caricato un. Il carattere ACF da un server HTTP è necessario usare il metodo [**Get**](get-method.md) (o [**preparate**](/windows/desktop/lwef/iagentcharacter--prepare)) per recuperare prima i dati dell'animazione. In questo modo, Agent richiede il file di animazione dal server e lo archivia nel buffer del browser nel computer locale.

Il metodo [**Speak**](speak-method.md) consente di programmare il carattere da pronunciare, sincronizzando automaticamente il labiale dell'output. Ulteriori dettagli sono trattati nella sezione output di questo documento.

È possibile usare il metodo [**MoveTo**](moveto-method.md) per posizionare il carattere in una nuova posizione. Quando si chiama il metodo **MoveTo** , Microsoft Agent esegue automaticamente l'animazione appropriata in base alla posizione corrente del carattere, quindi sposta il frame del carattere. Analogamente, quando si chiama [**GestureAt**](gestureat-method.md), Microsoft Agent riproduce l'animazione gestuale appropriata in base alla posizione del carattere e alla posizione specificata nella chiamata.

Per nascondere il carattere, chiamare il metodo [Hide](hide-method.md) . In questo modo viene automaticamente riprodotto il carattere associato allo stato **nascosto** del carattere, quindi il frame del carattere viene nascosto. Tuttavia, è anche possibile nascondere o visualizzare un carattere impostando la proprietà [**Visible**](visible-property.md) del carattere.

Microsoft Agent elabora in modo asincrono tutte le chiamate di animazione o *richieste*. Ciò consente al codice dell'applicazione di continuare a gestire altri eventi durante l'elaborazione della richiesta. Ad esempio, le chiamate al metodo [**Play**](play-method.md) inseriscono l'animazione in una coda per il carattere, in modo che le animazioni possano essere riprodotte in sequenza. Ciò significa tuttavia che non è possibile presupporre che una chiamata ad altre funzioni venga eseguita necessariamente dopo un'animazione che segue nel codice. Ad esempio, in genere, un'istruzione che segue una chiamata a **Play** o [**MoveTo**](moveto-method.md) verrà eseguita prima del completamento dell'animazione.

È possibile sincronizzare il codice con animazioni nella coda di un carattere creando un riferimento a un oggetto alla richiesta di animazione e, quando l'animazione viene avviata o completata, monitorando gli eventi di [richiesta](the-request-object.md) che il server usa per notificare ai client il carattere. Se, ad esempio, si desidera visualizzare una finestra di messaggio quando il carattere termina un'animazione, è possibile inserire la chiamata della finestra di messaggio nella subroutine di gestione degli eventi di [**RequestComplete**](requestcomplete-event.md) , verificando la presenza di un ID richiesta specifico.

Quando un carattere è nascosto, il server non riproduce le animazioni; Tuttavia, resta in coda ed elabora la richiesta di animazione (riproduce l'animazione) e passa di nuovo lo stato della richiesta al client. Nello stato hidden, il carattere non può diventare input-Active. Tuttavia, se l'utente pronuncia il nome del carattere (quando l'input vocale è abilitato), il server Visualizza automaticamente il carattere.

Quando l'applicazione client carica più caratteri contemporaneamente, i servizi animazione di Microsoft Agent consentono di animare i caratteri in modo indipendente o di usare i metodi [**wait**](wait-method.md), [**interrupt**](interrupt-method.md)o [**Stop**](stop-method.md) per sincronizzare l'animazione tra loro.

Microsoft Agent inoltre riproduce automaticamente altre animazioni. Se, ad esempio, lo stato del carattere non è stato modificato per diversi secondi, Agent inizia a riprodurre animazioni assegnate alle animazioni al **minimo** del carattere. Analogamente, quando l'input vocale è abilitato, Agent riproduce le animazioni di **ascolto** del carattere e quindi **Ascolta** le animazioni quando viene rilevata un'espressione. Queste animazioni gestite dal server sono denominate *Stati* e vengono definite quando viene creato un carattere. Per ulteriori informazioni, vedere [progettazione di caratteri per Microsoft Agent](agent-states.md).

 

 