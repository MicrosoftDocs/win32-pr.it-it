---
description: L'attributo mute specifica lo stato di silenziamento dell'oggetto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Disattiva attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124899"
---
# <a name="mute-attribute"></a>Disattiva attributo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `mute` attributo specifica lo stato di silenziamento dell'oggetto. Se il valore è **true**, né l'oggetto né i relativi elementi figlio vengono sottoposti a rendering. Se il valore è **false**, viene eseguito il rendering dell'oggetto e viene eseguito il rendering dei relativi elementi figlio in base al relativo stato di silenziamento. Il valore predefinito è **false**.

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md), [**composito**](composite-element.md), [**effetto**](effect-element.md), [**gruppo**](group-element.md), [**sequenza temporale**](timeline-element.md), [**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj:: semutato**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



