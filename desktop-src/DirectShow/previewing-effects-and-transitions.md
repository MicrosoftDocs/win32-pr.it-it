---
description: Anteprima degli effetti e delle transizioni
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Anteprima degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125079"
---
# <a name="previewing-effects-and-transitions"></a>Anteprima degli effetti e delle transizioni

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Alcuni effetti e transizioni importano un tempo relativamente lungo per il rendering. Durante l'anteprima questo può causare la sincronizzazione del video con l'audio. È possibile aumentare la velocità di anteprima disabilitando gli effetti o le transizioni:

-   Per disabilitare tutti gli effetti, chiamare [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).
-   Per disabilitare tutte le transizioni, chiamare [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).
-   Per disabilitare una particolare transizione, chiamare [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).

Quando gli effetti sono disabilitati, il rendering non viene eseguito durante l'anteprima. Quando una transizione è disabilitata, viene visualizzata come un salto. Il segue tra le tracce si verifica ancora, ma non viene eseguito il rendering dell'effetto visivo.

Se non è possibile eseguire il rendering di un effetto o di una transizione, il motore di rendering sostituisce un effetto predefinito o una transizione. Chiamare il metodo [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) per impostare l'effetto predefinito e il metodo [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) per impostare la transizione predefinita. Se non si specifica un valore predefinito o se quello specificato genera anche un errore, DES usa il proprio valore predefinito.

> [!Note]  
> È anche possibile migliorare la qualità di anteprima aumentando la quantità di buffering dei frame. Vedere [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



