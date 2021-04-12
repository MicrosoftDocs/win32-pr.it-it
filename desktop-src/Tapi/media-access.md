---
description: Le funzionalità multimediali sono diverse rispetto a TAPI 2,2 (TAPI/C) rispetto a TAPI 3 (COM), in gran parte perché l'API COM ha accesso ai provider di servizi multimediali (MSPs).
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Accesso ai supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb3fe361aab9d5b5c9897deb5ea36d6e85adcfd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234512"
---
# <a name="media-access"></a>Accesso ai supporti

Le funzionalità multimediali sono diverse rispetto a TAPI 2,2 (TAPI/C) rispetto a TAPI 3 (COM), in gran parte perché l'API COM ha accesso ai provider di servizi multimediali (MSPs). Per ulteriori informazioni su MSPs, vedere [informazioni sul provider di servizi multimediali (msp)](./about-the-media-service-provider-msp-.md). Per altre informazioni sulle operazioni dei flussi multimediali, vedere [controllo multimediale](./device-control.md).

I due concetti più importanti per un'applicazione sono il tipo di supporto (o la modalità) e il flusso. Il tipo è il formato in cui vengono trasmessi i dati. Per altre informazioni e per un elenco di tipi definiti da TAPI, [vedere \_ costanti LINEMEDIAMODE](linemediamode--constants.md). Il flusso multimediale è il flusso di dati effettivo. Un MSP può fornire accesso diretto al flusso. Le applicazioni TAPI 2,2 hanno un certo accesso, ma principalmente fanno riferimento ad altre API per implementare tali controlli.

Queste API includono l'API di forma d'onda, l'API di comunicazione e l'interfaccia di controllo multimediale (MCI). L'API per la forma d'onda viene usata per la programmazione multimediale, l'API di comunicazione è il set di funzioni di comunicazione fornite da Platform Software Development Kit (SDK) e il MCI fornisce un'interfaccia generalizzata di alto livello per il controllo dei dispositivi multimediali.

Per i dispositivi linea, ad esempio, un'applicazione può usare TAPI 2,2 per stabilire una connessione a un'altra stazione. Una volta stabilita la connessione, l'applicazione può quindi usare l'API di forma d'onda (o l'API MCI WaveAudio) sul dispositivo associato per riprodurre (inviare) e registrare (ricevere) dati audio sulla connessione. Analogamente, se il flusso del supporto di connessione è da un modem, un'applicazione utilizzerà le estensioni di configurazione del modem dell'API di comunicazione per controllare il flusso multimediale.

Per fornire a TAPI 2,2 l'accesso tramite flusso multimediale a un telefono o a una chiamata su un dispositivo a linee, il provider di servizi deve implementare sia la telefonia SPI che il flusso multimediale appropriato SPI o l'interfaccia DDI (Device-Driver Interface). Il provider di servizi può supportare linee e telefoni simultaneamente.

Poiché queste classi di dispositivi e operazioni di flusso multimediale funzionano indipendentemente l'una dall'altra, il coordinamento del loro utilizzo deve verificarsi a livello di applicazione. Per più applicazioni che condividono chiamate e flussi multimediali è probabile che sia necessario il coordinamento delle attività a livello di applicazione per impedire l'uso in conflitto di TAPI e dell'API del flusso multimediale.

TAPI segnala le modifiche apportate al tipo di flusso multimediale (voce, fax, modem dati e così via) alle applicazioni partecipanti. Questo processo viene talvolta definito classificazione delle [*chiamate*](c-tapgloss.md). Il meccanismo utilizzato per determinare il tipo di flusso multimediale è specifico del provider di servizi. Un provider di servizi, ad esempio, può filtrare il flusso multimediale per l'energia o i toni che caratterizzano il tipo di supporto oppure può utilizzare la suoneria distinta, i dati scambiati nei messaggi in rete o la conoscenza del chiamante o l'ID chiamato per effettuare questa determinazione.

-   [Monitoraggio delle chiamate](call-monitoring.md)
-   [Controllo multimediale](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Raccolta cifre](digit-gathering.md)
-   [Generazione di cifre e toni inband](generating-inband-digits-and-tones.md)

 

 
