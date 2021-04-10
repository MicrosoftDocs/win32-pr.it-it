---
description: Specifica la complessità dell'algoritmo del codificatore.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Proprietà MFPKEY_COMPLEXITYEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227022"
---
# <a name="mfpkey_complexityex-property"></a>\_Proprietà COMPLEXITYEX di MFPKEY

Specifica la complessità dell'algoritmo del codificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione codificatore                 | Valore predefinito |
|---------------------------------|---------------|
| Codificatore Windows Media Video 9   | 3             |
| Codificatore Windows Media Video 7/8 | 1             |



 

## <a name="possible-values"></a>Valori possibili

I valori possibili dipendono dalla versione del codificatore video, come illustrato nella tabella seguente.



| Versione codificatore                 | Valori possibili  |
|---------------------------------|------------------|
| Codificatore Windows Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Codificatore Windows Media Video 7/8 | 0, 1             |



 

## <a name="remarks"></a>Commenti

I valori più bassi fanno sì che il codec usi algoritmi di codifica meno complessi. Sebbene gli algoritmi più semplici producano un output di qualità inferiore, il processo di codifica è più veloce e richiede una minore potenza di elaborazione. Questo può essere importante quando si codifica il contenuto da un'origine live, perché il codificatore deve elaborare gli input in modo sufficientemente rapido da restare al passo con l'origine.

Qualsiasi valore assegnato a questa proprietà verrà ignorato se la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) è impostata su 1. In tal caso, MFPKEY \_ COMPLEXITYEX viene impostato automaticamente su 3.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




