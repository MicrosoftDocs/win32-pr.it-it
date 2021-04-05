---
title: Collegamenti ai comandi e varianti
description: Collegamenti ai comandi e varianti
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712529"
---
# <a name="command-shortcuts-and-variations"></a>Collegamenti ai comandi e varianti

Quando si utilizzano i comandi MCI è possibile utilizzare diversi tasti di scelta rapida. Questi tasti di scelta rapida consentono di usare un singolo identificatore per fare riferimento a tutti i dispositivi aperti dall'applicazione o di aprire un dispositivo senza emettere esplicitamente un comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).

È possibile specificare "All" (MCI \_ All \_ Device \_ ID) come identificatore di dispositivo per qualsiasi comando che non restituisce informazioni. Quando si specifica "All", MCI invia il comando in sequenza a tutti i dispositivi aperti dall'applicazione corrente.

Il comando [**Chiudi**](close.md) "tutti", ad esempio, chiude tutti i dispositivi aperti e il comando [**Play**](play.md) "All" avvia la riproduzione di tutti i dispositivi aperti dall'applicazione. Poiché MCI invia in modo sequenziale i comandi ai dispositivi MCI, esiste un intervallo tra la ricezione del comando da parte del primo e dell'ultimo dispositivo.

L'uso di "All" è un modo pratico per trasmettere un comando a tutti i dispositivi, ma non è consigliabile fare affidamento su di esso per sincronizzare i dispositivi. l'intervallo tra i messaggi può variare.

Quando si emette un comando e si specifica un dispositivo che non è aperto, MCI tenta di aprire il dispositivo prima di implementare il comando. Per l'apertura automatica dei dispositivi sono valide le regole seguenti:

-   La funzionalità di apertura automatica funziona solo con l'interfaccia della stringa di comando.
-   La funzionalità di apertura automatica non riesce per i comandi specifici dei driver di dispositivo personalizzati.
-   I dispositivi aperti automaticamente non rispondono ai comandi che usano "All" come nome del dispositivo.
-   La funzionalità di apertura automatica non consente all'applicazione di specificare il flag "Type". Senza il nome del dispositivo, MCI determina il nome del dispositivo dalle voci nel registro di sistema. Per usare un dispositivo specifico, è possibile combinare il nome del dispositivo con il nome del file usando il punto esclamativo, come descritto nel materiale di riferimento per il comando [**Apri**](open.md) .

Se un'applicazione usa la funzionalità di apertura automatica per aprire un dispositivo, l'applicazione deve controllare il valore restituito di ogni comando aperto successivo per verificare che il dispositivo sia ancora aperto. MCI chiude automaticamente anche tutti i dispositivi che vengono aperti automaticamente. MCI in genere chiude un dispositivo nelle situazioni seguenti:

-   Il comando è stato completato.
-   Si interrompe il comando.
-   Viene richiesta una notifica in un comando successivo.
-   MCI rileva un errore.

 

 




