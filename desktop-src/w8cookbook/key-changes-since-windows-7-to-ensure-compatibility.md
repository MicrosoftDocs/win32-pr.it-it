---
title: Modifiche principali rispetto alla Windows 7 per garantire la compatibilità
description: Modifiche principali rispetto alla Windows 7 per garantire la compatibilità
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ed00dacb0d8556d4e16de84fbc20b7ac6a56bed6560bee3213c7919b9760cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815191"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a>Modifiche principali rispetto alla Windows 7 per garantire la compatibilità

Microsoft è consapevole dell'importanza della compatibilità per gli sviluppatori. ISV e sviluppatori vogliono essere certi che le loro app vengano eseguite come previsto in tutte le versioni supportate del sistema operativo Windows. Per i consumatori e le aziende sono in gioco investimenti importanti: è fondamentale che le app che hanno acquistato continuino a funzionare. È noto come la compatibilità sia un criterio fondamentale per le decisioni sugli acquisti. Le app ben scritte in base alle procedure consigliate ridurranno notevolmente la varianza del codice quando viene rilasciata una nuova versione di Windows e ridurranno la frammentazione. Queste app hanno un investimento di progettazione ridotto da mantenere e un time-to-market più rapido.

Nell'era di Windows 7, l'approccio alla compatibilità è stato perlopiù reattivo. In Windows 8 abbiamo iniziato ad adottare una prospettiva diversa, lavorando ai meccanismi interni di Windows per garantire che la compatibilità fosse incorporata e non il risultato di interventi successivi. Windows 10 è la versione più compatibile del sistema operativo sin dalla progettazione finora pubblicata. Ecco alcuni dei principali aspetti che hanno reso possibile tutto ciò:

-   Telemetria delle app: questo consente di comprendere la popolarità delle app nell'ecosistema Windows per informare i test di compatibilità.
-   Partnership ISV: collaborare direttamente con partner esterni per fornire loro dati e risolvere i problemi che gli utenti possono sperimentare.
-   Revisioni di progettazione, rilevamento upstream: collaborare con i team di funzionalità per ridurre il numero di modifiche di rilievo Windows. La revisione per la compatibilità è un passaggio cruciale per i team responsabili delle funzionalità.
-   Controllo più stretto sulle modifiche dell'API & migliore comunicazione
-   Ciclo di invio e feedback: il Windows Insider riceve compilazioni in anteprima che consentono di migliorare la capacità di trovare problemi di compatibilità prima che venga rilasciata una build finale ai clienti. Il processo di feedback non serve solo a mettere in evidenza i bug, ma conferma che vengono offerte le funzionalità desiderate dagli utenti.

 

 




