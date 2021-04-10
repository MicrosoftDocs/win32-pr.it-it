---
description: Specifica la complessità dell'algoritmo del codificatore.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Proprietà MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227021"
---
# <a name="mfpkey_complexity-property"></a>\_Proprietà complessità MFPKEY

\[[**MFPKEY \_ La complessità**](mfpkey-complexityexproperty.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. In alternativa, usare **MFPKEY \_ COMPLEXITYEX**.\]

Specifica la complessità dell'algoritmo del codificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione codificatore                 | Valore predefinito |
|---------------------------------|---------------|
| Codificatore Windows Media Video 9   | 3             |
| Codificatore Windows Media Video 7/8 | 1             |



 

## <a name="remarks"></a>Commenti

Questo valore integer è compreso tra 0 e 3. I valori più bassi fanno sì che il codec usi algoritmi di codifica meno complessi. Sebbene gli algoritmi più semplici producano un output di qualità inferiore, il processo di codifica è più veloce e richiede una minore potenza di elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




