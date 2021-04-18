---
description: Con la funzione lineSetTerminal, l'applicazione può controllare o escludere il routing degli eventi di basso livello specificati (scambiati tra il commutatore e la stazione) a un dispositivo.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Routing di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307197"
---
# <a name="event-routing"></a>Routing di eventi

Con la funzione [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) , l'applicazione può controllare o escludere il routing degli eventi di basso livello specificati (scambiati tra il commutatore e la stazione) a un dispositivo. Con **lineSetTerminal**, l'applicazione specifica il terminale del dispositivo a cui vengono indirizzati questi eventi, ad esempio gli eventi di flusso multimediale di tipo riga, indirizzo o chiamata.

Il routing delle diverse classi di eventi può essere controllato singolarmente, consentendo di specificare terminali distinti per ogni classe di evento. Le classi di evento includono lampade, pulsanti, schermo, suoneria, hookswitch e flusso multimediale.

Ad esempio, il flusso multimediale di una chiamata (voce, ad esempio) può essere inviato a qualsiasi dispositivo trasduttore se il provider di servizi e l'hardware è in grado di farlo. In generale, un *trasduttore* equivale a quello definito come un dispositivo *hookswitch* in TAPI, un elemento con un microfono e un altoparlante. Gli eventi ring dallo switch al telefono possono essere mappati a un avviso visivo sullo schermo del computer oppure possono essere instradati a un dispositivo telefonico. Gli eventi LAMP e gli eventi di visualizzazione possono essere ignorati o indirizzati a un dispositivo telefonico, che sembra comportarsi come un normale set di telefono. Infine, le pressioni dei pulsanti in un dispositivo telefonico possono essere passate o meno alla riga. In ogni caso, questo routing di segnali di basso livello dalla riga non influisce sul funzionamento della parte della riga di TAPI, che esegue sempre il mapping degli eventi di basso livello all'equivalente funzionale. Per determinare i terminali disponibili in un dispositivo linea (e le relative funzionalità), consultare le funzionalità del dispositivo line con [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Si supponga inizialmente che l'applicazione abbia eliminato il routing di tutti gli eventi (con [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)) e che l'utente selezioni una cuffia come periferica di i/O corrente. Una chiamata in ingresso Invia un [**messaggio \_ CALLSTATE di riga**](line-callstate.md) e un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) con l'indicazione della *suoneria* . Poiché il routing di tutti gli eventi viene eliminato, gli eventi Ring non vengono indirizzati al telefono, quindi la suoneria viene annullata. Al contrario, l'applicazione invia una notifica all'utente con una finestra di dialogo popup e un segnale acustico di sistema nell'auricolare.

L'utente decide di rispondere alla chiamata. Poiché il dispositivo di I/O corrente dell'utente è l'auricolare, l'applicazione di telefonia richiama [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) sulla chiamata in ingresso per indirizzare il supporto della chiamata alla cuffia e rispondere alla chiamata. L'applicazione può anche richiamare **lineSetTerminal** per instradare la lampada e visualizzare gli eventi informativi al set di telefono in modo che si comporti come di consueto.

Come secondo esempio, si supponga che una chiamata in ingresso stia inviando avvisi sul computer dell'utente. Invece di selezionare l'opzione di risposta con il mouse, l'utente decide di selezionare semplicemente il telefono cellulare per rispondere alla chiamata. Lo stato Offhook al telefono invia un messaggio all'applicazione. L'applicazione può interpretare questo stato come richiesta da parte dell'utente per selezionare il telefono cellulare per condurre la conversazione. L'applicazione richiama quindi [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) per instradare i dati vocali sulla chiamata al set di telefono.

 

 



