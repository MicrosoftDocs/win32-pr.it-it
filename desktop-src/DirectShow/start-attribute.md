---
description: L'attributo Start specifica l'ora di inizio di un oggetto, relativa all'oggetto padre.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Attributo Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316329"
---
# <a name="start-attribute"></a>Attributo Start

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `start` attributo specifica l'ora di inizio di un oggetto, relativa all'oggetto padre.

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

 

 



