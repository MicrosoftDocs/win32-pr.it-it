---
description: L'attributo framerate specifica un framerate, in frame al secondo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Attributo framerate (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965656"
---
# <a name="framerate-attribute-directshow"></a>Attributo framerate (DirectShow)

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `framerate` attributo specifica un framerate, in frame al secondo.

## <a name="possible-values"></a>Valori possibili

Valore a virgola mobile. Il valore deve includere lo zero iniziali prima della posizione decimale. Ad esempio, 0,3, not. 3. Non usare più di sette cifre decimali.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md), [**gruppo**](group-element.md), [**sequenza temporale**](timeline-element.md)

## <a name="remarks"></a>Commenti

Per l'elemento **clip** , questo attributo specifica la frequenza dei fotogrammi predefinita dell'origine. Specificare l'attributo per le sequenze andDIB di immagini ancora. Per un'immagine ancora, impostare il valore su zero. Per una sequenza DIB, usare un valore diverso da zero. Il valore predefinito è zero.

Per l'elemento **Group** , questo attributo specifica la frequenza dei fotogrammi di output per il gruppo.

Per l'elemento **Timeline** , questo attributo specifica la frequenza dei fotogrammi predefinita per tutti i gruppi.

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

 

 



