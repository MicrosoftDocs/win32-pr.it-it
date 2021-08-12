---
description: Questo argomento descrive il modo in cui l'origine Sequencer gestisce gli orari di presentazione durante la riproduzione.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Tempi di presentazione delle sequenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45ea9c8b315171365810f33bb9a66ca4d223fb2119d7aea19288c3ebdd93ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238367"
---
# <a name="sequence-presentation-times"></a>Tempi di presentazione delle sequenze

Questo argomento descrive il modo in cui [l'origine Sequencer gestisce](sequencer-source.md) gli orari di presentazione durante la riproduzione.

## <a name="overview"></a>Panoramica

L'origine sequencer supporta due modalità diverse: sequenze di playlist e sequenze di modifica.

In una sequenza di modifica, l'applicazione specifica la durata di ogni segmento in anticipo, prima di avviare la riproduzione. In una sequenza di playlist, l'applicazione non specifica la durata in anticipo. In realtà, la durata potrebbe non essere nota.

In entrambi i casi, è possibile specificare l'ora di inizio e di arresto dei supporti di un segmento. Queste volte specificano la posizione nel file di origine in cui inizia e termina il segmento. Si supponga, ad esempio, che il file di origine sia lungo 90 secondi. Se si desidera tagliare i primi 10 secondi e gli ultimi 10 secondi, è necessario specificare i valori seguenti:

-   Avvio del supporto: 10 secondi
-   Arresto dei supporti: 80 secondi

Per specificare l'ora di inizio del supporto, impostare [l'attributo \_ MF TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) nel nodo di origine. Per specificare l'ora di arresto del supporto, impostare [l'attributo \_ MF TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) nel nodo di origine.

Per creare una sequenza di modifica, impostare [l'attributo MF \_ SESSION \_ GLOBAL \_ TIME](mf-session-global-time-attribute.md) quando si crea la sessione multimediale. In caso contrario, la sessione multimediale prevede sequenze di playlist. In una sequenza di modifica, ogni topologia di segmento deve avere l'attributo [ \_ \_ PROJECTSTART](mf-topology-projectstart-attribute.md) della topologia MF e [l'attributo MF \_ TOPOLOGY \_ PROJECTSTOP.](mf-topology-projectstop-attribute.md)

## <a name="playlist-sequences"></a>Sequenze di playlist

In una sequenza di playlist, l'orologio di presentazione inizia da zero e continua oltre i limiti dei segmenti. Le origini native forniscono esempi con timestamp uguali all'ora del supporto. La pipeline converte i timestamp nell'ora di presentazione corretta come indicato di seguito:

-   Nuovo timestamp = ora supporto + offset – avvio del supporto

Il valore di *offset è* l'ora di presentazione in cui è terminato il segmento precedente. Per il primo segmento, l'offset è zero. Di seguito sono riportati due esempi di come vengono calcolate queste conversioni di timestamp:

-   Esempio 1: si supponga che il primo segmento (S1) sia lungo 10 secondi e che il secondo segmento (S2) abbia un'ora di inizio media pari a zero. L'origine nativa usa l'ora dei supporti per i timestamp, quindi il primo campione di S2 ha un timestamp pari a zero. L'offset è di 10 secondi (durata di S1), quindi il timestamp regolato è:0 + 10 x 0 = 10 secondi.
-   Esempio 2: si supponga che il segmento S1 sia lungo 10 secondi e che S2 abbia un'ora di inizio multimediale di 5 secondi. Il primo esempio di S2 ha un timestamp di 5 secondi (tempo multimediale). L'offset è di 10 secondi, quindi il timestamp regolato è:5 + 10 x 5 = 10 secondi.

Tutti i componenti della pipeline a valle dai nodi di origine ricevono esempi con i timestamp modificati. I nodi di origine in una topologia possono avere orari di inizio dei supporti diversi, quindi le rettifiche vengono calcolate separatamente per ogni ramo della topologia.

Quando la presentazione passa al segmento successivo, l'orologio della presentazione non si arresta o si reimposta e il tempo di presentazione aumenta in modo monotono. Prima dell'avvio di un nuovo segmento, la sessione multimediale invia all'applicazione un evento [MESessionNotifyPresentationTime.](mesessionnotifypresentationtime.md) L'evento specifica l'ora di inizio del segmento, rispetto all'orologio di presentazione e il valore dell'offset. Quando viene avviato un nuovo segmento, la pipeline chiama [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) nell'origine sequencer con il valore VT \_ EMPTY. L'origine sequencer invia un [evento MESourceStarted](mesourcestarted.md) senza ora di inizio.

Per la ricerca, l'applicazione specifica un identificatore di segmento più una scostamento temporale all'interno del segmento. Dopo la ricerca, l'orologio di presentazione inizia in corrispondenza *dell'offset del* segmento. Di seguito è riportato un esempio del funzionamento di tale processo:

-   Esempio 3: l'applicazione cerca di segmentare S3, con un offset di segmento di 10 secondi. L'orologio di presentazione inizia a 10 secondi (offset del segmento). L'offset non include la durata dei segmenti S1 e S2. L'origine sequencer invia un [evento MESourceStarted](mesourcestarted.md) con un'ora di inizio uguale all'offset del segmento, 10 secondi.

Dopo una ricerca, se la riproduzione continua con il segmento successivo, la transizione funziona esattamente come gli esempi precedenti, ad eccezione del fatto che l'offset non include i segmenti ignorati.

Di seguito sono riportati altri dettagli che influiscono sul timestamp degli esempi:

-   I decodificatori potrebbero richiedere dati oltre l'ora di arresto del supporto. La pipeline estrae dall'origine la quantità di dati necessaria per il decodificatore e quindi taglia gli esempi di output del decodificatore.
-   Le trasformazioni potrebbero includere dati nel buffer. Ad esempio, un effetto audio potrebbe dover eseguire questa operazione. Quando termina un segmento, il timestamp dell'ultimo campione della trasformazione è precedente alla fine del segmento, perché la trasformazione contiene alcuni dati. All'avvio del segmento successivo, il timestamp del primo campione è leggermente precedente all'inizio del segmento. I timestamp non sono vuoti, quindi i dati che raggiungono il sink multimediale sono continui. Quando termina il segmento finale, la pipeline svuota la trasformazione, quindi non vengono persi dati.
-   Potrebbe essere necessario che l'origine inizi leggermente prima dell'ora di inizio del supporto per riprendere il fotogramma chiave precedente. Pertanto, dopo la regolazione, il primo campione potrebbe avere un'ora di presentazione negativa.

## <a name="editing-sequences"></a>Modifica di sequenze

In una sequenza di modifica, l'applicazione specifica in anticipo i limiti dei segmenti impostando gli attributi [**\_ \_ MF TOPOLOGY PROJECTSTART**](mf-topology-projectstart-attribute.md) e [**MF \_ TOPOLOGY \_ PROJECTSTOP.**](mf-topology-projectstop-attribute.md) La pipeline calcola le rettifiche per i timestamp quasi come per una sequenza di playlist:

-   Per l'offset, usa il valore di [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)anziché l'estremità osservata del segmento.

-   Per la ricerca, l'offset usa un valore uguale al valore [**\_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) della topologia MF del segmento più l'offset del segmento.

Pertanto, l'ora di presentazione in una sequenza di modifica è sempre relativa all'inizio della presentazione, anche se l'applicazione cerca un altro segmento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 



