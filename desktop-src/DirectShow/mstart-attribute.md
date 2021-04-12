---
description: L'attributo mstart specifica l'ora di inizio di una clip, relativa al file multimediale originale.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Attributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480757"
---
# <a name="mstart-attribute"></a>Attributo mstart

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `mstart` attributo specifica l'ora di inizio di una clip, relativa al file multimediale originale.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi. Esempio: 1:04:30.512. È possibile omettere le unità iniziali. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



