---
description: L'attributo mstop specifica l'ora di arresto di un clip rispetto al file multimediale originale.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072938"
---
# <a name="mstop-attribute"></a>Attributo mstop

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`mstop`L'attributo specifica l'ora di arresto di un clip rispetto al file multimediale originale.

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

 

 



