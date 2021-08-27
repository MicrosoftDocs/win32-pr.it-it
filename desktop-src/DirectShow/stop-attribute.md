---
description: L'attributo stop specifica l'ora di arresto di un oggetto rispetto all'oggetto padre.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Attributo stop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050172"
---
# <a name="stop-attribute"></a>Attributo stop

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`stop`L'attributo specifica l'ora di arresto di un oggetto rispetto all'oggetto padre.

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa nel formato *hh:mm:ss.ff,* dove *hh* = ore, mm = *minuti,* *ss* = secondi e *ff* = frazioni di secondi. Esempio: 1:04:30.512. Le unità iniziali possono essere omesse. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="applies-to"></a>Si applica a

[**clip,**](clip-element.md) [**effetto,**](effect-element.md) [**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



