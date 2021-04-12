---
description: L'attributo time specifica l'ora in cui un parametro presuppone un nuovo valore, relativo all'inizio della transizione o dell'effetto.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Time (attributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234205"
---
# <a name="time-attribute"></a>Time (attributo)

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `time` attributo specifica l'ora in cui un parametro presuppone un nuovo valore, relativo all'inizio della transizione o dell'effetto.

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi. Esempio: 1:04:30.512. È possibile omettere le unità iniziali. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="applies-to"></a>Si applica a

[**at**](at-element.md), [ **lineari**](linear-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> </dl>

 

 



