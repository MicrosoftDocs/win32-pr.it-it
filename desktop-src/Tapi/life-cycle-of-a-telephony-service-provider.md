---
description: In questo argomento viene fornita una revisione di alto livello delle operazioni TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Ciclo di vita di un provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012703"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Ciclo di vita di un provider di servizi di telefonia

In questo argomento viene fornita una revisione di alto livello delle operazioni TSP.

Una sessione è il tempo durante il quale una particolare configurazione rimane valida e vengono eseguite operazioni di telefonia. Un provider di servizi può supportare molte sessioni tra il momento in cui viene caricato per la prima volta e il momento in cui viene infine liberato. Per ogni sessione, TAPI negozia la versione dell'interfaccia, avvia la sessione, esegue operazioni e infine la arresta. Il provider di servizi non deve conservare le informazioni da una sessione alla successiva.

Una volta nota la versione dell'interfaccia, TAPI chiama la [**funzione \_ providerInit TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) per impostare tutti i parametri operativi. Il provider di servizi garantisce che tutte le informazioni di configurazione nel Registro di sistema siano stabili quando viene chiamata la **funzione \_ providerInit TSPI.** La maggior parte dei provider di servizi legge tutte le informazioni di configurazione in quel momento.

Le normali operazioni possono procedere in qualsiasi ordine, dopo l'inizializzazione del provider di servizi.

TAPI negozia le informazioni specifiche del dispositivo in base al dispositivo. TAPI e il provider di servizi emettono il commit in una versione all'apertura di un dispositivo.

Il provider di servizi può ricevere richieste di selezione e annullamento delle versioni dell'estensione. Mentre è selezionata una versione dell'estensione, il dispositivo funziona esclusivamente in base alla versione dell'estensione specifica del dispositivo.

La negoziazione di una versione dell'estensione specifica del dispositivo può verificarsi più volte, sia prima che dopo l'apertura del dispositivo. TAPI passa un intervallo di versioni e il provider di servizi sceglie e restituisce un valore da questo intervallo. In genere, le estensioni specifiche del dispositivo sono disabilitate nel provider di servizi.

In questo modo viene eseguito il commit sia di TAPI che del provider di servizi per operare a tale livello di versione dell'estensione fino a quando la selezione non viene annullata. Durante il periodo in cui è in vigore un'estensione specifica del dispositivo, un tentativo di negoziare un livello di versione dell'estensione deve consentire solo il livello di versione attualmente attivo. Dopo l'annullamento dell'estensione specifica del dispositivo, è possibile negoziare e selezionare una versione diversa.

Telefono operazioni all'interno **della coppia Apri/Chiudi** sono illustrate nella figura seguente. Alcune di queste operazioni sono sincrone, altre sono asincrone. Se un'operazione viene completata in modo asincrono, è possibile che venga richiesta un'altra operazione prima che la prima segnala il completamento. Le operazioni possono quindi sovrapporsi in qualsiasi modo. Il provider di servizi deve infine segnalare il completamento per qualsiasi operazione asincrona richiesta. La chiusura di un telefono forza il completamento delle operazioni asincrone in sospeso (possibilmente con un'indicazione di "errore").

Il ciclo di vita per i dispositivi line è simile al ciclo di vita per i telefoni, ad eccezione del fatto che le linee hanno procedure specifiche di negoziazione, inizializzazione, apertura e chiusura. Le operazioni su righe aperte sono racchiuse tra parentesi quadre in base alla **propria coppia Apri/Chiudi.** Questa coppia è a sua volta racchiusa tra parentesi quadre tra la stessa coppia **inizializzazione/arresto** del telefono **Apri/Chiudi**.

I cicli di vita delle chiamate sono racchiusi tra parentesi quadre tra **l'apertura e** la chiusura della riga che le contiene. La durata delle chiamate può iniziare in diversi modi:

-   Richiesto da TAPI tramite funzioni come [**lineMakeCall,**](/windows/win32/api/tapi/nf-tapi-linemakecall) [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)o [**lineSetupConference.**](/windows/win32/api/tapi/nf-tapi-linesetupconference)
-   Originate dal provider di servizi come nuove chiamate in ingresso, chiamate avviate dall'utente su un telefono collegato o chiamate generate come effetto collaterale di altre operazioni, ad esempio l'inserimento di una chiamata esistente in attesa.

Le durate delle chiamate distinte all'interno della stessa riga possono sovrapporsi in qualsiasi modo. Tutte le chiamate terminano la loro durata nel momento in cui viene richiamata la funzione [**TSPI \_ lineCloseCall.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) Il ciclo di vita di diverse chiamate è illustrato nella figura seguente.

![cicli di vita delle chiamate sovrapposte](images/modell.png)

