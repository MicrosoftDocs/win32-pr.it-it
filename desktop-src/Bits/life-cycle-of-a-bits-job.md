---
title: Ciclo di vita di un processo BITS
description: Il ciclo di vita di un processo BITS inizia al momento della creazione di un processo.
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c6ac23c598d28681968e9c0cbed776ba24c57e98
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320938"
---
# <a name="bits-job-states"></a>Stati del processo BITS
Sono disponibili quattro classi di [**Stati**](/windows/desktop/api/Bits/ne-bits-bg_job_state)bits: inizio, azione, trasferiti e finale. Durante l'esecuzione di un processo, viene eseguita la transizione tra gli Stati nelle diverse classi di stato. Quando un processo è in uno stato finale, non verrà spostato dallo stato finale e non verrà visualizzato in un'enumerazione di [processi](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs).

## <a name="state-changing-methods"></a>Metodi per la modifica dello stato
Sono disponibili quattro metodi per la modifica dello stato in un processo: [**Annulla**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel), [**completa**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete), [**Riprendi**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)e [**Sospendi**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend). Se un processo non è in uno stato finale, è possibile chiamare qualsiasi metodo di modifica dello stato. 

Il metodo [**Suspend**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) viene utilizzato per passare un processo allo stato Suspended. Quando un processo viene sospeso, tutti i relativi trasferimenti vengono arrestati e non vengono ripresi fino a quando non si chiama Resume.
Un processo già sospeso rimane semplicemente sospeso.

Il metodo [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) viene usato per avviare un processo sospeso. I processi in uno stato di errore o di errore temporaneo verranno configurati per essere ripetuti. I processi attualmente in uno stato di azione resteranno in tale stato.

Il metodo [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) viene usato per annullare un processo. Lo stato passerà a annullato. Tutti i file attualmente trasferiti non verranno completati. Tutti i file completamente trasferiti e parzialmente trasferiti verranno eliminati.

Il metodo [**completo**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) terminerà un trasferimento. Verranno conservati tutti i file scaricati completamente. i file non completamente trasferiti verranno eliminati.

È necessario chiamare Annulla o completa per spostare il processo in uno stato finale ed eseguire la pulizia. I processi che non vengono passati a uno stato finale elimineranno le risorse di sistema. BITS eliminerà infine automaticamente i processi precedenti. Il valore predefinito di [JobInactivityTimeout](/windows/desktop/Bits/group-policies) consiste nell'annullare i processi dopo 90 giorni.


## <a name="starting-state"></a>Stato iniziale 
Lo stato iniziale viene **sospeso**. Da qui è possibile aggiungere file al processo e impostare le proprietà del processo e del file. Per avviare il trasferimento di un processo, chiamare Resume sul processo. Se si riprende un processo senza file, verrà restituito un codice di errore BG_E_EMPTY e il processo resterà sospeso.

## <a name="action-states"></a>Stati azione
Gli stati in **coda**, di **connessione** e di **trasferimento** mostrano l'attività interna corrente del processo. Un processo ACCODAto è pronto per essere pianificato, probabilmente in attesa dell'utilità di pianificazione BITS o in attesa dell'accesso dell'utente. Un processo che si connette sta tentando di connettersi al server per iniziare a trasferire i file. Un processo che sta trasferendo sta caricando o scaricando attivamente i file.

Lo stato di **errore temporaneo** indica che il processo ha tentato e non è riuscito a trasferire il file. Questo potrebbe essere per motivi di criteri di rete. il processo potrebbe essere bloccato perché la rete corrente è troppo costosa. Potrebbe anche essere bloccata per motivi di sistema, come il sistema in modalità di gioco o di batteria, oppure perché non è disponibile connettività Internet. 

I processi nello stato di errore temporaneo verranno ripetuti automaticamente da BITS quando appropriato. BITS include un valore [MinimumRetryDelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) da controllare quando viene eseguito un nuovo tentativo di un processo e quando BITS smette di riprovare.


## <a name="transferred-states"></a>Stati trasferiti
Gli stati trasferiti si verificano quando non è più necessario eseguire il trasferimento. È necessario annullare o completare un processo in questo stato. È anche possibile aggiungere altri file da trasferire e chiamare Resume (), ma non si tratta di una pratica comune.

Lo stato di **errore** si verifica quando viene eseguito un trasferimento (non verrà ritentato), ma non è stato completato correttamente. Tutti i file devono essere trasferiti per avere esito positivo; Se si è verificato un errore in modo permanente, il processo sarà in errore. In genere si chiamerà Annulla o completa per spostare il processo in uno stato finale. La differenza pratica è che quando si chiama Annulla, qualsiasi file trasferito correttamente viene eliminato, ma se si chiama completa, il file trasferito correttamente non verrà eliminato.

