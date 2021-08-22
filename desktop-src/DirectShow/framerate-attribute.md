---
description: L'attributo framerate specifica una frequenza di fotogrammi, in fotogrammi al secondo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Attributo framerate (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015659"
---
# <a name="framerate-attribute-directshow"></a>Attributo framerate (DirectShow)

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`framerate`L'attributo specifica una frequenza di fotogrammi, in fotogrammi al secondo.

## <a name="possible-values"></a>Valori possibili

Valore a virgola mobile. Il valore deve includere lo zero iniziale prima della posizione decimale. Ad esempio, 0.3, non .3. Non usare più di sette cifre decimali.

## <a name="applies-to"></a>Si applica a

[**clip,**](clip-element.md) [**gruppo,**](group-element.md)sequenza [**temporale**](timeline-element.md)

## <a name="remarks"></a>Commenti

Per **l'elemento clip,** questo attributo specifica la frequenza fotogrammi predefinita dell'origine. Specificare l'attributo per le immagini fisse e le sequenze DIB. Per un'immagine ancorata, impostare il valore su zero. Per una sequenza DIB, usare un valore diverso da zero. Il valore predefinito è zero.

Per **l'elemento group,** questo attributo specifica la frequenza dei fotogrammi di output per il gruppo.

Per **l'elemento della** sequenza temporale, questo attributo specifica la frequenza fotogrammi predefinita per tutti i gruppi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



