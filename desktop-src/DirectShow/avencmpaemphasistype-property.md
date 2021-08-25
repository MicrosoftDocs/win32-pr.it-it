---
description: Specifica il tipo di filtro di de-enfasi che deve essere usato durante la decodifica. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Proprietà AVEncMPAEmphasisType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3da73e2708acde7a5b388d229a3a82c50a2dff04c4f2873551a992fe738189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824231"
---
# <a name="avencmpaemphasistype-property"></a>AVEncMPAEmphasisType - proprietà

Specifica il tipo di filtro di de-enfasi che deve essere usato durante la decodifica. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVEncMPAEmphasisType.**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)

## <a name="remarks"></a>Commenti

Questa proprietà imposta i bit di enfasi nell'intestazione del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

