---
description: In questo argomento viene fornita una revisione di alto livello delle operazioni di TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Ciclo di vita di un provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830bc16ca606bb5bd38c4bce7c1e6e39dadb65a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552641"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Ciclo di vita di un provider di servizi di telefonia

In questo argomento viene fornita una revisione di alto livello delle operazioni di TSP.

Una sessione è il tempo durante il quale una particolare configurazione rimane valida e vengono eseguite operazioni di telefonia. Un provider di servizi può supportare molte sessioni tra il momento in cui viene caricato per la prima volta e il momento in cui viene finalmente liberato. Per ogni sessione, TAPI negozia la versione dell'interfaccia, avvia la sessione, esegue le operazioni e infine arresta la sessione. Il provider di servizi non deve conservare le informazioni da una sessione a quella successiva.

Quando la versione dell'interfaccia è nota, TAPI chiama la funzione [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) per impostare tutti i parametri operativi. Il provider di servizi garantisce che tutte le informazioni di configurazione nel registro di sistema siano stabili quando viene chiamata la funzione **TSPI \_ providerInit** . La maggior parte dei provider di servizi legge tutte le informazioni di configurazione in quel momento.

Le normali operazioni possono continuare in qualsiasi ordine, dopo l'inizializzazione del provider di servizi.

TAPI negozia le informazioni specifiche del dispositivo in base ai singoli dispositivi. TAPI e il provider di servizi vengono sottoposte a commit in una versione all'apertura di un dispositivo.

Il provider di servizi può ricevere richieste per selezionare e annullare le versioni delle estensioni. Quando si seleziona una versione di estensione, il dispositivo funziona rigorosamente in base alla versione specifica del dispositivo.

La negoziazione di una versione di estensione specifica del dispositivo può essere eseguita più volte, sia prima che dopo l'apertura del dispositivo. TAPI passa un intervallo di versioni e il provider di servizi sceglie e restituisce un valore da questo intervallo. In genere, il provider di servizi dispone di estensioni specifiche del dispositivo disabilitate.

Questo consente di eseguire il commit sia di TAPI che del provider di servizi in modo che operi a tale livello di versione dell'estensione fino a quando la selezione non Nel momento in cui un'estensione specifica del dispositivo è attiva, un tentativo di negoziare un livello di versione dell'estensione deve consentire solo il livello di versione attualmente attivo. Dopo che l'estensione specifica del dispositivo è stata annullata, è possibile negoziare e selezionare una versione diversa.

Nella figura seguente sono illustrate le operazioni telefoniche all'interno della coppia di **apertura/chiusura** . Alcune di queste operazioni sono sincrone, altre sono asincrone. Se un'operazione viene completata in modo asincrono, è possibile richiedere un'altra operazione prima del completamento del primo report. Pertanto, le operazioni possono sovrapporsi in qualsiasi modo. Il provider di servizi deve infine segnalare il completamento di qualsiasi operazione asincrona richiesta. La chiusura di un telefono impone il completamento delle operazioni asincrone in attesa (probabilmente con indicazione "errore").

Il ciclo di vita per i dispositivi linea è simile al ciclo di vita per i telefoni, ad eccezione del fatto che le linee includono procedure di negoziazione, inizializzazione, apertura e chiusura personalizzate. Le operazioni sulle righe aperte sono racchiuse tra parentesi quadre per la propria coppia di **apertura/chiusura** . Questa coppia è a sua volta racchiusa tra la stessa coppia di **inizializzazione/arresto** del telefono **aperto/chiuso**.

I cicli di vita delle chiamate sono racchiusi tra parentesi quadre tra l' **apertura e la chiusura** della linea che li contiene. La durata delle chiamate può iniziare in diversi modi:

-   Richiesto da TAPI attraverso funzioni quali [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)o [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference).
-   Originato spontaneamente nel provider di servizi come nuove chiamate in ingresso, chiamate avviate dall'utente su un telefono collegato o chiamate generate come effetto collaterale di altre operazioni, ad esempio l'inserimento di una chiamata esistente in attesa.

Le durate delle chiamate distinte all'interno della stessa riga possono sovrapporsi in qualsiasi modo. Tutte le chiamate terminano la loro durata nel momento in cui viene richiamata la funzione TSPI [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Il ciclo di vita di diverse chiamate è illustrato nella figura seguente.

![cicli di vita delle chiamate sovrapposte](images/modell.png)

