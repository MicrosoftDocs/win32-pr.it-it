---
description: "MFPKEY_COMPLEXITYEX proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873538"
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
| Windows Codificatore Media Video 9   | 3             |
| Windows Codificatore Video multimediale 7/8 | 1             |



 

## <a name="possible-values"></a>Valori possibili

I valori possibili dipendono dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione del codificatore                 | Valori possibili  |
|---------------------------------|------------------|
| Windows Codificatore Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Windows Codificatore Video multimediale 7/8 | 0, 1             |



 

## <a name="remarks"></a>Commenti

I valori inferiori causano l'uso di algoritmi di codifica meno complessi da parte del codec. Anche se gli algoritmi più semplici producono un output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione. Questo può essere importante quando si codifica il contenuto da un'origine in tempo reale perché il codificatore deve elaborare gli input abbastanza velocemente da rimanere al passo con l'origine.

Qualsiasi valore assegnato a questa proprietà verrà ignorato se la [proprietà MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) è impostata su 1. In tal caso, MFPKEY \_ COMPLEXITYEX viene impostato automaticamente su 3.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




