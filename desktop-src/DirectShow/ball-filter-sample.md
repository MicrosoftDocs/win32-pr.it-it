---
description: Esempio di filtro a sfera
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Esempio di filtro a sfera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df215f6f4be5fa1bc94872ac4e5855d4e9c0f19a136708d0c9377b19c5d79dda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084541"
---
# <a name="ball-filter-sample"></a>Esempio di filtro a sfera

## <a name="description"></a>Descrizione

Il filtro palla è un filtro sorgente video che produce un'immagine di una palla che rimbalza. Questo esempio illustra la negoziazione del formato e l'uso delle classi di base del filtro di origine [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

Il codice in Fball.h e Fball.cpp gestisce le interfacce di filtro. Questi due file contengono approssimativamente il codice minimo necessario per un filtro di origine. I file Ball.h e Ball.cpp contengono il codice che rimbalza la palla.

Questo filtro ha un singolo pin di output, che fornisce un flusso video che mostra una palla che rimbalza nel fotogramma. Il filtro Ball accetta anche le richieste di gestione della qualità dal filtro downstream, che illustra una semplice strategia di gestione della qualità. Questo filtro implementa [**l'interfaccia IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a tale scopo.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: \[ *SDK Root* \] \\ Samples Multimedia DirectShow \\ Filters \\ \\ \\ Ball.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



