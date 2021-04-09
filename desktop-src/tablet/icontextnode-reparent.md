---
description: Sposta questo oggetto IContextNode dalla raccolta del nodo di contesto padre dei sottonodi alla raccolta di sottonodi del nodo di contesto specificato.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Metodo IContextNode:: Reparent (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049522"
---
# <a name="icontextnodereparent-method"></a>Metodo IContextNode:: Reparent

Sposta questo oggetto [**IContextNode**](icontextnode.md) dalla raccolta del nodo di contesto padre dei sottonodi alla raccolta di sottonodi del nodo di contesto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNewParent* \[ in\]
</dt> <dd>

Nuovo nodo padre per questo oggetto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

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

[**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




