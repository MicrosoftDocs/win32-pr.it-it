---
description: Questo argomento descrive il modo in cui l'origine del sequencer gestisce i tempi di presentazione durante la riproduzione.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Tempi di presentazione sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17f5b0ff4bd6f0cfee2b1b461d6fbd11bdbf0fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527835"
---
# <a name="sequence-presentation-times"></a>Tempi di presentazione sequenza

Questo argomento descrive il modo in cui l' [origine del sequencer](sequencer-source.md) gestisce i tempi di presentazione durante la riproduzione.

## <a name="overview"></a>Panoramica

L'origine di Sequencer supporta due modalità diverse: sequenze di playlist e sequenze di modifica.

In una sequenza di modifica, l'applicazione specifica la durata di ogni segmento in anticipo, prima di avviare la riproduzione. In una sequenza di playlist, l'applicazione non specifica la durata in anticipo. (Infatti, la durata potrebbe non essere nota).

In entrambi i casi, è possibile specificare l'ora di inizio e di fine del supporto del segmento. Queste volte specificano la posizione nel file di origine in cui inizia e termina il segmento. Si supponga, ad esempio, che il file di origine sia lungo 90 secondi. Se si desidera tagliare i primi 10 secondi e gli ultimi 10 secondi, è necessario specificare i valori seguenti:

-   Inizio del supporto: 10 secondi
-   Arresto supporto: 80 secondi

Per specificare l'ora di inizio del supporto, impostare l'attributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) nel nodo di origine. Per specificare l'ora di arresto del supporto, impostare l'attributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) nel nodo di origine.

Per creare una sequenza di modifica, impostare l'attributo dell' [ \_ \_ \_ ora globale della sessione MF](mf-session-global-time-attribute.md) quando si crea la sessione multimediale. In caso contrario, la sessione multimediale prevede sequenze di playlist. In una sequenza di modifica, ogni topologia del segmento deve avere l'attributo [ \_ \_ PROJECTSTART della topologia MF](mf-topology-projectstart-attribute.md) e l'attributo [ \_ \_ PROJECTSTOP della topologia MF](mf-topology-projectstop-attribute.md) .

## <a name="playlist-sequences"></a>Sequenze di playlist

In una sequenza di playlist, il clock di presentazione inizia da zero e continua tra i limiti del segmento. Le origini native forniscono campioni con timestamp uguali al tempo dei supporti. La pipeline converte i timestamp nell'ora di presentazione corretta, come indicato di seguito:

-   Nuovo timestamp = tempo supporto + offset-avvio supporti

Il valore di *offset* è l'ora di presentazione in cui è terminato il segmento precedente. Per il primo segmento, l'offset è zero. Ecco due esempi di come vengono calcolate le conversioni dei timestamp:

-   Esempio 1: si supponga che il primo segmento (S1) sia lungo 10 secondi e che il secondo segmento (S2) abbia un'ora di inizio del supporto pari a zero. L'origine nativa usa il tempo dei supporti per i timestamp, quindi il primo campione da S2 ha un timestamp pari a zero. L'offset è 10 secondi (la durata di S1), quindi l'indicatore di tempo modificato è: 0 + 10 − 0 = 10 secondi.
-   Esempio 2: supporre che il segmento S1 abbia una lunghezza di 10 secondi e che S2 abbia un'ora di inizio media di 5 secondi. Il primo esempio da S2 ha un timestamp di 5 secondi (tempo medio). L'offset è di 10 secondi, quindi l'indicatore di ora modificato è: 5 + 10 − 5 = 10 secondi.

Tutti i componenti della pipeline a valle dei nodi di origine ricevono esempi con i timestamp regolati. I nodi di origine in una topologia possono avere orari di avvio multimediali diversi, quindi le rettifiche vengono calcolate separatamente per ogni ramo della topologia.

Quando la presentazione passa al segmento successivo, il clock di presentazione non viene arrestato o reimpostato e il tempo di presentazione aumenta in modo progressivo. Prima dell'avvio di un nuovo segmento, la sessione multimediale invia all'applicazione un evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) . L'evento specifica l'ora di inizio del segmento, relativa al clock di presentazione e il valore dell'offset. Quando viene avviato un nuovo segmento, la pipeline chiama [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) sull'origine del sequencer con il valore VT \_ Empty. L'origine di Sequencer Invia un evento [MESourceStarted](mesourcestarted.md) senza ora di inizio.

Per la ricerca, l'applicazione specifica un identificatore di segmento più un offset temporale all'interno del segmento. Dopo la ricerca, il clock di presentazione inizia in corrispondenza dell'offset del *segmento* . Di seguito è riportato un esempio del funzionamento del processo:

-   Esempio 3: l'applicazione cerca il segmento S3, con un offset del segmento di 10 secondi. Il clock di presentazione inizia a 10 secondi (offset del segmento). L'offset non include la durata dei segmenti S1 e S2. L'origine del sequencer Invia un evento [MESourceStarted](mesourcestarted.md) con un'ora di inizio uguale all'offset del segmento, 10 secondi.

Dopo una ricerca, se la riproduzione continua fino al segmento successivo, la transizione funziona esattamente come gli esempi precedenti, ad eccezione del fatto che l'offset non include i segmenti ignorati.

Di seguito sono riportati alcuni altri dettagli che influiscono sul timestamp degli esempi:

-   I decodificatori potrebbero richiedere dati oltre l'ora di arresto del supporto. La pipeline estrae il maggior quantità di dati dall'origine come richiesto dal decodificatore e quindi taglia gli esempi di output del decodificatore.
-   Le trasformazioni potrebbero memorizzare dati nel buffer. Ad esempio, potrebbe essere necessario un effetto audio. Quando un segmento termina, il timestamp dell'ultimo campione dalla trasformazione è precedente alla fine del segmento, perché la trasformazione trattiene alcuni dati. Quando viene avviato il segmento successivo, il timestamp del primo campione è leggermente precedente all'inizio del segmento. Non vi è alcun gap negli indicatori temporali, quindi i dati che raggiungono il sink multimediale sono continui. Al termine del segmento finale, la pipeline svuota la trasformazione, quindi non viene perso alcun dato.
-   Potrebbe essere necessario avviare l'origine leggermente prima dell'ora di inizio del supporto, per prelevare il fotogramma chiave precedente. Quindi, dopo la regolazione, il primo campione potrebbe avere un tempo di presentazione negativo.

## <a name="editing-sequences"></a>Modifica di sequenze

In una sequenza di modifica, l'applicazione specifica i limiti del segmento in anticipo, impostando la topologia [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) e [**MF \_ topologia \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributi. La pipeline calcola le regolazioni per gli indicatori temporali nello stesso modo di una sequenza di playlist:

-   Per l'offset, viene usato il valore della [**\_ topologia MF \_ PROJECTSTART**](mf-topology-projectstart-attribute.md), invece di usare l'estremità osservata del segmento.

-   Per la ricerca, l'offset usa un valore uguale al valore [**\_ \_ PROJECTSTART della topologia MF**](mf-topology-projectstart-attribute.md) del segmento più l'offset del segmento.

Pertanto, l'ora di presentazione in una sequenza di modifica è sempre relativa all'inizio della presentazione, anche se l'applicazione cerca un altro segmento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



