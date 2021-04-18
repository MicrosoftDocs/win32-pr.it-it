---
description: L'attributo Stop specifica l'ora di arresto di un oggetto, relativa all'oggetto padre.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Interrompi attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316304"
---
# <a name="stop-attribute"></a>Interrompi attributo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `stop` attributo specifica l'ora di arresto di un oggetto, relativa all'oggetto padre.

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi. Esempio: 1:04:30.512. È possibile omettere le unità iniziali. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md), [**effetto**](effect-element.md), [**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



