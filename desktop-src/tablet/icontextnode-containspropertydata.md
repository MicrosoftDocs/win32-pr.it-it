---
description: Determina se l'oggetto IContextNode contiene dati archiviati con l'identificatore specificato.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Metodo IContextNode:: ContainsPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485116"
---
# <a name="icontextnodecontainspropertydata-method"></a>Metodo IContextNode:: ContainsPropertyData

Determina se l'oggetto [**IContextNode**](icontextnode.md) contiene dati archiviati con l'identificatore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPropertyDataId* \[ in\]
</dt> <dd>

Identificatore per i dati.

</dd> <dt>

*pbContains* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se l'oggetto [**IContextNode**](icontextnode.md) contiene dati archiviati con l'identificatore specificato. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Oltre ai dati specifici dell'applicazione, è anche possibile usare questo metodo per determinare se questo [**IContextNode**](icontextnode.md) contiene altri dati interni (vedere [proprietà hint di analisi](analysis-hint-properties.md) e [proprietà del nodo di contesto](context-node-properties.md)).

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

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode:: LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




