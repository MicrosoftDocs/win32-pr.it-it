---
description: Specifica il metodo di costo utilizzato dal codec per determinare la modalità macroblock da usare.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe61be79b07a09d1f55c09b1970c4becbf7aca9818c525420712952bac40db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873285"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>Proprietà MFPKEY \_ MACROBLOCKMODECOSTMETHOD

Specifica il metodo di costo utilizzato dal codec per determinare la modalità macroblock da usare.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Metodo usato                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadamard. Questa opzione configura il codec in modo da usare solo la distorsione durante il calcolo dei costi.             |
| 1     | Costo di Desktop remoto. Questa opzione configura il codec in modo da calcolare sia la frequenza che la distorsione durante il calcolo dei costi. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




