---
description: Con la funzione lineSetTerminal, l'applicazione può controllare o eliminare il routing di eventi di basso livello specificati (spostati tra il commutatore e la stazione) a un dispositivo.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Routing di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c71d07994090a1e68fcbadd1cd3b686a3de316e4a6fd01cca506fcdbcdbd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763097"
---
# <a name="event-routing"></a>Routing di eventi

Con la [**funzione lineSetTerminal,**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) l'applicazione può controllare o eliminare il routing di eventi di basso livello specificati (spostati tra il commutatore e la stazione) a un dispositivo. Con **lineSetTerminal,** l'applicazione specifica il dispositivo terminale a cui vengono indirizzati questi eventi, ad esempio riga, indirizzo o chiamata di eventi di flusso multimediale.

Il routing delle diverse classi di eventi può essere controllato singolarmente, consentendo di specificare terminali separati per ogni classe di evento. Le classi di evento includono lampioni, pulsanti, visualizzazione, ringer, hookswitch e flusso multimediale.

Ad esempio, il flusso multimediale di una chiamata (voce, ad esempio) può essere inviato a qualsiasi dispositivo trasduttore se il provider di servizi e l'hardware sono in grado di farlo. In generale, un *trasduttore* è uguale a quello che viene definito un dispositivo *hookswitch* in TAPI, un elemento che ha un microfono e un altoparlante. Gli eventi dell'anello dal commutatore al telefono possono essere mappati a un avviso visivo sullo schermo del computer o possono essere instradati a un dispositivo telefonico. Gli eventi lamp e gli eventi di visualizzazione possono essere ignorati o indirizzati a un dispositivo telefonico (che sembra comportarsi come un normale set di telefoni). Infine, la pressione di un pulsante su un dispositivo telefonico può essere passata o meno alla linea. In ogni caso, questo routing dei segnali di basso livello dalla linea non influisce sul funzionamento della parte di linea di TAPI, che esegue sempre il mapping degli eventi di basso livello al relativo equivalente funzionale. Per determinare i terminali di un dispositivo line disponibili (e le relative funzionalità), vedere le funzionalità del dispositivo line con [**lineGetDevCaps.**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)

Si supponga inizialmente che l'applicazione abbia eliminato il routing di tutti gli eventi (con [**lineSetTerminal)**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)e che l'utente seleziona un visore VR come dispositivo di I/O corrente. Una chiamata in ingresso invia un [**messaggio LINE \_ CALLSTATE**](line-callstate.md) e un [**messaggio LINE \_ LINEDEVSTATE**](line-linedevstate.md) con l'indicazione *di* anello. Poiché il routing di tutti gli eventi viene eliminato, gli eventi di anello non vengono instradati al telefono, quindi l'anello viene eliminato. Al contrario, l'applicazione invia una notifica all'utente con una finestra di dialogo popup e un segnale acustico del sistema nel visore VR.

L'utente decide di rispondere alla chiamata. Poiché il dispositivo di I/O corrente dell'utente è il visore VR, l'applicazione di telefonia richiama [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) sulla chiamata in ingresso per instradare i supporti della chiamata al visore VR e rispondere alla chiamata. L'applicazione può anche richiamare **lineSetTerminal** per instradare lamp e visualizzare gli eventi in informazioni al set di telefoni in modo che si comporti come di consueto.

Come secondo esempio, si supponga che una chiamata in ingresso avvisi sul computer dell'utente. Invece di selezionare l'opzione di risposta con il mouse, l'utente decide di riprendere il telefono per rispondere alla chiamata. Lo stato dell'offhook al telefono invia un messaggio all'applicazione. L'applicazione può interpretare questo stato come una richiesta da parte dell'utente di selezionare il telefono cellulare per condurre la conversazione. L'applicazione richiama quindi [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) per instradare i dati vocali della chiamata al set di telefoni.

 

 



