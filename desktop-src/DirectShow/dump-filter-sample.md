---
description: Esempio di filtro dump
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Esempio di filtro dump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522417"
---
# <a name="dump-filter-sample"></a>Esempio di filtro dump

## <a name="description"></a>Descrizione

Il filtro dump è un filtro renderer che scrive gli esempi di supporti ricevuti in un file di testo.

Questo esempio illustra come usare la classe di filtro di base [**CBaseFilter**](cbasefilter.md) e la classe del PIN di input con rendering [**CRenderedInputPin**](crenderedinputpin.md). Viene inoltre illustrato come implementare l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) . Il filtro dump ha un singolo pin di input, che scrive tutti i campioni ricevuti direttamente in un file.

## <a name="usage"></a>Utilizzo

Questo filtro è un utile strumento di debug. Ad esempio, è possibile verificare, bit per bit, i risultati di un filtro di trasformazione. È possibile compilare un grafo manualmente usando GraphEdit e connettere il filtro dump all'output di un filtro di trasformazione o di qualsiasi altro pin di output. È anche possibile connettere un filtro Tee e inserire il filtro dump su una gamba del filtro Tee e l'output tipico su un'altra parte per monitorare i risultati in uno scenario in tempo reale.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ directory radice \] SDK* \\ esempi di \\ \\ filtri DirectShow Multimedia \\ \\ dump.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



