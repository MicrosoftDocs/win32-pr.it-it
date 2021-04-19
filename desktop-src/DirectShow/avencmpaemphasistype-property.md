---
description: Specifica il tipo di filtro di deenfasi da usare durante la decodifica. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Proprietà AVEncMPAEmphasisType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304147"
---
# <a name="avencmpaemphasistype-property"></a>Proprietà AVEncMPAEmphasisType

Specifica il tipo di filtro di deenfasi da usare durante la decodifica. Questa proprietà si applica ai codificatori audio MPEG.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .

## <a name="remarks"></a>Commenti

Questa proprietà imposta i bit di enfasi nell'intestazione del frame.

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

 

