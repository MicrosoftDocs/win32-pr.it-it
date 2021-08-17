---
description: Dati Flow nello strumento di spostamento DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Dati Flow nello strumento di spostamento DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e649edfacf0a1fad56cfbe8e73a5e1e9aaf099b9c17463858bf776ab06605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953360"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Dati Flow nello strumento di spostamento DVD

Lo strumento di spostamento DVD dispone di metodi per arrestare e sospendere la riproduzione. Questi metodi sono simili, ma non identici, ai metodi **Stop** **e Pause** in [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) Ecco la differenza tra di essi:

-   I **metodi IDvdControl2** modificano ciò che lo strumento di spostamento DVD legge dal disco. Non modificano lo stato del grafico.
-   I **metodi IMediaControl** modificano lo stato del grafico. Non modificano ciò che lo strumento di navigazione DVD legge dal disco. Esiste un'eccezione importante, illustrata nella sezione successiva, relativa al **metodo Stop.**

Ad esempio, [**il metodo IDvdControl2::P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) esegue il comando "Pause On" dell'allegato J, ma non sospende \_ il grafico dei filtri. Il [**metodo IMediaControl::P ause,**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) d'altra parte, sospende il grafico ma non esegue alcun comando DVD.

In generale, usare **i metodi IMediaControl::P ause** e **Stop** anziché i metodi **IDvdControl2** corrispondenti. I **metodi IMediaControl** hanno latenze molto piccole, mentre i metodi **IDvdControl2** possono avere fino a due secondi di latenza.

Arresto della riproduzione

Il comportamento di [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) dipende da un flag che è possibile impostare con il [**metodo IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

-   Se il flag ResetOnStop del DVD è \_ **FALSE,** **IMediaControl::Stop** arresta il grafico, ma non modifica il dominio dello strumento di navigazione dvd. Quando si chiama run di nuovo, la riproduzione riprende dalla posizione corrente.
-   Se DVD \_ ResetOnStop è **TRUE,** **IMediaControl::Stop** causa la reimpostazione dello strumento di navigazione DVD. Quando si chiama [**di nuovo IMediaControl::Run,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) lo strumento di spostamento DVD viene riprodotto dal dominio First Play, come se si inseriva il DVD per la prima volta.

Il flag \_ DVD ResetOnStop è **TRUE** per impostazione predefinita, per compatibilità con le applicazioni meno recenti. In genere, tuttavia, è consigliabile eseguire l'override del valore predefinito e impostare il flag su **FALSE.** Il motivo è che determinati eventi possono causare l'arresto del grafico durante la riproduzione. Ad esempio, se la risoluzione dello schermo cambia, il grafico dei filtri si arresta, riconnette il renderer video e si riavvia. Se \_ l'opzione DVD ResetOnStop è impostata su **TRUE,** la riproduzione verrà riavviata dall'inizio del disco. Probabilmente non è ciò che l'utente si aspetta.

All'inizio dell'applicazione, quindi, chiamare **SetOption** con DVD \_ ResetOnStop impostato su **FALSE.** Se si vuole arrestare la riproduzione e riprenderla dalla stessa posizione, chiamare **IMediaControl::Stop** o **IMediaControl::P ause.** Se si vuole arrestare la riproduzione e reimpostare il disco, chiamare **SetOption** con DVD ResetOnStop uguale a TRUE, quindi chiamare \_ **IMediaControl::Stop.** Infine, chiamare di nuovo **SetOption** e reimpostare DVD  \_ ResetOnStop su **FALSE.**

Sospensione della riproduzione

Se si assegna allo strumento di navigazione DVD un comando mentre il grafico è in pausa, il comando potrebbe non essere completato fino a quando il grafico non viene eseguito di nuovo. In alcune situazioni, ciò può causare un deadlock nell'applicazione. Esistono due regole da seguire per evitare deadlock:

-   Durante la sospensione, non eseguire più di un comando DVD asincrono.
-   Durante la sospensione, non bloccare il thread dell'interfaccia utente dell'applicazione o il thread che modifica lo stato del grafico.

La seconda regola vale la pena esaminare in modo più dettagliato. Ecco alcuni scenari specifici che possono causare un deadlock:

-   **Scenario:** mentre è in pausa, l'applicazione esende un comando DVD con il flag di blocco. Ciò può causare un deadlock se il thread che esegue il comando DVD è lo stesso thread che esegue il comando run. Il comando DVD si blocca fino all'esecuzione del grafo, ma il grafo non può essere eseguito fino al completamento del comando.

    **Raccomandazione:** eseguire il comando DVD in un thread di lavoro separato o non usare il flag di blocco.

-   **Scenario:** mentre è in pausa, l'applicazione esende un comando DVD, quindi chiama [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) sull'oggetto comando. Questa situazione è equivalente all'esempio precedente. Se si chiama **Wait** dal thread dell'interfaccia utente, il thread dell'interfaccia utente non può eseguire il grafico fino a quando il **metodo Wait** non viene sbloccato, ma il metodo **Wait** non si sblocca fino all'esecuzione del grafico.

    **Raccomandazione:** chiamare **Wait** su un thread di lavoro.

-   **Scenario:** durante l'esecuzione del grafo, l'applicazione esegue un comando DVD con il flag di blocco e quindi chiama pause da un altro thread. Si tratta di una possibile race condition perché il grafico può essere sospeso prima dell'esecuzione del comando. Se uno dei due thread è il thread dell'interfaccia utente, è possibile che si sia causato un deadlock simile ai due esempi precedenti. Questo esempio illustra l'importanza della scrittura di codice thread-safe se l'applicazione usa più thread.

    **Raccomandazione:** se si usano thread di lavoro, assicurarsi che il codice sia thread-safe.

-   **Scenario:** mentre è in pausa, l'applicazione disabilita il comando esegui dall'interfaccia utente e quindi esegue un comando DVD asincrono. Questo caso non è strettamente un deadlock, perché il thread dell'applicazione è ancora in esecuzione. Tuttavia, all'utente viene ora impedito di eseguire il grafo e pertanto il comando non verrà mai completato.

    **Raccomandazione:** in caso di sospensione, lasciare sempre abilitato il comando esegui.

Ricerca di un DVD a un'ora specificata

Per cercare in modo accurato un'ora specificata su un disco, chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Chiamare quindi [**IDvdControl2::P layAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), specificando l'ora e *impostando dwFlags* su DVD \_ CMD FLAG \_ \_ Flush.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



