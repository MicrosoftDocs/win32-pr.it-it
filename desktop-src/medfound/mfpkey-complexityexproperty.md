---
description: "MFPKEY_COMPLEXITYEX proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087609"
---
# <a name="mfpkey_complexityex-property"></a>Proprietà MFPKEY \_ COMPLEXITYEX

Specifica la complessità dell'algoritmo del codificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione del codificatore                 | Valore predefinito |
|---------------------------------|---------------|
| codificatore Windows Media Video 9   | 3             |
| Windows Media Video codificatore 7/8 | 1             |



 

## <a name="possible-values"></a>Valori possibili

I valori possibili dipendono dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione del codificatore                 | Valori possibili  |
|---------------------------------|------------------|
| codificatore Windows Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Windows Media Video codificatore 7/8 | 0, 1             |



 

## <a name="remarks"></a>Commenti

I valori inferiori determinano l'uso di algoritmi di codifica meno complessi da parte del codec. Anche se gli algoritmi più semplici producono output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione. Questo può essere importante quando si codifica il contenuto da un'origine live perché il codificatore deve elaborare gli input in modo sufficientemente veloce da rimanere al passo con l'origine.

Qualsiasi valore assegnato a questa proprietà verrà ignorato se la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) è impostata su 1. In tal caso, MFPKEY \_ COMPLEXITYEX viene impostato automaticamente su 3.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




