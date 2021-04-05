---
title: Affidabilità delle informazioni estese sugli errori
description: Le informazioni estese sugli errori non sono affidabili.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707324"
---
# <a name="reliability-of-extended-error-information"></a>Affidabilità delle informazioni estese sugli errori

Le informazioni estese sugli errori non sono affidabili. Le informazioni estese sugli errori non possono essere usate per la compilazione della logica del codice. È consigliabile verificare la presenza di informazioni estese sugli errori e, in tal caso, eseguire il dump, salvare o registrare tali informazioni. Ma non si basano sulle informazioni o sul contenuto.

I motivi seguenti spiegano perché le informazioni estese sugli errori non sono affidabili:

-   La sequenza e il contenuto dei record degli errori estesi dipendono dall'architettura interna del sistema, che è soggetta a modifiche. Una determinata operazione può passare attraverso NPFS nei sistemi correnti, ma domani potrebbe passare attraverso TCP. Questi diversi componenti generano codici di errore molto diversi e i controlli del codice sono pertanto intrinsecamente inaffidabili e non consigliati.
-   La propagazione delle informazioni estese sugli errori può essere disabilitata, come illustrato in precedenza. Se il codice di rilevamento è incluso, l'applicazione smetterà probabilmente di funzionare in determinati ambienti.
-   La propagazione delle informazioni sugli errori estesi viene eseguita nel modo migliore possibile. La propagazione o la generazione di informazioni estese sugli errori possono avere esito negativo se nel computer non è disponibile memoria sufficiente per elaborare o propagare la catena. In tali circostanze, la catena verrà eliminata. Alcuni protocolli hanno lunghezze limitate per i pacchetti di errore, perché in genere non includono molte informazioni. Se la lunghezza della catena supera la lunghezza consentita del pacchetto, il tempo di esecuzione RPC inizia a rilasciare le informazioni dalla catena nel tentativo di adattare la catena al pacchetto. Il tempo di esecuzione Elimina prima di tutto i record, a partire dal penultimo record, andando indietro fino a quando non rimangono solo il primo e l'ultimo record. Se la catena continua a non rientrare in un pacchetto, il tempo di esecuzione Elimina i parametri di stringa e i nomi dei computer. Se viene eliminato un parametro di stringa, il tipo del parametro viene impostato su None. Se un record viene eliminato, il flag EEInfoNextRecordsMissing viene impostato nel record successivo e EEInfoPreviousRecordsMissing viene impostato nel record precedente.

 

 




