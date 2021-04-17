---
title: Architettura plug-in
description: Le unità biometriche espongono le funzionalità di un dispositivo al Framework tramite un'interfaccia standard costituita da sensori, motore e adattatori di archiviazione.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e43af9c0ea5a8db57cc0e0970b5625b1ba118f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473710"
---
# <a name="plug-in-architecture"></a>Architettura plug-in

I dispositivi biometrici sono prodotti in un'ampia gamma di tipi e configurazioni. Il Windows Biometric Framework risolve questa varietà offrendo un'architettura estendibile che consente agli sviluppatori di terze parti di creare componenti plug-in personalizzati. Il componente principale è un oggetto software denominato unità biometrica. Le unità biometriche espongono le funzionalità di un dispositivo al Framework tramite un'interfaccia standard costituita da sensori, motore e adattatori di archiviazione. Le unità biometriche e i relativi componenti costitutivi vengono descritti negli argomenti seguenti.

## <a name="biometric-unit"></a>Unità biometrica

Il componente centrale dell'architettura di plug-in Windows Biometric Framework è l'unità biometrica, un oggetto software che espone le funzionalità di un dispositivo biometrico al Framework tramite un'interfaccia standard.

Un singolo sensore fisico è associato a ogni unità biometrica. Il sensore acquisisce i dati biometrici e può anche, a seconda delle funzionalità hardware, eseguire altre operazioni biometriche, ad esempio la corrispondenza dei modelli e l'archiviazione. I sensori che non supportano l'onboarding o l'archiviazione richiedono moduli software aggiuntivi per eseguire queste funzioni. Per ulteriori informazioni, vedere [Adapter](/previous-versions//dd401508(v=vs.85)).

Nella figura seguente viene illustrato il flusso di dati attraverso un'unità biometrica. Il flusso di dati costituisce essenzialmente un tipo di pipeline. L'input iniziale per la pipeline è un campione biometrico acquisito da un sensore fisico. Il motore tenta di trovare una corrispondenza tra l'esempio e i modelli già presenti nell'archivio modelli o, se non viene trovata alcuna corrispondenza, compila un nuovo modello da esempi fisici ripetuti e salva il modello nell'archivio.