Una chiamata può avere origine in TAPI, come illustrato nella **coppia MakeCall/CloseCall.** Una chiamata può avere origine anche nel provider di servizi. Il provider di servizi lo annuncia con un [**messaggio LINE \_ NEWCALL**](line-newcall.md) a una routine di callback fornita da TAPI. In tal caso, TAPI restituisce il relativo identificatore per la chiamata, incluso nei callback successivi che segnalano gli eventi che si verificano nella chiamata. Nel caso di chiamate la cui durata ha origine in TAPI, questo identificatore è incluso nell'operazione TSPI che crea la chiamata.

Tutte le operazioni che avviano la durata di una chiamata comportano lo scambio di identificatori TAPI e del provider di servizi per la nuova chiamata. Nel caso di chiamate originate da TAPI, TAPI passa il relativo identificatore e riceve l'identificatore del provider di servizi come parametro restituito. Nel caso in cui la chiamata ha origine nel provider di servizi, il provider di servizi passa il relativo identificatore a TAPI e riceve l'identificatore TAPI come parametro restituito.

La figura seguente offre una visualizzazione di alto livello dell'installazione, della configurazione e della rimozione del provider di servizi. sequenze del ciclo di vita che si estendono su più sessioni. Il ciclo di vita tipico per queste operazioni può essere visualizzato con la seguente linea temporale.

![installazione, configurazione e rimozione del provider di servizi](images/model2.png)

Viene visualizzato il ciclo di vita tipico di installazione e rimozione, che si estende su più sessioni. Le chiamate alle **procedure Install** [**e Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) sono strettamente abbinate e non si sovrappongono. Le chiamate alla **procedura config** possono essere effettuate più volte all'interno di questa coppia. Una viene in genere eseguita dal provider di servizi come effetto collaterale interno della procedura **di** installazione per creare voci di linea e telefono. La **procedura config** può essere chiamata in altri momenti per modificare un'installazione esistente. La **procedura di** installazione deve essere eseguita prima che qualsiasi altra funzione TSPI sia consentita. Nello scenario ideale, tutte le sessioni sono rigorosamente annidate all'interno della coppia di procedure **Install/Remove.**

Le funzioni [**provider \_ TSPIInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**provider \_ TSPIConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)e [**provider \_ TSPIRimuovi**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagiscono con il provider di servizi stesso anziché con qualsiasi dispositivo specifico. Influiscono sulle informazioni di configurazione statiche che non sono presenti in più sessioni e devono essere presenti per poter continuare con qualsiasi altra operazione. Tutte le altre operazioni vengono quindi annidate tra la chiamata di **provider \_ TSPIInstall** e il completamento del **provider TSPI \_ corrispondenteRimuovi**. Queste due operazioni vengono in genere eseguite molto distanti, molto probabilmente in un carico diverso del provider di servizi o in un avvio diverso del computer. La chiamata **esterna della** funzione Config è facoltativa, perché la procedura **install** è necessaria per includere il comportamento **config** oltre al proprio. Il motivo consueto per chiamare il metodo esternamente è la modifica di una configurazione esistente.

Nel concetto di completamento di un'operazione TSPI providerRemove è incorporata [**\_ una sottigliezza.**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) È consigliabile consentire all'utente di eseguire l'utilità di telefonia Pannello di controllo fornita con il servizio di telefonia per modificare le configurazioni del provider di servizi, anche quando sono in corso operazioni di telefonia (sessioni). Di conseguenza, entrambe le [**specifiche \_ providerConfig e**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) **TSPI \_ providerRemove** consentono la chiamata mentre è presente una sessione in sospeso. Tuttavia, tutte le modifiche alla configurazione devono essere posticipate fino a quando le operazioni di telefonia non vengono arrestate e riavviate. Pertanto, in senso stretto, il completamento di qualsiasi **\_ operazione TSPI providerConfig** o **TSPI \_ providerRemove** avviene all'esterno di qualsiasi sessione. L'annidamento delle azioni è come illustrato nella figura, anche se le chiamate alle procedure possono apparire in un ordine leggermente diverso. È consentito a un provider di  servizi di non consentire semplicemente Config o [**Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) mentre sono in corso operazioni, anche se l'utente deve ricevere una notifica con una finestra di dialogo. È preferibile un'implementazione più semplice che consenta almeno un subset di operazioni.

Tutte queste operazioni **Install,** **Config** e [**Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) hanno l'effetto collaterale di segnalare eventuali applicazioni di telefonia in esecuzione, determinando l'arresto dell'uso del servizio di telefonia. Insieme, tutte le sessioni in sospeso per i provider di servizi terminano. Ciò significa che i provider di servizi devono leggere la nuova configurazione del Registro di sistema all'inizio di nuove sessioni. Tutte le modifiche in sospeso a causa di una **configurazione o** [**di una**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) rimozione durante l'esecuzione delle operazioni hanno effetto.

 

 
