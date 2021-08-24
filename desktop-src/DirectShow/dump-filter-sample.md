---
description: Esempio di filtro dump
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Esempio di filtro dump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5643f0334071b8c238a70ed31eee87de4e93e3637b5403d886d79f2816e39c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148734"
---
# <a name="dump-filter-sample"></a>Esempio di filtro dump

## <a name="description"></a>Descrizione

Dump Filter è un filtro renderer che scrive gli esempi multimediali ricevuti in un file di testo.

Questo esempio illustra come usare la classe di filtro di base [**CBaseFilter**](cbasefilter.md) e la classe di pin di input sottoposta a rendering [**CRenderedInputPin.**](crenderedinputpin.md) Illustra anche come implementare [**l'interfaccia IFileSinkFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) Il filtro Dump ha un singolo pin di input, che scrive ogni campione ricevuto direttamente in un file.

## <a name="usage"></a>Utilizzo

Questo filtro è uno strumento di debug utile. Ad esempio, è possibile verificare, bit per bit, i risultati di un filtro di trasformazione. È possibile compilare un grafo manualmente usando GraphEdit e connettere il filtro Dump all'output di un filtro di trasformazione o di qualsiasi altro pin di output. È anche possibile connettere un filtro tee e inserire il filtro Dump su una parte del filtro tee e l'output tipico in un'altra parte per monitorare i risultati in uno scenario in tempo reale.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Dump.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



