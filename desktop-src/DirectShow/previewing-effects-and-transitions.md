---
description: Anteprima di effetti e transizioni
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Anteprima di effetti e transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baa5f35511ca9b01990e1c3e0562a3a564204a52026c08e2e2827c154b166b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748301"
---
# <a name="previewing-effects-and-transitions"></a>Anteprima di effetti e transizioni

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Il rendering di alcuni effetti e transizioni può richiedere un tempo relativamente lungo. Durante l'anteprima, questo può causare la distrazione o la sincronizzazione del video con l'audio. È possibile aumentare la velocità di anteprima disabilitando gli effetti o le transizioni:

-   Per disabilitare tutti gli effetti, chiamare [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).
-   Per disabilitare tutte le transizioni, chiamare [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).
-   Per disabilitare una particolare transizione, chiamare [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).

Quando gli effetti sono disabilitati, non ne viene eseguito il rendering durante l'anteprima. Quando una transizione è disabilitata, viene eseguito il rendering come taglio di salto. L'elemento segue tra le tracce si verifica ancora, ma non viene eseguito il rendering dell'effetto visivo.

Se non è possibile eseguire il rendering di un effetto o di una transizione, il motore di rendering sostituisce un effetto o una transizione predefinita. Chiamare il [**metodo IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) per impostare l'effetto predefinito e il metodo [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) per impostare la transizione predefinita. Se non si specifica un valore predefinito o se quello specificato genera anche un errore, DES usa il proprio valore predefinito.

> [!Note]  
> È anche possibile migliorare la qualità dell'anteprima aumentando la quantità di buffering dei frame. Vedere [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



