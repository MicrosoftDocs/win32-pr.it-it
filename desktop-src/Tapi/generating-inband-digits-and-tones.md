---
description: Quando una chiamata è nello stato connesso, le informazioni possono essere trasmesse al suo interno.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Generazione di cifre e toni inband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306329"
---
# <a name="generating-inband-digits-and-tones"></a>Generazione di cifre e toni inband

Quando una chiamata è nello stato *connesso* , le informazioni possono essere trasmesse al suo interno. Vengono fornite due funzioni che consentono la segnalazione di inband end-to-end tra l'applicazione e le apparecchiature della stazione remota, ad esempio un computer di risposta. Una funzione è [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), che genera cifre inband in una chiamata e la segnala sul canale vocale. Le cifre possono essere segnalate come sequenze rotanti/impulsi o come toni DTMF. L'altra funzione è [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), che consente all'applicazione di generare uno dei diversi toni multifrequenza inband (sul flusso multimediale). In questo modo vengono generati i toni di telefonia, ad esempio la riponderia, il segnale acustico e il traffico occupato, nonché i toni multifrequenza arbitrari.

In una chiamata in qualsiasi momento può essere in corso una sola generazione di cifre o di un tono. Quando il numero o la generazione di un tono viene completata, viene inviato un messaggio di generazione [**riga \_**](line-generate.md) all'applicazione che ha richiesto la generazione. Nel caso in cui vengano generate più cifre, viene restituito un singolo messaggio dopo che sono state generate tutte le cifre. La chiamata a [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) o [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) mentre è in corso la generazione di cifre o di un tono interromperà la generazione attualmente in corso e invierà il messaggio di generazione della riga \_ all'applicazione la cui generazione è stata interrotta con un'indicazione di annullamento.

 

 