I motivi per lo stato di errore includono 
* Rimanere troppo a lungo in uno stato di errore temporaneo (oltre l'impostazione [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) ).
* Ottenere un errore di BG_E_TOKEN_REQUIRED e richiedere assistenza con i [token Helper](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs)

Si tratta di una procedura comune per riconfigurare un processo di errore, quindi chiamare Resume per ritentare il processo. Ad esempio, è possibile che l'app debba aggiornare il nome remoto di un file tramite [Seremotename](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename).

Lo stato **trasferito** si verifica quando viene eseguito un trasferimento e ha esito positivo. Per finalizzare il processo, è necessario chiamare complete. per i processi di download i file scaricati non saranno disponibili fino al termine della chiamata a complete. L'eccezione a questa regola è rappresentata dai processi che rappresentano i processi a prestazioni elevate (ed è comunque necessario chiamare complete).

## <a name="final-states"></a>Stati finali
Quando un processo è in uno stato finale, non è possibile chiamare uno dei metodi di modifica dello stato. Il processo verrà **riconosciuto** dopo la chiamata a complete () e saranno disponibili tutti i file scaricati completati. Il processo verrà **annullato** dopo la chiamata a Cancel () e tutti i file scaricati verranno eliminati. 


## <a name="life-cycle-of-a-bits-job"></a>Ciclo di vita di un processo BITS

Il ciclo di vita di un processo BITS inizia al momento della creazione di un processo. Un processo è un contenitore che contiene uno o più file da trasferire. Un processo dispone anche di proprietà che specificano il modo in cui BITS trasferisce i file e interagisce con l'applicazione. Ad esempio, è possibile specificare la priorità del processo, se il processo è un processo di caricamento o download e per quali eventi si desidera ricevere la notifica.

Dopo aver creato il processo, aggiungere uno o più file (i processi di caricamento possono contenere un solo file) al processo e modificare i valori delle proprietà in base alle esigenze dell'applicazione. Quando si aggiunge un file al processo, specificare sia il nome locale (client) che quello remoto (Server) del file. Il nome del file remoto deve usare il protocollo HTTP, HTTPS o SMB. I file all'interno di un processo vengono elaborati in sequenza (First in, First out).

BITS sospende automaticamente i processi al momento della creazione. È necessario riprendere il processo per attivarlo nella coda di trasferimento. È possibile sospendere o riprendere un processo in qualsiasi momento. Se si riprende il processo, lo stato del processo verrà spostato dallo stato sospeso allo stato in coda. Il processo rimane nello stato in coda fino a quando l'utilità di pianificazione non determina che è il turno del processo di trasferimento dei file. Tutti i processi in primo piano vengono eseguiti simultaneamente con un processo in background. BITS elabora in modo seriale i file all'interno dei processi in primo piano.

Quando è il turno di un processo di trasferimento dei file, il processo passa allo stato di connessione mentre BITS si connette al server remoto (specificato nel nome file remoto). Se BITS è in grado di connettersi al server remoto, il processo passa allo stato trasferente, dove rimane fino al termine del periodo di tempo, il trasferimento è completo, si verifica un errore o l'applicazione sospende il processo.

Il processo viene spostato tra gli stati in coda, la connessione e il trasferimento fino a quando BITS non trasferisce tutti i file nel processo. A questo punto, il processo passa allo stato trasferito. BITS usa la pianificazione Round Robin per pianificare processi con lo stesso livello di priorità. A ogni processo viene assegnata una sezione di tempo per elaborare i file. Se il processo non viene completato durante l'intervallo di tempo, il processo torna allo stato in coda e il processo successivo nella coda viene attivato. Ciò impedisce ai processi di grandi dimensioni di bloccare i processi più piccoli. I processi vengono elaborati in gran parte su una base FIFO (First in, First out); BITS, tuttavia, non può garantire l'elaborazione FIFO a causa della pianificazione Round Robin, degli errori di processo e dei riavvii del servizio.

I file trasferiti non sono disponibili per il client finché l'applicazione non chiama il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) per trasferire la proprietà dei file da BITS all'utente. I processi di caricamento vengono inoltre impostati sullo stato trasferito quando il file viene ricevuto correttamente dal server. I processi di caricamento-risposta vengono impostati sullo stato trasferito dopo che il file è stato inviato correttamente al server e la risposta dall'applicazione server è stata trasferita al client.

Se si verifica un errore, il processo si sposta in uno stato di errore irreversibile o temporaneo. Gli errori irreversibili sono errori che non possono essere ripristinati da o che richiedono un intervento da risolvere. Se l'applicazione è in grado di correggere l'errore, l'applicazione riprende il processo e BITS sposta il processo nello stato in coda. Gli errori temporanei sono errori che possono risolversi autonomamente. BITS ritenta i processi nello stato di errore temporaneo fino a quando il trasferimento non riesce o si verifica il timeout del processo. Si verifica il timeout del processo quando non viene eseguito alcun avanzamento entro il periodo specificato dall'applicazione. Se il processo scade, BITS sposta il processo in stato di errore irreversibile.

Per ulteriori informazioni sugli stati dei processi, vedere la pagina relativa [**\_ \_ allo stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state).
