---
description: Specifica il numero predefinito di fotogrammi B consecutivi tra i frame I e P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Proprietà AVEncMPVDefaultBPictureCount (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95604d8b3849175e579d276fa006f5a8c4d2833a167228316c4cf830b01618b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276261"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>AVEncMPVDefaultBPictureCount - proprietà

Specifica il numero predefinito di fotogrammi B consecutivi tra i frame I e P.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Prima di Windows 8, questa proprietà si applica ai codificatori video MPEG. A partire Windows 8, questa proprietà viene usata dai codificatori video MPEG, WMV e H.264.

Se il codificatore supporta questa proprietà, può essere usata per controllare la struttura del gruppo di immagini (GOP).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




