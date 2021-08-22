---
description: Specifica il compromesso tra qualità e velocità della codifica. Questa proprietà è valida in tutte le modalità di controllo della frequenza.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Proprietà AVEncCommonQualityVsSpeed (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9def8fc53a6cf88384a42870ef695294a0117ab3bfdd26ba69c95bd2b02a63b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540881"
---
# <a name="avenccommonqualityvsspeed-property"></a>AVEncCommonQualityVsSpeed - proprietà

Specifica il compromesso tra qualità e velocità della codifica. Questa proprietà è valida in tutte le modalità di controllo della frequenza.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà ha l'intervallo seguente.



| Valore | Descrizione                      |
|-------|----------------------------------|
| 0     | Qualità inferiore, codifica più veloce.  |
| 100   | Maggiore qualità, codifica più lenta. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