Una chiamata può provenire in TAPI, come illustrato con la coppia **MakeCall/CloseCall** . Una chiamata può inoltre provenire dal provider di servizi. Il provider di servizi annuncia questa operazione con un messaggio di [**riga \_ NEWCALL**](line-newcall.md) a una procedura di callback fornita da TAPI. In tal caso, TAPI restituisce il relativo identificatore per la chiamata, incluso nei callback successivi che segnalano gli eventi che si verificano sulla chiamata. Nel caso di chiamate la cui durata ha origine in TAPI, questo identificatore è incluso nell'operazione TSPI che crea la chiamata.

Tutte le operazioni che avviano la durata di una chiamata a TAPI e provider di servizi scambiano gli identificatori per la nuova chiamata. Nel caso di chiamate originate da TAPI, TAPI passa il relativo identificatore e riceve l'identificatore del provider di servizi come parametro restituito. Nel caso in cui la chiamata ha origine nel provider di servizi, il provider di servizi passa il relativo identificatore a TAPI e riceve l'identificatore TAPI come parametro restituito.

La figura seguente offre una visualizzazione di alto livello dell'installazione, della configurazione e della rimozione del provider di servizi; sequenze del ciclo di vita che si estendono su più sessioni. Il ciclo di vita tipico per queste operazioni può essere visualizzato con la seguente sequenza temporale.

![installazione, configurazione e rimozione del provider di servizi](images/model2.png)

Viene visualizzato il ciclo di vita tipico di installazione e rimozione, che si estende su più sessioni. Le chiamate alle procedure di **installazione** e [**rimozione**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) sono strettamente abbinate e non si sovrappongono. Le chiamate alla procedura di **configurazione** possono verificarsi più volte all'interno di questa coppia. Una viene in genere eseguita dal provider di servizi come effetto collaterale interno della procedura di **installazione** per creare voci di riga e telefono. È possibile chiamare la procedura di **configurazione** in altri momenti per modificare un'installazione esistente. È necessario eseguire la procedura di **installazione** prima che sia consentita qualsiasi altra funzione TSPI. Nello scenario ideale, tutte le sessioni sono strettamente annidate all'interno della coppia di procedure di **installazione/rimozione** .

Le funzioni [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)e [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagiscono con il provider di servizi stesso invece che con qualsiasi dispositivo specifico. Interessano le informazioni di configurazione statiche che sopravvivono tra più sessioni e che devono essere presenti per continuare l'operazione. Tutte le altre operazioni sono quindi annidate tra la chiamata di **TSPI \_ providerInstall** e il completamento del corrispondente **TSPI \_ providerRemove**. Queste due operazioni si verificano in genere molto distanti, molto probabilmente in un carico diverso del provider di servizi o in un altro avvio del computer. La chiamata della funzione **config** esternamente è facoltativa, perché la procedura di **installazione** è necessaria per includere il comportamento di **configurazione** in aggiunta a se stesso. Il motivo per cui viene chiamato esternamente è la modifica di una configurazione esistente.

Esiste una sottigliezza incorporata nel concetto di completamento di un'operazione [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) . È consigliabile consentire all'utente di eseguire l'utilità pannello di controllo di telefonia fornita con il servizio di telefonia per modificare le configurazioni del provider di servizi, anche quando sono in corso operazioni di telefonia (sessioni). Di conseguenza, entrambe le specifiche [**TSPI \_ ProviderConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) e **TSPI \_ providerRemove** consentono la chiamata mentre esiste una sessione in attesa. Tuttavia, le modifiche apportate alla configurazione devono essere posticipate fino a quando le operazioni di telefonia non vengono arrestate e riavviate. Pertanto, in modo rigoroso, il completamento di qualsiasi operazione **TSPI \_ ProviderConfig** o **TSPI \_ providerRemove** si verifica all'esterno di qualsiasi sessione. L'annidamento delle azioni è illustrato nella figura, anche se le chiamate alle procedure possono apparire in un ordine leggermente diverso. È consentito a un provider di servizi di non consentire semplicemente la **configurazione** o la [**rimozione**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) mentre sono in corso le operazioni, sebbene l'utente debba ricevere una notifica con una finestra di dialogo. È preferibile un'implementazione più intuitiva che consenta almeno un subset di operazioni.

Queste operazioni di **installazione**, **configurazione** e [**rimozione**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) hanno tutti l'effetto collaterale di segnalare qualsiasi applicazione di telefonia in esecuzione, il che comporta la chiusura dell'uso del servizio di telefonia. Insieme, termina tutte le sessioni in sospeso per i provider di servizi. Ciò significa che i provider di servizi devono leggere la nuova configurazione del registro di sistema quando iniziano nuove sessioni. Tutte le modifiche in sospeso dovute a una **configurazione** o a una [**rimozione**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) mentre erano in corso le operazioni diventano effettive.

 

 
