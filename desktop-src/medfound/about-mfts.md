---
description: Informazioni sulle MFT
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Informazioni sulle MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035714"
---
# <a name="about-mfts"></a>Informazioni sulle MFT

Media Foundation trasformazioni (MFT) forniscono un modello generico per l'elaborazione dei dati multimediali. Le MFT vengono usate per decodificatori, codificatori e processori di segnali digitali (DSP). In breve, tutto ciò che si trova nella pipeline multimediale tra l'origine multimediale e il sink multimediale è un MFT.

Per la maggior parte delle applicazioni, i dettagli dell'elaborazione dei dati MFT sono nascosti dai livelli superiori dell'Media Foundation architettura. Molte Media Foundation non effettuano mai una chiamata diretta a un MFT. Tuttavia, è certamente possibile ospitare un MFT direttamente nell'applicazione.

Le MFT sono un'evoluzione del modello di trasformazione introdotto per la prima volta con DirectX Media Objects (DMO). In realtà, è relativamente semplice creare una trasformazione che supporti entrambi i modelli. Rispetto alle DMO, i comportamenti necessari delle MFT sono più chiaramente specificati, semplificando la scrittura di un'implementazione corretta. Inoltre, i MFT possono supportare l'elaborazione video con accelerazione hardware.

Questo argomento offre una breve panoramica del modello di elaborazione MFT, concentrandosi sulla progettazione complessiva anziché sulle chiamate di metodo specifiche. Per una descrizione più dettagliata e dettagliata, vedere Modello di [elaborazione MFT di base](basic-mft-processing-model.md).

## <a name="streams"></a>Flussi

Un MFT include flussi di input e flussi di output. I flussi di input ricevono dati e i flussi di output producono dati. Ad esempio, un decodificatore ha un flusso di input, che riceve i dati codificati, e un flusso di output, che produce i dati decodificati.

I flussi in un MFT non sono rappresentati come oggetti COM distinti. Ogni flusso ha invece un identificatore di flusso designato e i metodi [**nell'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) accettano gli identificatori di flusso come parametri di input.

Alcuni MFT hanno un numero fisso di flussi. Ad esempio, decodificatori e codificatori hanno in genere esattamente un input e un output. Altri MFT hanno un numero dinamico di flussi. Se un MFT supporta flussi dinamici, il client può aggiungere nuovi flussi di input. Il client non può aggiungere flussi di output, ma il MFT potrebbe aggiungere o rimuovere i flussi di output durante l'elaborazione. Ad esempio, i multiplexer consentono in genere al client di aggiungere flussi di input e di avere un output per il flusso multiplexed. I demultiplex sono il contrario, con un input ma un numero dinamico di flussi di output, a seconda del contenuto del flusso di input. La figura seguente illustra la differenza tra multiplexer e demultiplexer.

![diagramma che mostra un codificatore/decodificatore (1 input, 1 output), un multiplexer (2 input, 1 output) e un demultiplexer (1 input, 2 output)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Tipi di supporti

Quando viene creato un MFT per la prima volta, nessuno dei flussi ha un formato stabilito. Prima che MFT possa elaborare i dati, il client deve impostare i formati per i flussi. Ad esempio, con un decodificatore, il formato di input è il formato di compressione usato nel file di origine originale e il formato di output è un formato non compresso, ad esempio audio PCM o video RGB. I formati di flusso vengono descritti usando [i tipi di supporto](media-types.md).

A seconda dello stato interno di MFT, potrebbe fornire un elenco di possibili tipi di supporti per ogni flusso. È possibile usare questo elenco come suggerimento quando si impostano i tipi di supporti. L'impostazione del tipo di supporto in un flusso può modificare l'elenco dei tipi possibili per un altro flusso. Ad esempio, un decodificatore in genere non può fornire alcun tipo di output finché il client non imposta il tipo di input. Il tipo di input contiene le informazioni necessarie al decodificatore per restituire un elenco di possibili tipi di output.

Per impostare il tipo di supporto in un flusso, chiamare [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) o [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Per ottenere l'elenco dei tipi di supporti possibili per un flusso, chiamare [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) o [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Elaborazione dei dati

Dopo che il client ha impostato i tipi di supporti nei flussi, MFT è pronto per elaborare i dati. A tale scopo, il client alterna la fornitura di dati di input al MFT e il recupero dei dati di output da MFT:

-   Per assegnare dati di input all'MFT, chiamare [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Per eseguire il pull dei dati di output da MFT, chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Il [**metodo ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) accetta un puntatore a un campione multimediale allocato dal client. L'esempio di supporto contiene uno o più buffer e ogni buffer contiene dati di input per l'elaborazione di MFT.

Il [**metodo ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) supporta due diversi modelli di allocazione: MFT alloca i buffer di output o il client alloca i buffer di output. Alcuni MFT supportano entrambi i modelli di allocazione, ma non è necessario che un MFT supporti entrambi. Ad esempio, un MFT potrebbe richiedere al client di allocare i buffer di output. Il [**metodo IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) restituisce informazioni su un flusso di output, incluso il modello di allocazione che supporta MFT.

Le MFT sono progettate per eseguire il buffer del meno possibile sui dati, in modo da ridurre al minimo la latenza nella pipeline. Pertanto, in qualsiasi momento, MFT può segnalare una delle condizioni seguenti:

-   MFT richiede più dati di input. In questo stato, MFT non può produrre output finché il client non chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) almeno una volta.
-   MFT non accetterà più input finché il client non chiama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) almeno una volta.

Si supponga, ad esempio, di usare un decodificatore video per decodificare un flusso video contenente una combinazione di fotogrammi chiave e fotogrammi differenziali. Inizialmente, MFT richiede un input prima di poter decodificare i fotogrammi. Il client chiama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per recapitare il primo frame. Si supponga che il primo frame sia un frame differenziale (illustrato nel diagramma seguente come "P" per il frame previsto). Il decodificatore mantiene questo fotogramma, ma non può produrre alcun output finché non ottiene il fotogramma chiave successivo.

![diagramma che mostra l'mft che richiede input, che punta a un frame previsto](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

Il client continua a chiamare [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e raggiunge infine il fotogramma chiave successivo (illustrato nel diagramma successivo come "I" per frame intra-codificato). Il decodificatore ha ora un numero di fotogrammi sufficiente per avviare la decodifica. A questo punto smette di accettare l'input e il client deve chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere i frame decodificati.

![diagramma che mostra un mft che non accetta input, che punta a un frame intracodato e a tre fotogrammi stimati](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

L'approccio più semplice per il client consiste semplicemente nell'alternare le chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un algoritmo più sofisticato è descritto nell'argomento [Modello di elaborazione MFT di base](basic-mft-processing-model.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 



