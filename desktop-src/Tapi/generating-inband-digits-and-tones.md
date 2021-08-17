---
description: Quando una chiamata è nello stato connesso, le informazioni possono essere trasmesse su di essa.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Generazione di cifre e toni inband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424881"
---
# <a name="generating-inband-digits-and-tones"></a>Generazione di cifre e toni inband

Quando una chiamata è nello *stato connesso,* le informazioni possono essere trasmesse su di essa. Sono disponibili due funzioni che consentono la segnalazione in banda end-to-end tra l'applicazione e le apparecchiature di stazione remota, ad esempio una answering machine. Una funzione è [**lineGenerateDigits,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)che genera cifre inband in una chiamata, segnalandole tramite il canale vocale. Le cifre possono essere segnalate come sequenze di pulse/rotanti o come toni DTMF. L'altra funzione è [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), che consente all'applicazione di generare uno dei diversi toni multifrequency inband (sul flusso multimediale). Ciò genera toni di telefonia, ad esempio ringback, segnale acustico e occupato, nonché toni arbitrari multifrequency e multicadenced.

In una chiamata può essere in corso una sola cifra o generazione di toni alla volta. Al termine della generazione di cifre o toni, viene inviato un messaggio [**LINE \_ GENERATE**](line-generate.md) all'applicazione che ha richiesto la generazione. Nel caso in cui vengono generate più cifre, viene inviato un solo messaggio dopo la generazione di tutte le cifre. La chiamata [**a lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) o [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) mentre è in corso la generazione di cifre o toni interromperà la generazione attualmente in corso e invierà il messaggio LINE GENERATE all'applicazione la cui generazione è stata interrotta con un'indicazione di \_ annullamento.

 

 