![flusso di dati attraverso un'unità biometrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo di vita dell'unità biometrica

### <a name="creation"></a>Creazione

Quando il servizio biometrico di Windows viene avviato o quando riceve una notifica hardware dal gestore di Plug and Play, analizza tutti i componenti hardware che supportano il noto GUID di interfaccia \_ DEVINTERFACE \_ Biometric \_ Reader (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Per ogni dispositivo biometrico è stato individuato:

-   Apre un handle per il dispositivo.
-   Esegue una query sulle funzionalità del dispositivo usando un'interfaccia di controllo del driver biometrico di Windows.
-   Apre la chiave del registro di sistema del dispositivo e tenta di individuare le informazioni relative a tutti i plug-in di adapter associati.
-   Apre la chiave del registro di sistema del servizio biometrico di Windows e cerca informazioni sui plug-in globali che devono eseguire l'override dei valori specifici del dispositivo rilevati nel passaggio precedente.
-   Compila un'unità biometrica per rappresentare il dispositivo e passa l'unità a un provider di servizi biometrico.

### <a name="configuration"></a>Configurazione

Dopo che un provider di servizi biometrico (BSP) accetta un'unità biometrica, configura l'unità e la assegna a un pool di sensori. Per altre informazioni, vedere [pool di sensori](sensor-pools.md). L'unità viene configurata caricando le schede appropriate, connettendosi a un archivio modelli e possibilmente modificando la modalità operativa. Un'unità biometrica può essere configurata in modo da funzionare in una delle due modalità seguenti:

-   Nella modalità di base, l'unità funge da dispositivo di acquisizione semplice. Non usa l'elaborazione o l'archiviazione onboarding, ma si basa interamente sulle schede software per ottenere supporto aggiuntivo. Dovrebbe essere in grado di generare esempi in un formato standard. Ad esempio, i lettori di impronte digitali devono generare esempi che siano conformi a ANSI INCIs 381-2004. Lo scopo della modalità di base è quello di supportare l'interoperabilità tra i componenti di fornitori diversi.
-   In modalità avanzata l'unità biometrica usa le funzioni di elaborazione e archiviazione di onboarding. Deve esporre le interfacce standard, ma è in grado di generare ed elaborare esempi in qualsiasi formato desiderato.

Quando un'unità biometrica viene spostata da un pool di sensori a un altro, gli adapter vengono scaricati e vengono riconfigurati per il nuovo pool di sensori. L'identità dell'unità biometrica rimane costante; vengono modificati solo i plug-in di configurazione hardware e di adapter.

### <a name="shut-down"></a>Arresta

Quando il servizio biometrico di Windows viene arrestato o quando il Plug and Play Manager notifica che un'unità è stata rimossa, il servizio Elimina tutte le unità biometriche.

## <a name="adapters"></a>adapter

I componenti del software plug-in denominati adapter consentono di connettere un'unità biometrica all'hardware sottostante e fornire tutte le funzionalità che potrebbero mancare dall'hardware del sensore. Sono disponibili tre tipi di adapter che è possibile creare:

-   Un adattatore del sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di esempi e il controllo del flusso di dati biometrici nel motore di elaborazione.
-   Un adattatore del motore genera modelli biometrici dagli esempi acquisiti, associa gli esempi ai modelli esistenti e indicizza i modelli.
-   Un adattatore di archiviazione gestisce i database modello.

È possibile caricare e scaricare gli adapter in fase di esecuzione. In questo modo, il servizio biometrico di Windows consente di riconfigurare dinamicamente un'unità biometrica connettendosi a un diverso set di schede.

Infine, ognuna delle interfacce dei sensori, dei motori e degli adattatori di archiviazione espone due metodi, **ControlUnit** e **ControlUnitPrivileged**, che consentono alle applicazioni client di accedere alle funzionalità di adapter personalizzate definite dal fornitore. Ciò consente al fornitore di definire un set di operazioni di controllo quasi illimitato per un dispositivo. Inoltre, scegliendo la funzione da implementare, un fornitore può scegliere di rendere disponibili alcune operazioni di controllo agli utenti senza privilegi, limitando al tempo stesso le altre operazioni agli utenti con privilegi.

Per ulteriori informazioni sulla creazione di adapter, vedere [creazione di plug-](creating-adapter-plug-ins.md)in di adapter.

## <a name="adapter-performance-requirements"></a>Requisiti delle prestazioni dell'adapter

Poiché l'obiettivo è la risposta rapida complessiva, le prestazioni di un adapter non vengono specificate in termini di limiti di tempo per routine specifiche. Al contrario, le prestazioni vengono specificate come un set di requisiti per l'esperienza utente complessiva.

Esistono due requisiti:

-   Qualsiasi interazione tra l'utente e il sistema operativo che prevede la biometria deve essere completata entro due secondi. Tale intervallo misura l'ora di inizio e di fine che l'utente percepisce dal momento in cui tocca o scorre il sensore fino al momento in cui si verifica un evento visibile sullo schermo del dispositivo. Ad esempio, durante lo sblocco, non è necessario più di un ritardo di due secondi tra l'utente che tocca o scorre il sensore di impronta digitale e la schermata di blocco che riconosce l'identità dell'utente.
-   Per quanto riguarda l'aspetto iniziale dei riquadri delle credenziali nella schermata di accesso o di blocco, è possibile attendere un po' più tempo (tre secondi, massimo), ma si preferisce ancora prima piuttosto che in seguito. In particolare, il riquadro bio deve essere visibile sullo schermo entro tre secondi dall'aspetto del pannello di blocco o di accesso.

Questi numeri non sono arbitrari. Numerosi studi hanno dimostrato che gli esseri umani tendono a sperimentare tutto ciò che accade in un intervallo di due secondi come parte del momento "ora". Se l'evento A e l'evento B avvengono entro due secondi l'uno dall'altro, gli utenti percepiscono tali eventi come simultanei. Se gli eventi sono separati da più di tre secondi, le persone pensano che ci sia un ritardo, ovvero che qualcosa stia "richiedendo troppo tempo". Si tratta quindi di un problema di psicologia umana cablata.

 

 