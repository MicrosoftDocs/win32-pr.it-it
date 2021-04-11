---
description: L'attributo mstop specifica l'ora di arresto di una clip rispetto al file multimediale originale.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123468"
---
# <a name="mstop-attribute"></a>Attributo mstop

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `mstop` attributo specifica l'ora di arresto di una clip rispetto al file multimediale originale.

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

 

 



