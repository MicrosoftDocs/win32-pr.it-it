---
description: Determina se l'oggetto IContextNode contiene dati archiviati nell'identificatore specificato.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: Metodo IContextNode::ContainsPropertyData (IACom.h)
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
ms.openlocfilehash: 7bf840b921461f7b767d622a3daecd7b9d3dc3ad8d93b90b7b1f8cfa4d101af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044852"
---
# <a name="icontextnodecontainspropertydata-method"></a>Metodo IContextNode::ContainsPropertyData

Determina se [**l'oggetto IContextNode**](icontextnode.md) contiene dati archiviati nell'identificatore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPropertyDataId* \[ Pollici\]
</dt> <dd>

Identificatore per i dati.

</dd> <dt>

*pbContains* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se [**l'oggetto IContextNode**](icontextnode.md) contiene dati archiviati nell'identificatore specificato; in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Oltre ai dati specifici dell'applicazione, è anche possibile usare questo metodo per determinare se [**questo IContextNode**](icontextnode.md) contiene altri dati interni (vedere [Proprietà hint](analysis-hint-properties.md) di analisi e proprietà del nodo [di contesto).](context-node-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




