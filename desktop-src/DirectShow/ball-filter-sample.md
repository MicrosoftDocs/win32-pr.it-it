---
description: Esempio di filtro palla
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Esempio di filtro palla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876958"
---
# <a name="ball-filter-sample"></a>Esempio di filtro palla

## <a name="description"></a>Descrizione

Il filtro palla è un filtro di origine video che produce un'immagine di una palla da rimbalzo. Questo esempio illustra la negoziazione del formato e l'uso delle classi di base del filtro di origine [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

Il codice in Fball. h e Fball. cpp gestisce le interfacce del filtro. Questi due file contengono approssimativamente il codice minimo necessario per un filtro di origine. I file Ball. h e Ball. cpp contengono il codice che rimbalza sulla palla.

Questo filtro ha un singolo pin di output, che fornisce un flusso video che mostra una palla che rimbalza nel frame. Il filtro palla accetta anche richieste di gestione di qualità dal filtro downstream, che illustra una semplice strategia di gestione della qualità. Questo filtro implementa l'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a tale scopo.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: \[ *SDK radice* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Ball.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



