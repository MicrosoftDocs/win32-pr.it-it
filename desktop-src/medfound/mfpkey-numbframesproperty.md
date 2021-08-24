---
description: Specifica il numero di fotogrammi predittivi bidirezionali (fotogrammi B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcf103da1d629c90209aef4badd604651d73af3e9101cac0f613b47c82883e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555420"
---
# <a name="mfpkey_numbframes-property"></a>Proprietà MFPKEY \_ NUMBFRAMES

Specifica il numero di fotogrammi predittivi bidirezionali (fotogrammi B).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo di dati

VT-I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Per impostazione predefinita, Windows Media Video 9 usa solo intraframe (fotogrammi I), noti anche come fotogrammi chiave o fotogrammi di ancoraggio, che sono fotogrammi completamente codificati, e fotogrammi predittivi (fotogrammi P), che vengono codificati come differenza rispetto al fotogramma I precedente. I frame B sono diversi dai frame P perché archiviano sia le differenze rispetto al frame precedente che le differenze rispetto al frame seguente.

Quando si configura il codec per l'uso di fotogrammi B, verrà utilizzato il numero specificato di fotogrammi B tra ogni coppia di fotogrammi di tipo I o P.

Ad esempio, se una sequenza di frame senza frame B è "IPPPPPPPPI", la stessa codifica di sequenza con due frame B sarà "IBBPBBPBBI".

Per la maggior parte del contenuto sono appropriati uno o due frame B. A velocità di dati più elevate, un frame B è in genere la scelta ottimale. Tre o più sono raramente utili.

L'intervallo valido di valori per questa proprietà è compreso tra 0 e 7.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




