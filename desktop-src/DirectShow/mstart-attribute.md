---
description: L'attributo mstart specifica l'ora di inizio di un clip rispetto al file multimediale originale.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Attributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050951"
---
# <a name="mstart-attribute"></a>Attributo mstart

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`mstart`L'attributo specifica l'ora di inizio di un clip rispetto al file multimediale originale.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa nel formato *hh:mm:ss.ff,* dove *hh* = ore, mm = *minuti,* *ss* = secondi e *ff* = frazioni di secondi. Esempio: 1:04:30.512. Le unità iniziali possono essere omesse. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



