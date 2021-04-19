---
title: Implementazione di In-Place attivazione
description: Implementazione di In-Place attivazione
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298281"
---
# <a name="implementing-in-place-activation"></a>Implementazione di In-Place attivazione

L'attivazione sul posto consente a un utente di interagire con un oggetto incorporato senza uscire dal documento contenitore. Quando un utente attiva l'oggetto, una *barra dei menu composita* che include elementi dalle barre dei menu delle applicazioni del contenitore e dell'applicazione Server sostituisce la barra dei menu principale del contenitore. I comandi e le funzionalità di entrambe le applicazioni sono quindi disponibili per l'utente, inclusa la Guida sensibile al contesto per l'oggetto attivo. Quando un utente inizia a lavorare con una parte non oggetto del documento, l'oggetto viene disattivato, causando il menu originale del documento contenitore per sostituire il menu composito.

Questa funzionalità è stata originariamente denominata *modifica sul posto*. Il nome è stato modificato perché un utente può interagire con un oggetto in esecuzione solo un modo. I clip audio, ad esempio, possono essere ascoltati anziché modificarli. È possibile visualizzare i clip video anziché modificarli. L'attivazione sul posto è particolarmente adatta nel caso di clip video perché consente l'esecuzione sul posto, senza chiamare una finestra separata. Questo potrebbe essere fondamentale se il video venisse visualizzato, ad esempio, in combinazione con i dati di testo adiacenti nel documento contenitore.

L'implementazione dell'attivazione sul posto è strettamente facoltativa per le applicazioni contenitore e server. OLE supporta ancora il modello in cui l'attivazione di un oggetto comporta l'apertura di una finestra separata da parte dell'applicazione server. Gli oggetti collegati vengono sempre aperti in una finestra separata per evidenziare che si trovano in un documento separato.

L'attivazione sul posto inizia con l'oggetto in risposta a una chiamata di [**Overb IOleObject::D**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) dal relativo contenitore. Questa chiamata viene in genere eseguita in risposta a un utente che fa doppio clic sull'oggetto o seleziona un comando (verbo) dal menu modifica dell'applicazione contenitore.

La finestra sul posto riceve l'input della tastiera e del mouse mentre l'oggetto incorporato è attivo. Quando un utente seleziona i comandi dalla barra dei menu composita, il comando e i messaggi di menu associati vengono inviati al contenitore o all'applicazione oggetto, a seconda del proprietario del menu a discesa particolare selezionato. L'input per mezzo di righelli, barre degli strumenti o aree di controllo di un oggetto passa direttamente all'oggetto incorporato che possiede le finestre.

Un oggetto incorporato attivato sul posto rimane attivo fino a quando il contenitore non lo disattiva in risposta all'input dell'utente oppure l'oggetto volontariamente lo stato attivo, come può fare, ad esempio, un clip video. Un utente può disattivare un oggetto facendo clic all'interno del documento del contenitore ma al di fuori della finestra di attivazione sul posto dell'oggetto o semplicemente facendo clic su un altro oggetto. Un oggetto attivato sul posto rimane attivo, tuttavia, se l'utente fa clic sulla barra del titolo del contenitore, sulla barra di scorrimento o, in particolare, sulla barra dei menu.

È possibile implementare un server oggetto di attivazione sul posto come un server in-process (DLL) o un server locale (EXE). In entrambi i casi, la barra dei menu composita contiene elementi, in genere menu a discesa, sia dal processo del server che da quello del contenitore. Nel caso di un server in-process, la finestra di attivazione sul posto è semplicemente un'altra finestra figlio nella gerarchia della finestra del contenitore, ricevendo l'input tramite il message pump dell'applicazione contenitore.

Nel caso di un server locale, la finestra di attivazione sul posto appartiene al processo dell'applicazione server dell'oggetto incorporato, ma la finestra padre appartiene al contenitore. L'input per la finestra attivazione sul posto viene visualizzato nella coda di messaggi del server e viene inviato dal ciclo di messaggi del server. Le librerie OLE sono responsabili del modo in cui i comandi di menu e i messaggi vengono inviati correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




