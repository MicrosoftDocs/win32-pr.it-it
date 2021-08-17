---
title: Architettura del plug-in
description: Le unità biometriche espongono le funzionalità di un dispositivo al framework tramite un'interfaccia standard costituita da sensori, motori e adattatori di archiviazione.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a82f85387698f7fb80c65525004ac541a1108635ca3d929adda7b0cbb932cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411066"
---
# <a name="plug-in-architecture"></a>Architettura del plug-in

I dispositivi biometrici vengono prodotti in un'ampia gamma di tipi e configurazioni. Il Windows Biometric Framework risolve questa varietà fornendo un'architettura estendibile che consente agli sviluppatori di terze parti di creare componenti plug-in personalizzati. Il componente principale è un oggetto software denominato unità biometrica. Le unità biometriche espongono le funzionalità di un dispositivo al framework tramite un'interfaccia standard costituita da sensori, motori e adattatori di archiviazione. Le unità biometriche e i relativi componenti costitutivi sono descritti negli argomenti seguenti.

## <a name="biometric-unit"></a>Unità biometrica

Il componente centrale dell'architettura plug-in Windows Biometric Framework è l'unità biometrica, un oggetto software che espone le funzionalità di un dispositivo biometrico al framework tramite un'interfaccia standard.

A ogni unità biometrica è associato un singolo sensore fisico. Il sensore acquisisce i dati biometrici e può anche, a seconda delle funzionalità hardware, eseguire altre operazioni biometriche, ad esempio la corrispondenza dei modelli e l'archiviazione. Per eseguire queste funzioni, i sensori che non supportano l'onboard o l'archiviazione richiedono moduli software aggiuntivi. Per altre informazioni, vedere [Adapter.](/previous-versions//dd401508(v=vs.85))

La figura seguente mostra il flusso dei dati attraverso un'unità biometrica. In sostanza, il flusso di dati forma un tipo di pipeline. L'input iniziale per la pipeline è un campione biometrico acquisito da un sensore fisico. Il motore tenta di associare l'esempio ai modelli già esistenti nell'archivio modelli oppure, se non viene trovata alcuna corrispondenza, compila un nuovo modello da campioni fisici ripetuti e salva il modello nell'archivio.

