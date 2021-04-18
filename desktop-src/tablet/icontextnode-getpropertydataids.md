---
description: Recupera gli identificatori per i quali sono presenti dati della proprietà.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Metodo IContextNode:: GetPropertyDataIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307435"
---
# <a name="icontextnodegetpropertydataids-method"></a>Metodo IContextNode:: GetPropertyDataIds

Recupera gli identificatori per i quali sono presenti dati della proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulGuidCount* \[ out\]
</dt> <dd>

Numero di proprietà.

</dd> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Identificatori per i quali sono presenti dati della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppGuids* quando le informazioni non sono più necessarie.

 

Questo metodo restituisce gli identificatori specifici dell'applicazione per i dati delle proprietà che sono stati aggiunti. Restituisce inoltre gli identificatori per i dati della proprietà interna, descritti dalle costanti delle [proprietà del nodo di contesto](context-node-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

