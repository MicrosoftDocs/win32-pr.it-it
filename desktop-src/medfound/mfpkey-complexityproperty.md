---
description: "MFPKEY_COMPLEXITY proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092939"
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
| codificatore Windows Media Video 9   | 3             |
| Windows Media Video codificatore 7/8 | 1             |



 

## <a name="remarks"></a>Commenti

Questo valore intero è compreso tra 0 e 3. I valori inferiori determinano l'uso di algoritmi di codifica meno complessi da parte del codec. Anche se gli algoritmi più semplici producono output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




