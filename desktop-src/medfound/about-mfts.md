---
description: Informazioni su MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Informazioni su MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09adce4bc93c110cf98e4fd8ed427ffcd009c3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879398"
---
# <a name="about-mfts"></a>Informazioni su MFTs

Le trasformazioni Media Foundation (MFTs) forniscono un modello generico per l'elaborazione dei dati multimediali. MFTs vengono usati per i decodificatori, i codificatori e i processori di segnale digitale (DSP). In breve, tutto ciò che si trova nella pipeline multimediale tra l'origine multimediale e il sink multimediale è un MFT.

Per la maggior parte delle applicazioni, i dettagli dell'elaborazione dei dati MFT sono nascosti da livelli più elevati dell'architettura Media Foundation. Molte applicazioni Media Foundation non effettueranno mai una chiamata diretta a un MFT. Tuttavia, è certamente possibile ospitare un MFT direttamente nell'applicazione.

MFTs sono un'evoluzione del modello Transform introdotto per la prima volta con DirectX Media Objects (DMOs). Di fatto, è relativamente facile creare una trasformazione che supporti entrambi i modelli. Rispetto a DMOs, i comportamenti necessari di MFTs sono specificati in modo più chiaro, semplificando la scrittura di un'implementazione corretta. Inoltre, MFTs può supportare l'elaborazione video con accelerazione hardware.

In questo argomento viene illustrata una breve panoramica del modello di elaborazione MFT, che si concentra sulla progettazione complessiva anziché sulle chiamate di metodo specifiche. Per una descrizione dettagliata, vedere [modello di elaborazione MFT di base](basic-mft-processing-model.md).

## <a name="streams"></a>Flussi

Un MFT presenta flussi di input e flussi di output. I flussi di input ricevono i dati e i flussi di output producono dati. Ad esempio, un decodificatore ha un flusso di input, che riceve i dati codificati e un flusso di output, che produce i dati decodificati.

I flussi in un MFT non sono rappresentati come oggetti COM distinti. Al contrario, ogni flusso ha un identificatore di flusso designato e i metodi nell'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) accettano gli identificatori di flusso come parametri di input.

Alcuni MFTs hanno un numero fisso di flussi. Ad esempio, i decodificatori e i codificatori hanno in genere esattamente un input e un output. Altri MFTs hanno un numero dinamico di flussi. Se una MFT supporta flussi dinamici, il client può aggiungere nuovi flussi di input. Il client non può aggiungere flussi di output, ma MFT potrebbe aggiungere o rimuovere i flussi di output durante l'elaborazione. Ad esempio, i multiplexer consentono in genere al client di aggiungere flussi di input e avere un output per il flusso multiplexato. I Demultiplexer sono l'inverso, con un input ma un numero dinamico di flussi di output, a seconda del contenuto del flusso di input. Nella figura seguente viene illustrata la differenza tra multiplexer e Demultiplexer.

![diagramma che mostra un codificatore/decodificatore (1 input, 1 output), un multiplexer (2 input, 1 output) e un Demultiplexer (1 input, 2 output)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Tipi di supporto

Quando viene creata una MFT, nessuno dei flussi ha un formato consolidato. Prima che il MFT possa elaborare i dati, il client deve impostare i formati per i flussi. Con un decodificatore, ad esempio, il formato di input è il formato di compressione usato nel file di origine originale e il formato di output è un formato non compresso, ad esempio audio PCM o video RGB. I formati dei flussi vengono descritti utilizzando i [tipi di supporto](media-types.md).

A seconda dello stato interno della MFT, potrebbe fornire un elenco di tipi di supporti possibili per ogni flusso. È possibile utilizzare questo elenco come hint quando si impostano i tipi di supporto. Impostando il tipo di supporto in un flusso, è possibile modificare l'elenco dei tipi possibili per un altro flusso. Un decodificatore, ad esempio, non può in genere fornire tipi di output fino a quando il client non imposta il tipo di input. Il tipo di input contiene le informazioni necessarie al decodificatore per restituire un elenco di tipi di output possibili.

Per impostare il tipo di supporto in un flusso, chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) o [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Per ottenere l'elenco dei tipi di supporti possibili per un flusso, chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) o [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Elaborazione dei dati

Quando il client imposta i tipi di supporto nei flussi, il file MFT è pronto per l'elaborazione dei dati. A tale proposito, il client alterna la fornitura di dati di input alla MFT e la ricezione dei dati di output dalla MFT:

-   Per assegnare i dati di input a MFT, chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Per eseguire il pull dei dati di output dalla MFT, chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Il metodo [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) accetta un puntatore a un esempio multimediale allocato dal client. L'esempio multimediale contiene uno o più buffer e ogni buffer contiene i dati di input per l'elaborazione di MFT.

Il metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) supporta due modelli di allocazione diversi: il MFT alloca i buffer di output o il client alloca i buffer di output. Alcuni MFTs supportano entrambi i modelli di allocazione, ma non è necessario che un MFT supporti entrambi. Ad esempio, un MFT potrebbe richiedere al client di allocare i buffer di output. Il metodo [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce informazioni su un flusso di output, incluso il modello di allocazione supportato da MFT.

MFTs sono progettati per memorizzare nel buffer il minor quantità possibile di dati, in modo da ridurre al minimo la latenza nella pipeline. Pertanto, in un determinato momento, la MFT può segnalare una delle condizioni seguenti:

-   Il MFT richiede più dati di input. In questo stato, il MFT non può produrre output finché il client non chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) almeno una volta.
-   In MFT non verrà accettato alcun input finché il client non chiamerà [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) almeno una volta.

Si supponga, ad esempio, di usare un decodificatore video per decodificare un flusso video che contiene una combinazione di fotogrammi chiave e frame Delta. Inizialmente, il MFT richiede un input prima di poter decodificare eventuali frame. Il client chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per recapitare il primo frame. Si supponga che il primo frame sia un frame Delta, illustrato nel diagramma seguente come "P" per il frame stimato. Il decodificatore utilizza questo frame, ma non può produrre alcun output finché non ottiene il fotogramma chiave successivo.

![diagramma che mostra il MFT che necessita di input, che punta a un frame stimato](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

Il client continua a chiamare [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e infine raggiunge il fotogramma chiave successivo, illustrato nel diagramma seguente come ' I ' per il frame intra-codificato. Il decodificatore dispone ora di un numero sufficiente di frame per iniziare la decodifica. A questo punto interrompe l'accettazione dell'input e il client deve chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere i frame decodificati.

![diagramma che mostra un MFT che non accetta input, puntando a un frame intra-codificato e a tre frame stimati](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

L'approccio più semplice per il client è semplicemente quello di effettuare chiamate alternative a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un algoritmo più sofisticato è descritto nell'argomento [modello di elaborazione MFT di base](basic-mft-processing-model.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



