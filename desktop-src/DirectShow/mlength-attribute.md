---
description: L'attributo mlength specifica la durata di un file di origine. Questo valore deve essere la durata effettiva o possono verificarsi errori di rendering.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Attributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2aac65cd917fe99e296298bac425e0ff76ca18fc51c82e9294eaedf0ef1c23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051151"
---
# <a name="mlength-attribute"></a>Attributo mlength

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`mlength`L'attributo specifica la durata di un file di origine. Questo valore deve essere la durata effettiva o possono verificarsi errori di rendering.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa nel formato *hh:mm:ss.ff,* dove *hh* = ore, mm = *minuti,* *ss* = secondi e *ff* = frazioni di secondi. Esempio: 1:04:30.512. Le unità iniziali possono essere omesse. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



