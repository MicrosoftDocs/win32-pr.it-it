---
description: L'attributo Lock specifica se un oggetto deve essere modificato. Se il valore è TRUE, l'applicazione deve considerare l'oggetto come bloccato e non consentire le modifiche apportate a tale oggetto o ai relativi elementi figlio. Il valore predefinito è FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: Blocca attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7716f047e0df47ffb5e84cb2de0e9fe345836b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747194"
---
# <a name="lock-attribute"></a>Blocca attributo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `lock` attributo specifica se un oggetto deve essere modificato. Se il valore è **true**, l'applicazione deve considerare l'oggetto come bloccato e non consentire le modifiche apportate a tale oggetto o ai relativi elementi figlio. Il valore predefinito è **false**.

## <a name="possible-values"></a>Valori possibili

Valori possibili i valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md), [**composito**](composite-element.md), [**effetto**](effect-element.md), [**gruppo**](group-element.md), [**sequenza temporale**](timeline-element.md), [**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj:: selocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



