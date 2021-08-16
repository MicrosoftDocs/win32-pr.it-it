---
title: Tasti di scelta rapida e varianti dei comandi
description: Tasti di scelta rapida e varianti dei comandi
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a3379b5eb6dced9ccebb3e04e76be87fdca7ea5af341b647cb0205888c283
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807921"
---
# <a name="command-shortcuts-and-variations"></a>Tasti di scelta rapida e varianti dei comandi

È possibile usare diversi tasti di scelta rapida quando si usano i comandi MCI. Questi tasti di scelta rapida consentono di usare un singolo identificatore per fare riferimento a tutti i dispositivi aperti dall'applicazione o per aprire un dispositivo senza emettere in modo esplicito un comando open [**(**](open.md) [**MCI \_ OPEN).**](mci-open.md)

È possibile specificare "all" (MCI ALL DEVICE ID) come identificatore di dispositivo per qualsiasi \_ comando che non restituisce \_ \_ informazioni. Quando si specifica "all", MCI invia il comando in sequenza a tutti i dispositivi aperti dall'applicazione corrente.

Ad esempio, il [**comando close**](close.md) "all" chiude tutti i dispositivi aperti e il comando [**play**](play.md) "all" avvia la riproduzione di tutti i dispositivi aperti dall'applicazione. Poiché MCI invia in sequenza i comandi ai dispositivi MCI, esiste un intervallo tra il momento in cui il primo e l'ultimo dispositivo ricevono il comando.

L'uso di "all" è un modo pratico per trasmettere un comando a tutti i dispositivi, ma non è consigliabile basarsi su di esso per sincronizzare i dispositivi. L'intervallo tra i messaggi può variare.

Quando si esegue un comando e si specifica un dispositivo non aperto, MCI tenta di aprire il dispositivo prima di implementare il comando. Le regole seguenti si applicano all'apertura automatica dei dispositivi:

-   La funzionalità di apertura automatica funziona solo con l'interfaccia della stringa di comando.
-   La funzionalità di apertura automatica non riesce per i comandi specifici dei driver di dispositivo personalizzati.
-   I dispositivi aperti automaticamente non rispondono ai comandi che usano "all" come nome del dispositivo.
-   La funzionalità di apertura automatica non consente all'applicazione di specificare il flag "type". Senza il nome del dispositivo, MCI determina il nome del dispositivo dalle voci nel Registro di sistema. Per usare un dispositivo specifico, è possibile combinare il nome del dispositivo con il nome del file usando il punto esclamativo, come descritto nel materiale di riferimento per il [**comando open.**](open.md)

Se un'applicazione usa la funzionalità di apertura automatica per aprire un dispositivo, l'applicazione deve controllare il valore restituito di ogni successivo comando aperto per verificare che il dispositivo sia ancora aperto. McI chiude automaticamente anche tutti i dispositivi che si apre automaticamente. McI chiude in genere un dispositivo nelle situazioni seguenti:

-   Il comando è stato completato.
-   Il comando viene interrotto.
-   Si richiede la notifica in un comando successivo.
-   MCI rileva un errore.

 

 




