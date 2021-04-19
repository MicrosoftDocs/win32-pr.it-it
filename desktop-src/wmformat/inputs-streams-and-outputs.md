---
title: Input, flussi e output
description: Input, flussi e output
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows Media Format SDK, input
- Windows Media Format SDK, flussi
- Windows Media Format SDK, output
- Advanced Systems Format (ASF), input
- ASF (formato avanzato dei sistemi), input
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- ASF (Advanced Systems Format), output
- ASF (formato avanzato dei sistemi), output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6b6941a990b108c16b49648ec0d8d028a44d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298693"
---
# <a name="inputs-streams-and-outputs"></a>Input, flussi e output

Un "input" in questa documentazione è qualsiasi flusso di dati multimediali digitali, ad esempio audio o video, che l'applicazione recapita all'oggetto writer da un'origine usando le API appropriate. Gli input devono essere recapitati in un formato supportato. Sono supportati come input diversi formati RGB e YUV standard e i codec audio supportano il PCM. Se un formato di input specificato non è supportato in modo nativo dal codec, l'oggetto writer creerà un'istanza di un oggetto helper audio o video in grado di convertire un'ampia gamma di formati in formati che possono essere accettati dal codec. Per gli input audio, l'oggetto helper modificherà la profondità del bit, la frequenza di campionamento e il numero di canali in base alle esigenze. Per gli input video, l'oggetto helper video eseguirà le conversioni dello spazio del colore e le regolazioni delle dimensioni del rettangolo. In alcuni casi, i dati audio e video compressi possono essere passati in un flusso di input. Un input può essere di un altro tipo di supporto oltre a audio e video, ad esempio testo, comandi di script, immagini ancora o dati di file arbitrari.

Un "output" in questa documentazione si riferisce ai dati che l'oggetto Reader passa a un'applicazione per il rendering. Un output equivale a un singolo flusso al momento della riproduzione. Se si usa l'esclusione reciproca, tutti i flussi che si escludono a vicenda condividono un singolo output. In genere, i dati di output sono sotto forma di dati audio o video non compressi, sebbene possano contenere qualsiasi tipo di dati. I formati di output video supportati sono elencati altrove in questa documentazione.

Il termine "flusso" in questa documentazione fa riferimento ai dati in un file ASF, anziché (1) i dati di origine di input prima che vengano elaborati dall'oggetto writer e (2) i dati di output dopo che sono stati decompressi dall'oggetto Reader. Un flusso ASF contiene dati provenienti da un singolo input nell'oggetto writer, anche se è possibile creare più di un flusso dallo stesso input. Un flusso ha lo stesso formato e le stesse impostazioni di compressione dall'inizio alla fine. Un file ASF semplice include due flussi, uno per audio e uno per i video. Un file più complesso potrebbe avere due flussi audio e diversi flussi video. I flussi audio possono avere le stesse impostazioni di compressione, ma contengono contenuto diverso, ad esempio una narrazione in linguaggi diversi. I flussi video possono contenere lo stesso contenuto, ma hanno impostazioni di compressione diverse. Nel profilo vengono specificati il formato multimediale e le impostazioni di compressione che l'oggetto writer applicherà a ogni flusso.

La relazione tra input, flussi e output può essere di tre tipi di base. I tre diagrammi seguenti illustrano le relazioni.

Nella relazione più semplice, che è un profilo senza alcuna esclusione reciproca, ogni input viene elaborato dal writer e inserito nel file ASF come un singolo flusso. Durante la riproduzione, il lettore legge il flusso e recapita campioni non compressi come singolo output, come illustrato nel diagramma seguente.

![diagramma che mostra la relazione normale tra input, flussi e output.](images/formatsdk03.png)

Una relazione più complessa si verifica quando viene usata l'esclusione reciproca A più velocità in bit. In questo caso, un singolo input viene elaborato dal writer e codificato a più velocità in bit. Ogni codifica dei dati viene inserita nel file ASF come flusso separato. Al momento della riproduzione, il lettore determina il flusso da decomprimere in base alla larghezza di banda disponibile. Il lettore legge quindi il flusso selezionato e recapita campioni non compressi come output singolo, come illustrato nella figura seguente.

![diagramma che mostra le relazioni tra input, flussi e output quando si usa l'esclusione reciproca a più velocità in bit.](images/formatsdk04.png)

Il terzo tipo di relazione può verificarsi quando viene utilizzata un'esclusione reciproca basata su linguaggio o personalizzata. In questa relazione, più input vengono elaborati dal lettore e ognuno viene inserito nel file ASF come singolo flusso. Durante la riproduzione, l'applicazione seleziona manualmente il flusso da decomprimere in base alla logica fornita. Il lettore legge quindi il flusso selezionato e recapita campioni non compressi come singolo output. Questo processo può essere usato per includere Soundtrack in più linguaggi. La figura seguente illustra questo processo.

![diagramma che mostra le relazioni tra input, flussi e output quando si usa l'esclusione reciproca personalizzata.](images/formatsdk02.png)

Esistono alcune variazioni nelle relazioni descritte in precedenza. Un file può includere, ad esempio, tutte e tre le relazioni o una o due. È anche possibile che alcuni input siano compressi, nel qual caso il writer non esegue alcuna compressione aggiuntiva. Il lettore può inoltre fornire esempi compressi. Tuttavia, quando si esegue questa operazione, è necessario accedervi in base al numero di flusso, non in base al numero di output.

> [!Note]  
> Input, vapori e output sono tutti numeri assegnati dagli oggetti di Windows Media Format SDK. I flussi hanno un numero di flusso, che è basato su 1, definito nel profilo. A ogni flusso viene assegnato anche un indice del flusso da usare per l'enumerazione dei flussi in un profilo. Nessuno di questi numeri è garantito che siano coerenti tra loro. Ovvero, il numero di input 1 potrebbe non corrispondere al flusso numero 1, il flusso numero 1 potrebbe non corrispondere all'indice di flusso 1 e così via.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Esclusione reciproca**](mutual-exclusion.md)
</dt> </dl>

 

 