![flusso di dati attraverso un'unità biometrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo di vita delle unità biometriche

### <a name="creation"></a>Creazione

All'avvio del servizio biometrico Windows o quando riceve una notifica hardware dal gestore di Plug and Play, esegue l'analisi di qualsiasi hardware che supporta il noto GUID di interfaccia \_ DEVINTERFACE \_ BIOMETRIC READER \_ (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Per ogni dispositivo biometrico individuato:

-   Apre un handle per il dispositivo.
-   Esegue query sulle funzionalità del dispositivo usando un'Windows di controllo del driver biometrico.
-   Apre la chiave del Registro di sistema del dispositivo e tenta di individuare le informazioni sui plug-in della scheda associati.
-   Apre la Windows del Registro di sistema del servizio biometrico e cerca informazioni su eventuali plug-in globali che devono eseguire l'override dei valori specifici del dispositivo trovati nel passaggio precedente.
-   Crea un'unità biometrica per rappresentare il dispositivo e passa l'unità a un provider di servizi biometrici.

### <a name="configuration"></a>Configurazione

Dopo che un provider di servizi biometrici (BSP) ha accettato un'unità biometrica, configura l'unità e la assegna a un pool di sensori. Per altre informazioni, vedere [Pool di sensori.](sensor-pools.md) L'unità viene configurata caricando le schede appropriate, connettendosi a un archivio modelli ed eventualmente modificando la modalità operativa. Un'unità biometrica può essere configurata per operare in una delle due modalità seguenti:

-   Nella modalità di base, l'unità funge da dispositivo di acquisizione semplice. Non usa l'elaborazione o l'archiviazione su scheda, ma si basa interamente su schede software per un supporto aggiuntivo. Dovrebbe essere in grado di generare esempi in un formato standard. Ad esempio, i lettori di impronte digitali devono generare campioni conformi a ANSI INCITS 381-2004. Lo scopo della modalità di base è supportare l'interoperabilità tra componenti di fornitori diversi.
-   Nella modalità avanzata, l'unità biometrica usa funzioni di elaborazione e archiviazione su scheda. Deve esporre le interfacce standard, ma può generare ed elaborare gli esempi in qualsiasi formato desiderato.

Quando un'unità biometrica viene spostata da un pool di sensori a un altro, le schede vengono scaricate e riconfigurate per il nuovo pool di sensori. L'identità dell'unità biometrica rimane costante; cambiano solo la configurazione hardware e i plug-in dell'adattatore.

### <a name="shut-down"></a>Arresta

Quando il Windows biometrico viene arrestato o quando il gestore Plug and Play notifica che un'unità è stata rimossa, il servizio elimina tutte le unità biometriche.

## <a name="adapters"></a>adapter

I componenti software plug-in denominati adattatori connettono un'unità biometrica all'hardware sottostante e forniscono eventuali funzionalità mancanti nell'hardware del sensore. È possibile creare tre tipi di adattatori:

-   Un adattatore sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di campioni e il controllo del flusso dei dati biometrici al motore di elaborazione.
-   Un adattatore motore genera modelli biometrici da esempi acquisiti, abbina esempi a modelli esistenti e indici.
-   Un adattatore di archiviazione gestisce i database modello.

Gli adapter possono essere caricati e scaricati in fase di esecuzione. Ciò consente al Windows biometrico di riconfigurare dinamicamente un'unità biometrica connetterla a un set diverso di schede.

Infine, ognuna delle interfacce del sensore, del motore e dell'adattatore di archiviazione espone due metodi, **ControlUnit** e **ControlUnitPrivileged,** che consentono alle applicazioni client di accedere alle funzionalità dell'adattatore personalizzato definite dal fornitore. In questo modo il fornitore può definire un set quasi illimitato di operazioni di controllo per un dispositivo. Inoltre, scegliendo la funzione da implementare, un fornitore può scegliere di rendere disponibili alcune operazioni di controllo agli utenti senza privilegi limitando al tempo stesso altre operazioni agli utenti con privilegi.

Per altre informazioni su come creare adattatori, vedere [Creare plug-in dell'adattatore.](creating-adapter-plug-ins.md)

## <a name="adapter-performance-requirements"></a>Requisiti di prestazioni dell'adapter

Poiché l'obiettivo è una risposta rapida complessiva, le prestazioni di un adapter non vengono specificate in termini di limiti di tempo per routine specifiche. Al contrario, le prestazioni vengono specificate come un set di requisiti per l'esperienza utente complessiva.

Esistono due requisiti:

-   Qualsiasi interazione tra l'utente e il sistema operativo che comporta la biometria deve essere completata entro due secondi. Questo intervallo misura l'ora di inizio e fine percepita dall'utente dal momento in cui tocca o scorre rapidamente il sensore fino all'ora in cui si verifica un evento visibile sullo schermo del dispositivo. Ad esempio, durante lo sblocco, non deve essere presente più di due secondi di ritardo tra il tocco o lo scorrimento del sensore di impronta digitale da parte dell'utente e la schermata di blocco che conferma l'identità dell'utente.
-   Per l'aspetto iniziale dei riquadri delle credenziali nella schermata di accesso o di blocco, è consentito un po' più di tempo (tre secondi, massimo), ma è comunque preferibile prima che successivamente. In particolare, il riquadro bio deve essere visibile sullo schermo entro tre secondi dall'aspetto del pannello di blocco o di accesso.

Questi numeri non sono arbitrari. Numerosi studi hanno dimostrato che gli esseri umani tendono a sperimentare tutto ciò che accade in un intervallo di due secondi come parte del momento "adesso". Se l'evento A e l'evento B si verificano entro due secondi l'uno dall'altro, gli utenti percepiranno tali eventi come simultanei. Se gli eventi sono separati da più di tre secondi circa, si pensa che si sia verificato un ritardo, ovvero che qualcosa sta "prendendo troppo tempo". Si tratta quindi di un problema di salute umana hardwired.

 

 