---
description: Specifica il compromesso tra la qualità e la velocità di codifica. Questa proprietà è valida in tutte le modalità di controllo della frequenza.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Proprietà AVEncCommonQualityVsSpeed (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125244"
---
# <a name="avenccommonqualityvsspeed-property"></a>Proprietà AVEncCommonQualityVsSpeed

Specifica il compromesso tra la qualità e la velocità di codifica. Questa proprietà è valida in tutte le modalità di controllo della frequenza.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore | Descrizione                      |
|-------|----------------------------------|
| 0     | Qualità inferiore, codifica più veloce.  |
| 100   | Maggiore qualità, codifica più lenta. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




