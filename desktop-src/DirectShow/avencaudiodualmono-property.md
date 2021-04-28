---
description: "Proprietà AVEncAudioDualMono: specifica se l'audio a 2 canali è codificato come stereo o doppio mono."
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Proprietà AVEncAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096579"
---
# <a name="avencaudiodualmono-property"></a>AVEncAudioDualMono - proprietà

Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncAudioDualMono**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVEncAudioDualMono.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)

## <a name="remarks"></a>Commenti

Questa proprietà non si applica ai codificatori audio MPEG. Per l'audio MPEG, usare la [**proprietà AVEncMPACodingMode.**](avencmpacodingmode-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP per app desktop di Windows 2000 Professional \[ \|\]<br/>                     |
| Server minimo supportato<br/> | App UWP per app desktop di Windows 2000 Server \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

