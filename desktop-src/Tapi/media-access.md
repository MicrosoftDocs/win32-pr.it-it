---
description: Le funzionalità multimediali sono diverse con TAPI 2.2 (TAPI/C) anziché TAPI 3 (COM), principalmente perché l'API COM ha accesso ai provider di servizi multimediali (MSP).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Accesso ai supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575611"
---
# <a name="media-access"></a>Accesso ai supporti

Le funzionalità multimediali sono diverse con TAPI 2.2 (TAPI/C) anziché TAPI 3 (COM), principalmente perché l'API COM ha accesso ai provider di servizi multimediali (MSP). Per altre informazioni sui provider di servizi multimediali, vedere [Informazioni sul provider di servizi multimediali .](./about-the-media-service-provider-msp-.md) Per altre informazioni sulle operazioni del flusso multimediale, vedere [Controllo multimediale](./device-control.md).

I due concetti più importanti per un'applicazione sono il tipo di supporto (o modalità) e il flusso. Il tipo è il formato in cui vengono trasmessi i dati. Per altre informazioni e un elenco di tipi definiti da TAPI, vedere [Costanti LINEMEDIAMODE \_ ](linemediamode--constants.md). Il flusso multimediale è il flusso effettivo di dati. Un msp può fornire l'accesso diretto al flusso. Le applicazioni TAPI 2.2 hanno accesso, ma fanno riferimento principalmente ad altre API per implementare tali controlli.

Queste API includono l'API Waveform, l'API Comm e Media Control Interface (MCI). L'API Waveform viene usata per la programmazione multimediale, l'API Comm è il set di funzioni di comunicazione fornite da Platform Software Development Kit (SDK) e MCI fornisce un'interfaccia generalizzata di alto livello per il controllo dei dispositivi multimediali.

Ad esempio, per i dispositivi line, un'applicazione può usare TAPI 2.2 per stabilire una connessione a un'altra stazione. Dopo aver stabilito la connessione, l'applicazione può quindi usare l'API Waveform (o l'API WAVEAUDIO MCI) nel dispositivo associato per riprodurre (inviare) e registrare (ricevere) i dati audio sulla connessione. Analogamente, se il flusso multimediale di connessione è di un modem, un'applicazione userebbe le estensioni di configurazione del modem dell'API Comunicazioni per controllare il flusso multimediale.

Per fornire a TAPI 2.2 l'accesso tramite flusso multimediale a un telefono o a una chiamata su un dispositivo line, il provider di servizi deve implementare sia lo SPI di telefonia che l'interfaccia SPI o DDI (Device-Driver Interface) del flusso multimediale appropriato. Il provider di servizi può supportare linee e telefoni contemporaneamente.

Poiché queste classi di dispositivo e le operazioni del flusso multimediale funzionano indipendentemente l'una dall'altra, il coordinamento del relativo utilizzo deve verificarsi a livello di applicazione. È probabile che più applicazioni che condividono chiamate e flussi multimediali richiedano il coordinamento delle attività a livello di applicazione per evitare un uso in conflitto di TAPI e dell'API del flusso multimediale.

TAPI segnala le modifiche nel tipo di flusso multimediale (voce, fax, modem dati e così via) alle applicazioni partecipanti. Questo processo viene talvolta definito classificazione [*delle chiamate*](c-tapgloss.md). Il meccanismo usato per determinare il tipo di flusso multimediale è specifico del provider di servizi. Ad esempio, un provider di servizi può filtrare il flusso multimediale per l'energia o i toni che caratterizzano il tipo di supporto oppure può usare anelli distintivi, dati s scambiati nei messaggi in rete o informazioni sul chiamante o sull'ID chiamato per effettuare questa determinazione.

-   [Monitoraggio delle chiamate](call-monitoring.md)
-   [Controllo dei supporti](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Raccolta di cifre](digit-gathering.md)
-   [Generazione di cifre e toni inband](generating-inband-digits-and-tones.md)

 

 
