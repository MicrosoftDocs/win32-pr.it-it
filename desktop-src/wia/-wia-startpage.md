---
description: Windows Image Acquisition (WIA) è la piattaforma di acquisizione immagini ancora della famiglia di sistemi operativi Windows a partire da Windows Millennium Edition (Windows Me) e Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Acquisizione di immagini di Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff1f3fb51a4c87d909637a90591336d9d2eb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526419"
---
# <a name="windows-image-acquisition-wia"></a>Acquisizione di immagini di Windows (WIA)

Windows Image Acquisition (WIA) è la piattaforma di acquisizione immagini ancora della famiglia di sistemi operativi Windows a partire da Windows Millennium Edition (Windows Me) e Windows XP.

-   [Introduzione](#introduction)
-   [Vantaggi dell'acquisizione di immagini Windows 2,0](#benefits-of-windows-image-acquisition-20)
    -   [Per writer di applicazioni](#for-application-writers)
    -   [Per i produttori di dispositivi](#for-device-manufactures)
    -   [Per gli utenti dello scanner](#for-scanner-users)
-   [Sviluppo dell'acquisizione di immagini Windows](#development-of-windows-image-acquisition)
-   [Panoramica dell'acquisizione di immagini Windows](#overview-of-windows-image-acquisition)
-   [Fact sull'acquisizione di immagini Windows 2,0](#facts-about-windows-image-acquisition-20)
-   [Destinatari degli sviluppatori](#developer-audience)
-   [Requisiti della fase di esecuzione](#run-time-requirements)
-   [Argomenti WIA](#wia-topics)

## <a name="introduction"></a>Introduzione

La piattaforma WIA consente alle applicazioni di imaging/grafica di interagire con l'hardware per la creazione di immagini e di standardizzare l'interazione tra applicazioni e scanner diversi. In questo modo le diverse applicazioni possono comunicare e interagire con i diversi scanner senza che i writer di applicazioni e lo scanner producano per personalizzare l'applicazione o i driver per ciascuna combinazione di dispositivi applicativi.

![grafico che mostra l'architettura di base di WIA come un livello bidirezionale tra applicazioni e dispositivi di creazione di immagini. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Vantaggi dell'acquisizione di immagini Windows 2,0

WIA offre vantaggi per sviluppatori di applicazioni, produttori di dispositivi e utenti di scanner che devono interagire con l'hardware per la creazione di immagini.

### <a name="for-application-writers"></a>Per writer di applicazioni

-   Windows esegue un processo di certificazione per i driver WIA in modo da garantire che le applicazioni WIA siano compatibili a livello di base con tutti gli scanner basati su WIA.
-   I driver WIA vengono caricati nel processo del servizio WIA, offrendo in questo modo un ambiente di driver più stabile.
-   Le applicazioni possono essere avviate dal pulsante Scan scanner tramite gli eventi push supportati dal sottosistema WIA.
-   Il WIA include un filtro di segmentazione predefinito che tutti i driver possono sfruttare; in questo modo, le applicazioni non devono scrivere codice per l'analisi in più aree per scopi quali la separazione di un numero elevato di foto distribuite su uno scanner piano.

### <a name="for-device-manufactures"></a>Per i produttori di dispositivi

-   Il processo di certificazione del driver WIA consente agli sviluppatori di driver di stabilire che i driver sono conformi a WIA.
-   I driver WIA possono sfruttare i vantaggi di un filtro di segmentazione incorporato, di un filtro per l'elaborazione di immagini e di un gestore di errori, se scelgono di farlo.
-   Gli scanner basati su WIA funzionano direttamente in Windows con le applicazioni di analisi di Windows, ad esempio fax di Windows e analisi e disegno.
-   I driver WIA offrono una migliore integrazione con Windows, ad esempio l'esperienza completa del dispositivo.
-   La versione di Windows Vista include un driver di classe WSD-WIA che consente a tutti i dispositivi conformi al protocollo WS-Scan (Web Services for scanner) di funzionare con le applicazioni WIA senza alcun driver o software aggiuntivo.

### <a name="for-scanner-users"></a>Per gli utenti dello scanner

-   Gli scanner basati su WIA possono essere utilizzati da applicazioni Windows quali fax e scanner di Windows, senza la necessità di software aggiuntivo.
-   Le applicazioni e gli scanner basati su WIA possono inoltre sfruttare i componenti aggiuntivi WIA, ad esempio il filtro di segmentazione, che consente a tali funzionalità di elaborare un numero di immagini sullo scanner e di analizzarle tutte in singoli file senza l'intervento dell'utente.
-   I dispositivi basati su WIA offrono una migliore integrazione con altre funzionalità di Windows, ad esempio la funzionalità relativa alla fase del dispositivo per Windows 7.
-   WIA offre un'esperienza di analisi più solida, stabile e affidabile isolando il driver e l'applicazione.

## <a name="development-of-windows-image-acquisition"></a>Sviluppo dell'acquisizione di immagini Windows

L'architettura di imaging in Windows 2000 e Windows 95 o versioni successive è costituita da un'astrazione hardware di basso livello, da un'architettura di immagini ancora (STI) e da un set di API di alto livello noto come TWAIN. In Windows XP e Windows me è stato introdotto WIA. WIA è un'architettura di imaging basata su ist e non richiede TWAIN, anche se TWAIN è ancora supportato insieme a WIA.

WIA 1,0 è stato introdotto in Windows me e Windows XP e supporta scanner, fotocamere digitali e apparecchiature video digitali. WIA 2,0 è stato rilasciato con Windows Vista. WIA 2,0 è destinato agli scanner, ma continua a offrire supporto per le applicazioni e i dispositivi WIA 1,0 legacy tramite un livello di compatibilità WIA 1,0 a WIA 2,0 fornito dal servizio WIA. Tuttavia, il supporto per contenuti video è stato rimosso da WIA per Windows Vista. In futuro è consigliabile usare l'API Windows Portable Devices (WPD) per fotocamere digitali e apparecchiature video digitali. WIA 1,0, oltre ai driver STI TWAIN, sono ancora supportati direttamente in Windows Vista e Windows 7 insieme ai driver di dispositivo e alle applicazioni per la creazione di immagini WIA 2,0 nativi.

## <a name="overview-of-windows-image-acquisition"></a>Panoramica dell'acquisizione di immagini Windows

WIA fornisce un Framework che consente a un dispositivo di presentare le proprie funzionalità esclusive al sistema operativo e consente alle applicazioni per la creazione di immagini di richiamare tali funzionalità esclusive.

La piattaforma WIA include un protocollo di acquisizione dei dati, un modello di driver di dispositivo e un'interfaccia (DDI), un'API e un servizio WIA dedicato. La piattaforma include anche un set di driver in modalità kernel predefiniti che supportano la comunicazione con i dispositivi di imaging connessi localmente tramite interfacce USB, seriale/parallela, SCSI e FireWire. Il sottosistema WIA include anche un livello di compatibilità trasparente che consente alle applicazioni compatibili con TWAIN di impiegare e utilizzare i dispositivi basati sul driver WIA.

I dispositivi di creazione di immagini connesse alla rete che supportano il protocollo WSD (Web Services for Devices) possono essere utilizzati anche da applicazioni di imaging compatibili con WIA in Windows Vista e Windows 7 predefinite tramite un driver di classe WSD-WIA fornito come parte di Windows Vista. Il driver di classe converte le chiamate WIA in chiamate WSD e viceversa e rende le applicazioni WIA già esistenti funzionano con gli scanner basati su WSD senza driver aggiuntivi.

I driver WIA sono costituiti da un componente dell'interfaccia utente (UI) e da un componente driver principale, caricati in due diversi spazi di elaborazione: interfaccia utente nello spazio dell'applicazione e core del driver nello spazio del servizio WIA. Il servizio viene eseguito nel contesto di sistema locale in Windows XP e viene eseguito nel contesto del servizio locale a partire da Windows Server 2003 e Windows Vista per garantire una protezione avanzata da parte di bug o driver dannosi.

![grafico che mostra l'architettura di WIA e il modo in cui opera come servizio.](images/wia-arch.png)

Il set di API WIA espone le applicazioni per la creazione di immagini alla funzionalità hardware di acquisizione delle immagini, fornendo supporto per:

-   Enumerazione dei dispositivi di acquisizione immagini disponibili.
-   Creazione simultanea di connessioni a più dispositivi.
-   Esecuzione di query sulle proprietà dei dispositivi in modo standard ed espandibile.
-   Acquisizione dei dati del dispositivo mediante meccanismi di trasferimento standard e ad alte prestazioni.
-   Gestione delle proprietà delle immagini tra trasferimenti di dati.
-   Notifica dello stato del dispositivo e della gestione degli eventi di analisi.

Windows ha aggiunto il supporto per gli script a WIA rilasciando la libreria di automazione WIA in 2002 incorporata in Windows Vista come livello di automazione Windows Image Acquisition (WIA) e continua a far parte di Windows 7. La libreria di automazione WIA fornisce funzionalità di acquisizione di immagini end-to-end per ambienti di sviluppo di applicazioni abilitate per l'automazione e linguaggi di programmazione quali Microsoft Visual Basic 6,0, pagine Active Server (ASP), VBScript e C \# .

Per Windows 7, le API WIA hanno supporto aggiuntivo per integrare il supporto per l'analisi push già esistente.

-   Analisi avviata dal dispositivo configurata automaticamente con i parametri di analisi configurati sullo scanner nel pannello anteriore del dispositivo.
-   Selezione automatica dell'origine per l'analisi avviata dal dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Fact sull'acquisizione di immagini Windows 2,0

-   Il meccanismo di trasferimento dei dati in WIA 2,0 è basato sul flusso. L'astrazione del flusso rimuove la distinzione tra tipi di trasferimento diversi e consente inoltre lo scambio di metadati che si concordano a vicenda tra il dispositivo e l'applicazione.
-   Il sottosistema WIA 2,0 include anche un componente aggiuntivo di base del driver del filtro per l'elaborazione delle immagini che può essere sostituita facoltativamente dal driver dello scanner, se il driver sceglie di fornire un filtro personalizzato per l'elaborazione delle immagini. Il filtro incorporato consente la post-elaborazione delle immagini acquisite tramite lo scanner. Il filtro di elaborazione delle immagini Abilita anche le anteprime software in tempo reale quando vengono regolate impostazioni ridotte, ad esempio luminosità e contrasto.
-   Il filtro di segmentazione è un altro componente WIA utile che può essere sostituito da un filtro più personalizzato da parte del driver dello scanner. Il filtro di segmentazione può essere usato per l'analisi in più aree. L'analisi in più aree, ad esempio, consente a un'applicazione di rilevare automaticamente aree di analisi diverse senza alcun intervento dell'utente, ad esempio l'identificazione di una serie di foto che si trovano in modo casuale sul piano dello scanner.
-   WIA 2,0 fornisce un gestore di errori sostituibile/estendibile per gestire correttamente ed eventualmente recuperare da errori di software, hardware e configurazione e ritardi. Il gestore errori è un altro componente WIA che può essere sostituito con una versione più personalizzata dal driver dello scanner. Questa estensione fornisce messaggi di stato e di errore durante le acquisizioni dei dati, ad esempio "illuminazione lampo", "copertina aperta", "Inceppamento carta" e così via. Questa estensione consente anche il supporto più pulito per le "operazioni di annullamento".

## <a name="developer-audience"></a>Sviluppatori

L'API WIA è progettata per l'uso da parte dei programmatori C/C++. È necessaria una certa familiarità con le interfacce Windows GUI e Component Object Model (COM).

Per gli sviluppatori che hanno familiarità con Microsoft Visual Basic 6,0, Active Server Pages (ASP) o scripting, WIA fornisce un livello di automazione per Windows XP Service Pack 1 (SP1) o versione successiva che si basa su e semplifica l'accesso alle fondamenta fornite da C/C++. Per informazioni sul livello di automazione, vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> Il livello di automazione WIA sostituisce lo script Windows Image Acquisition (WIA) 1,0.

 

## <a name="run-time-requirements"></a>Requisiti di runtime

Per le applicazioni che usano l'API WIA è necessario Windows XP o versione successiva.

## <a name="wia-topics"></a>Argomenti WIA

Gli argomenti WIA sono organizzati come illustrato nella tabella seguente.



|                                                                                                                              |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Informazioni sull'acquisizione di immagini Windows](-wia-about-windows-image-acquisition.md)                                                  | Informazioni generali su WIA                                                                     |
| [Driver di acquisizione immagini Windows](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Sviluppo di driver WIA                                                                            |
| [Livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Livello di automazione WIA                                                                              |
| [Esercitazione WIA](-wia-wia-tutorial.md)                                                                                        | Procedura dettagliata del codice incluso nel Software Development Kit (SDK) incentrato su attività specifiche |
| [Riferimento](-wia-reference.md)                                                                                              | Informazioni sulle interfacce WIA, i metodi, gli oggetti e i tipi di dati utilizzati in C/C++ e nello scripting.      |



 

 

 
