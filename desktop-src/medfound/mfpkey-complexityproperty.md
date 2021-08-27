---
description: "MFPKEY_COMPLEXITY proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bb611c95451f590df2e9ff4c1df02b17eda2d1dc00e256381931cbacde435f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113441"
---
# <a name="mfpkey_complexity-property"></a>Proprietà MFPKEY \_ COMPLEXITY

\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece **MFPKEY \_ COMPLEXITYEX.**\]

Specifica la complessità dell'algoritmo del codificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione del codificatore                 | Valore predefinito |
|---------------------------------|---------------|
| Windows Codificatore Media Video 9   | 3             |
| Windows Codificatore Media Video 7/8 | 1             |



 

## <a name="remarks"></a>Commenti

Questo valore intero è compreso tra 0 e 3. I valori inferiori determinano l'uso di algoritmi di codifica meno complessi da parte del codec. Anche se gli algoritmi più semplici producono output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione.

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

 

 




