---
description: L'attributo mute specifica lo stato di disattivazione dell'audio dell'oggetto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Attributo mute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d89632e632ec4dbf0fe76a915e073baa769044fa1eaad455c16dd3065dc1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791041"
---
# <a name="mute-attribute"></a>Attributo mute

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`mute`L'attributo specifica lo stato di disattivazione dell'audio dell'oggetto. Se il valore è **TRUE,** non viene eseguito il rendering dell'oggetto né dei relativi elementi figlio. Se il valore è **FALSE,** viene eseguito il rendering dell'oggetto e dei relativi elementi figlio in base al proprio stato mute. Il valore predefinito è **FALSE.**

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**clip,**](clip-element.md) [**composito,**](composite-element.md) [**effetto,**](effect-element.md) [**gruppo,**](group-element.md) [**sequenza temporale,**](timeline-element.md) [**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



