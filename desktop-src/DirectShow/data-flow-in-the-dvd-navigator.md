---
description: Flusso di dati nel navigatore DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Flusso di dati nel navigatore DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747426"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Flusso di dati nel navigatore DVD

Il navigatore DVD dispone di metodi per arrestare e sospendere la riproduzione. Questi metodi sono simili, ma non identici, ai metodi **Stop** e **pause** in [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Di seguito è illustrata la differenza tra di essi:

-   I metodi **IDVDControl2** modificano gli elementi letti dal navigatore DVD dal disco. Non cambiano lo stato del grafico.
-   I metodi **IMediaControl** modificano lo stato del grafico. Non modificano le letture di DVD Navigator dal disco. (È presente un'eccezione importante, illustrata nella sezione successiva, correlata al metodo **Stop** ).

Ad esempio, [**IDVDControl2::P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) metodo esegue il comando Annex J "pause \_ on", ma non sospende il grafico del filtro. Il metodo [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) , d'altra parte, mette in pausa il grafo ma non emette alcun comando DVD.

In generale, usare i metodi **IMediaControl::P ause** e **Stop** anziché i metodi **IDVDControl2** corrispondenti. I metodi **IMediaControl** hanno latenze molto piccole, mentre i metodi **IDVDControl2** possono avere fino a due secondi di latenza.

Arresto della riproduzione

Il comportamento di [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) dipende da un flag che è possibile impostare con il metodo [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

-   Se il \_ flag DVD ResetOnStop è **false**, **IMediaControl:: Stop** arresta il grafo, ma non modifica il dominio del navigatore DVD. Quando si chiama di nuovo l'esecuzione, la riproduzione riprende dalla posizione corrente.
-   Se \_ il DVD ResetOnStop è **true**, **IMediaControl:: Stop** causa la reimpostazione del navigatore DVD. Quando si chiama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , il NAVIGAtore DVD viene riprodotto dal primo dominio di riproduzione, come se si stesse inserendo il DVD per la prima volta.

Il \_ flag RESETONSTOP DVD è **true** per impostazione predefinita, per compatibilità con le applicazioni meno recenti. In genere, tuttavia, è necessario eseguire l'override dell'impostazione predefinita e impostare il flag su **false**. Il motivo è che alcuni eventi possono causare l'arresto del grafico durante la riproduzione. Se, ad esempio, la risoluzione dello schermo viene modificata, il grafico di filtro si interrompe, riconnette il renderer video e viene riavviato. Se \_ il DVD ResetOnStop è **true**, la riproduzione verrà riavviata dall'inizio del disco. Probabilmente non è quello previsto dall'utente.

All'inizio dell'applicazione, quindi, chiamare **seoption** con DVD \_ ResetOnStop impostato su **false**. Se si desidera arrestare la riproduzione e riprenderla dallo stesso percorso, chiamare **IMediaControl:: Stop** o **IMediaControl::P ause**. Se si desidera arrestare la riproduzione e reimpostare il disco, chiamare la funzione **SetOption** con DVD \_ ResetOnStop uguale a **true**, quindi chiamare **IMediaControl:: Stop**, infine chiamare nuovamente la funzione **SetOption** e reimpostare DVD \_ ResetOnStop su **false**.

Sospensione della riproduzione

Se si assegna al navigatore DVD un comando quando il grafico è sospeso, il comando potrebbe non essere completato fino a quando il grafico non viene più eseguito. In alcune situazioni, questo può causare un deadlock nell'applicazione. Per evitare deadlock, è necessario seguire due regole:

-   In pausa, non eseguire più di un comando DVD asincrono.
-   Durante la pausa, non bloccare il thread dell'interfaccia utente dell'applicazione o il thread che modifica lo stato del grafico.

La seconda regola vale la pena esaminare in modo più dettagliato. Di seguito sono riportati alcuni scenari specifici che possono causare un deadlock:

-   **Scenario**: durante la pausa, l'applicazione emette un comando DVD con il flag di blocco. Questo può causare un deadlock se il thread che emette il comando DVD è lo stesso thread che rilascia il comando Run. Il comando DVD si blocca fino a quando non viene eseguito il grafo, ma il grafico non può essere eseguito fino al completamento del comando.

    **Raccomandazione**: eseguire il comando DVD su un thread di lavoro separato oppure non usare il flag di blocco.

-   **Scenario**: durante la pausa, l'applicazione esegue un comando DVD, quindi chiama [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) sull'oggetto Command. Questa situazione è equivalente all'esempio precedente. Se si chiama **wait** dal thread UI, il thread dell'interfaccia utente non può eseguire il grafo finché il metodo **wait** non viene sbloccato, ma il metodo **wait** non viene sbloccato fino a quando non viene eseguito il grafo.

    **Raccomandazione**: chiamare **wait** su un thread di lavoro.

-   **Scenario**: durante l'esecuzione del grafo, l'applicazione emette un comando DVD con il flag di blocco e quindi chiama pause da un altro thread. Si tratta di un possibile race condition perché il grafo può essere sospeso prima dell'emissione del comando. Se uno dei due thread è il thread dell'interfaccia utente, è possibile che si verifichi un deadlock simile ai due esempi precedenti. In questo esempio viene illustrata l'importanza della scrittura di codice thread-safe se l'applicazione utilizza più thread.

    **Suggerimento**: se si usano i thread di lavoro, assicurarsi che il codice sia thread-safe.

-   **Scenario**: durante la pausa, l'applicazione Disabilita il comando Run dall'interfaccia utente e quindi emette un comando DVD asincrono. Questo caso non è esclusivamente un deadlock, perché il thread dell'applicazione è ancora in esecuzione. Tuttavia, a questo punto l'utente non è in grado di eseguire il grafo, quindi il comando non verrà mai completato.

    **Suggerimento**: quando si sospende, lasciare sempre il comando Run attivato.

Ricerca di un DVD a un'ora specificata

Per cercare in modo accurato a un'ora specificata su un disco, chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Chiamare quindi [**IDVDControl2::P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), specificando l'ora e l'impostazione di *dwFlags* su DVD \_ comando di \_ \_ scaricamento del flag.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



