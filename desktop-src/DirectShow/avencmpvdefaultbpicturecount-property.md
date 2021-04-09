---
description: Specifica il numero predefinito di fotogrammi B consecutivi tra I frame I e P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Proprietà AVEncMPVDefaultBPictureCount (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049025"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Proprietà AVEncMPVDefaultBPictureCount

Specifica il numero predefinito di fotogrammi B consecutivi tra I frame I e P.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Prima di Windows 8, questa proprietà si applica ai codificatori video MPEG. A partire da Windows 8, questa proprietà viene usata dai codificatori video MPEG, WMV e H. 264.

Se il codificatore supporta questa proprietà, può essere usato per controllare la struttura del Group of Pictures (GOP).

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

 

 




